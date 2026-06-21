# Anywhere.file ― 企画書

> どのPCからでも、URLにアクセスすれば自分のファイルへ到達できる「個人専用ファイルアクセスポイント」。
> 保管先は GitHub に直接。フロント（サイト本体）は GitHub Pages で公開し、ファイル実体は別の private リポジトリに置く。

---

## 0. この企画書の前提と結論

- **保管先**：GitHub リポジトリに直接（追加インフラ・サーバー不要、無料、自動バージョン管理）。
- **最重要の設計判断**：「公開URLでどこからでもアクセス」と「中身は自分だけ」を両立させるため、**リポジトリを2つに分ける**。
  - フロント（`index.html` など）→ **public** リポジトリ＋GitHub Pages で公開（コードだけ公開される）。
  - ファイル実体（Pythonプロジェクト・DESIGN.md・画像）→ **private** リポジトリに格納し、ブラウザから GitHub API（トークン認証）でのみ読み書き。
- これにより、URLを知っていてもトークンが無い人はファイルを取得できない。

### なぜ1リポジトリではダメか（確認済みの事実）

| 事項 | 事実 |
|---|---|
| Pages のアクセス制限付き公開 | **GitHub Enterprise Cloud 限定**。個人の Free/Pro では不可。 |
| private リポジトリの Pages 公開 | 公開設定にすると、ソースは隠れるが**ビルド済み静的ファイルは誰でもURLで閲覧可能**。 |
| 結論 | フロントとデータを同じ公開リポジトリに置くと、アップロードした個人ファイルが世界に公開される。→ 分離必須。 |

---

## 1. 全体アーキテクチャ

```
[どのPCのブラウザ]
      │ ① 公開URLにアクセス
      ▼
[ anywhere-file (public) ] ── GitHub Pages ──▶ index.html / app.js / style.css を配信
      │
      │ ② 初回にトークン(PAT)を入力 → sessionStorage に一時保持（コードには埋め込まない）
      ▼
[ GitHub REST API ] ◀── ③ トークン認証で読み書き ──▶ [ anywhere-file-data (private) ]
                                                          ├ data/python/...
                                                          ├ data/design/...
                                                          └ manifest.json（索引）
```

- **読み取り**：起動時に `manifest.json` を取得して一覧表示。各ファイルは Contents API か Git Blob で取得。
- **書き込み（単一ファイル）**：DESIGN.md・画像は Contents API（PUT）で1ファイルずつコミット。
- **書き込み（フォルダ一括）**：Pythonプロジェクトは Git Data API（blobs → tree → commit → ref更新）で**フォルダ丸ごとを1コミット**にまとめる。

---

## 2. リポジトリ構成 ― どこに何を置くか

### 2-1. `anywhere-file`（public・Pagesで公開）

```
anywhere-file/                  # public リポジトリ（GitHub Pages で公開）
├── index.html                  # サイト本体（現サンプルHTMLがここに入る）
├── assets/
│   ├── app.js                  # GitHub API連携ロジック（将来CSS/JSを分離する場合）
│   └── style.css               # スタイル（分離しない場合は index.html 内のままでも可）
├── DESIGN.md                   # サイト自身のデザイン規約（参照用・任意）
└── README.md                   # 使い方
```

- ここに置くのは**コードだけ**。個人ファイルは絶対に置かない。
- `assets/` にトークンや個人情報を書き込まない（公開されるため）。

### 2-2. `anywhere-file-data`（private・ファイル実体）

```
anywhere-file-data/             # private リポジトリ（トークン保有者のみアクセス可）
├── manifest.json               # 全登録アイテムの索引（一覧表示・検索の元データ）
├── data/
│   ├── python/                 # 「Python」タブの保管先
│   │   ├── tohshi/             # プロジェクト＝フォルダ単位で格納
│   │   │   ├── main.py
│   │   │   ├── requirements.txt
│   │   │   └── _meta.json      # このプロジェクトの「一言説明」など
│   │   └── booking_scraper/
│   │       ├── booking_jp_scraper.py
│   │       └── _meta.json
│   └── design/                 # 「DESIGN.md」タブの保管先
│       ├── vivit-cyber-pop/
│       │   ├── DESIGN.md
│       │   └── images/         # プレビュー用画像
│       │       ├── sample01.png
│       │       └── sample02.png
│       └── ...
└── .gitkeep                    # 空フォルダ維持用（初期化時）
```

### 2-3. 各要素の役割

| パス | 役割 |
|---|---|
| `manifest.json` | サイトが最初に読む索引。何が登録済みかを一覧化（後述） |
| `data/python/<project>/` | Pythonプロジェクトをフォルダ単位で格納。zip不要 |
| `data/python/<project>/_meta.json` | 「何をするファイルか」の一言説明・登録日時を保持 |
| `data/design/<name>/DESIGN.md` | DESIGN.md 単体 |
| `data/design/<name>/images/` | デザインプレビュー用画像 |

---

## 3. manifest.json の設計（一覧管理の中核）

サイトは起動時にこれを読んで、タブごとの一覧を描画する。アップロード／削除のたびに更新してコミットする。

```json
{
  "updated": "2026-06-14T12:00:00Z",
  "python": [
    {
      "name": "tohshi",
      "desc": "上場企業のPVティアを判定するデータパイプライン",
      "path": "data/python/tohshi/",
      "fileCount": 12,
      "updated": "2026-06-14T12:00:00Z"
    }
  ],
  "design": [
    {
      "name": "vivit-cyber-pop",
      "path": "data/design/vivit-cyber-pop/DESIGN.md",
      "images": ["data/design/vivit-cyber-pop/images/sample01.png"],
      "updated": "2026-06-14T12:00:00Z"
    }
  ]
}
```

- `desc`（一言説明）は、現サンプルの「WHAT IT DOES // 一言説明」入力欄の値をそのまま保存。
- 一覧描画はこの manifest だけで完結するので、毎回リポジトリ全体を走査しなくて済む（高速）。

---

## 4. 作成手順 ― どう作るか

> Claude（AI）はリポジトリ作成や複数フォルダの一括生成ができません。
> **★印の手動作業はご自身で**、それ以外（コード生成）は私が担当します。

1. **★ public リポジトリ `anywhere-file` を作成**。
2. ここに `index.html`（私が用意）を配置。
3. **★ Settings → Pages** でブランチ（main）を選び Pages を有効化。`https://<ユーザー名>.github.io/anywhere-file/` が公開URLになる。
4. **★ private リポジトリ `anywhere-file-data` を作成**。初期コミットで `manifest.json`（中身は空配列）と `data/.gitkeep` を置く。
   - 空フォルダはGitに置けないため、各階層に `.gitkeep` を1つ入れて初期化する。
5. **★ Fine-grained Personal Access Token を発行**。
   - 対象リポジトリ：`anywhere-file-data` のみ。
   - 権限：`Contents` の **Read and write** だけ（最小権限）。
   - 有効期限を設定（例：90日）。
6. 公開URLにアクセスし、初回にトークンを入力 → `sessionStorage` に一時保持（タブを閉じると消える）。
7. 以降、UIの UPLOAD から `anywhere-file-data` にコミットされる。

---

## 5. 認証・容量・セキュリティの整理

### 5-1. トークンの扱い（最重要）

- トークンは **コード・HTML・JSに絶対に埋め込まない**（公開Pagesから漏洩するため）。
- 実行時に入力欄から受け取り、`sessionStorage` に保持。`localStorage` への長期保存は漏洩リスクが上がるため非推奨。
- Fine-grained PAT で**対象リポジトリと権限を最小化**（data リポジトリの Contents だけ）。

### 5-2. 容量の上限（GitHubの制約）

| 対象 | 目安 |
|---|---|
| 1ファイル | 100MB がハード上限（50MB超で警告）。大容量は Git LFS か別ストレージ検討 |
| リポジトリ | 1GB 未満を推奨（〜数GBで警告） |
| API経由のファイル作成 | 巨大ファイルは Contents API より Git Data API（blob）向き |

- 大きなデータ（CSV・SQLite・モデル等）を多数置く運用なら、別途 Git LFS か外部ストレージ（後日検討）に逃がす方針を推奨。

### 5-3. 公開範囲（再掲）

- フロントは公開されてよい（コードのみ）。
- データは private リポジトリ＋トークンでガード。トークンが無ければ URL を知っていても取得不可。

---

## 6. 実装フェーズ

| フェーズ | 内容 | 状態 |
|---|---|---|
| Phase 0 | UIサンプル（タブ・アップロードUI・DESIGN.mdプレビュー） | ✅ 完了（現HTML） |
| Phase 1 | 起動時に `manifest.json` を読み取り、一覧を実データで描画 | 未 |
| Phase 2 | 単一ファイルアップロード（DESIGN.md・画像）→ Contents API でコミット | 未 |
| Phase 3 | フォルダ一括アップロード（Python）→ Git Data API で1コミット | 未 |
| Phase 4 | 一言説明（_meta）の保存・更新・削除、トークン入力UI | 未 |

---

## 7. 次のアクション（承認後に私がやること）

この企画書の方向で問題なければ、次の順で実装コードを用意します。

1. 現 `index.html` に **トークン入力UI** と **GitHub API連携（Phase 1：一覧読み取り）** を追加した版。
2. **Phase 2（単一アップロード）** → **Phase 3（フォルダ一括）** の順で機能追加。
3. 各段階ごとにファイルを分けて出力（**今後は版を上書きせず、別名で残します**）。

手動でお願いする部分（★）は、リポジトリ2つの作成・Pages有効化・トークン発行のみです。

---

### 確認したい論点（任意・企画を詰めるなら）

- データ用リポジトリを **private 1個** で進めるか、Pythonとデザインで分けるか。
- 大容量データを扱う予定があるか（あれば Git LFS / 外部ストレージを最初から設計に入れる）。
- トークンは毎回入力で良いか（より楽にしたい場合は別方式を検討）。
