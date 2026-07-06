---
name: Warm Community Narrative
colors:
  surface: '#fcf9f8'
  surface-dim: '#dcd9d9'
  surface-bright: '#fcf9f8'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#f6f3f2'
  surface-container: '#f0eded'
  surface-container-high: '#eae7e7'
  surface-container-highest: '#e5e2e1'
  on-surface: '#1c1b1b'
  on-surface-variant: '#59413c'
  inverse-surface: '#313030'
  inverse-on-surface: '#f3f0ef'
  outline: '#8d716b'
  outline-variant: '#e1bfb8'
  surface-tint: '#ad3319'
  primary: '#ad3319'
  on-primary: '#ffffff'
  primary-container: '#f66748'
  on-primary-container: '#5d0d00'
  inverse-primary: '#ffb4a4'
  secondary: '#655d51'
  on-secondary: '#ffffff'
  secondary-container: '#eadece'
  on-secondary-container: '#6a6155'
  tertiary: '#00696b'
  on-tertiary: '#ffffff'
  tertiary-container: '#00a5a7'
  on-tertiary-container: '#003334'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#ffdad3'
  primary-fixed-dim: '#ffb4a4'
  on-primary-fixed: '#3d0600'
  on-primary-fixed-variant: '#8b1a02'
  secondary-fixed: '#ede1d1'
  secondary-fixed-dim: '#d0c5b5'
  on-secondary-fixed: '#201b11'
  on-secondary-fixed-variant: '#4d463a'
  tertiary-fixed: '#7bf5f7'
  tertiary-fixed-dim: '#5cd8da'
  on-tertiary-fixed: '#002020'
  on-tertiary-fixed-variant: '#004f50'
  background: '#fcf9f8'
  on-background: '#1c1b1b'
  surface-variant: '#e5e2e1'
  surface-warm: '#FFF9EC'
  accent-orange: '#F66748'
  muted-earth: '#E8DCCC'
  deep-text: '#1A1A1A'
  pure-white: '#FFFFFF'
typography:
  display-lg:
    fontFamily: Noto Sans
    fontSize: 48px
    fontWeight: '700'
    lineHeight: '1.2'
    letterSpacing: -0.02em
  display-lg-mobile:
    fontFamily: Noto Sans
    fontSize: 32px
    fontWeight: '700'
    lineHeight: '1.2'
  headline-md:
    fontFamily: Noto Sans
    fontSize: 24px
    fontWeight: '700'
    lineHeight: '1.4'
  headline-sm:
    fontFamily: Noto Sans
    fontSize: 20px
    fontWeight: '700'
    lineHeight: '1.4'
  body-lg:
    fontFamily: Noto Sans
    fontSize: 18px
    fontWeight: '400'
    lineHeight: '1.6'
  body-md:
    fontFamily: Noto Sans
    fontSize: 16px
    fontWeight: '400'
    lineHeight: '1.6'
  label-md:
    fontFamily: Noto Sans
    fontSize: 14px
    fontWeight: '500'
    lineHeight: '1.4'
    letterSpacing: 0.05em
  label-sm:
    fontFamily: Noto Sans
    fontSize: 12px
    fontWeight: '500'
    lineHeight: '1.4'
rounded:
  sm: 0.25rem
  DEFAULT: 0.5rem
  md: 0.75rem
  lg: 1rem
  xl: 1.5rem
  full: 9999px
spacing:
  base: 8px
  xs: 4px
  sm: 12px
  md: 24px
  lg: 48px
  xl: 80px
  container-max: 1200px
  gutter: 24px
---

## Brand & Style

The design system is centered on the concept of "Nurturing Connections." It targets a multi-generational community, emphasizing warmth, accessibility, and mutual support. The aesthetic is a blend of **Modern Minimalism** and **Tactile Organicism**, prioritizing human-centric layouts that feel inviting rather than institutional.

The visual narrative uses soft, high-quality whitespace and organic color transitions to evoke a sense of calm and reliability. Key attributes include:
- **Approachability:** Using rounded forms and warm neutral backgrounds.
- **Clarity:** Bold typography and high-contrast accents to guide users of all ages.
- **Vitality:** Strategic use of energetic orange to highlight points of engagement and growth.

## Colors

The palette is rooted in an "Earth & Sun" metaphor. The primary color is a vibrant orange (`#F66748`), used for calls to action and critical brand moments. The background avoids stark whites in favor of a warm cream (`#FFF9EC`), which reduces eye strain and reinforces the community feel.

- **Primary:** Vitality and action. Used for primary buttons, active states, and highlights.
- **Secondary:** Grounding and stability. Used for secondary UI elements, borders, and subtle backgrounds.
- **Neutral:** Precision and depth. The deep charcoal (`#1A1A1A`) is used for primary text to ensure maximum legibility against warm backgrounds.
- **Surface:** The off-white (`#FFFFFF`) is reserved for cards and elevated components to provide crisp contrast against the cream page background.

## Typography

This design system utilizes **Noto Sans** for its universal legibility and friendly humanist qualities. The type scale is generous, prioritizing readability for a diverse audience.

- **Headlines:** Use heavy weights (700) with slightly tighter letter spacing to create strong visual anchors.
- **Body Text:** Set with ample line heights (1.6) to ensure comfort during long-form reading.
- **Labels:** Use medium weights (500) and increased letter spacing to distinguish functional metadata from narrative content.
- **Hierarchy:** Maintain a clear distinction between levels by combining size changes with weight shifts. For Japanese character support, ensure Noto Sans JP is loaded as the primary fallback.

## Layout & Spacing

The layout follows a **Fluid-Fixed Hybrid** model. Content is contained within a 1200px maximum width on desktop but fluidly adapts on smaller screens. 

- **Grid:** A 12-column grid system is used for desktop, 8-column for tablet, and 4-column for mobile.
- **Rhythm:** Spacing is built on an 8px base unit. Section vertical spacing (`xl`) is significant to create "breathing room," reinforcing the calm brand personality.
- **Margins:** Mobile margins are set to `md` (24px) to ensure touch targets don't crowd the edge of the screen.

## Elevation & Depth

This design system uses **Tonal Layers** and **Soft Ambient Shadows** to convey hierarchy. Depth is physical but subtle, mimicking paper or soft surfaces.

- **Level 0 (Background):** `#FFF9EC` - The base canvas.
- **Level 1 (Cards/Surfaces):** `#FFFFFF` - Used for primary content containers. These use a very soft, low-blur shadow with a hint of the brand secondary color (`#E8DCCC`) in the shadow tint.
- **Level 2 (Interactive/Floating):** Used for dropdowns and modals. These feature a more defined shadow to indicate they sit above the primary content plane.
- **Interactive State:** Hovering over a Level 1 card should subtly increase its elevation through a slightly deeper shadow and a -4px Y-axis shift.

## Shapes

The shape language is consistently **Rounded**, avoiding sharp corners to maintain a friendly, non-threatening atmosphere.

- **Standard Elements:** 0.5rem (8px) radius for buttons, input fields, and small cards.
- **Large Containers:** 1rem (16px) or 1.5rem (24px) radius for section containers and primary cards to emphasize a "soft" container feel.
- **Icons:** Should follow a rounded cap and join style to match the UI's geometry.

## Components

### Buttons
- **Primary:** Solid `#F66748` with white text. High-contrast, rounded corners.
- **Secondary:** Outlined with `#F66748` or solid `#E8DCCC` with `#1A1A1A` text for less urgent actions.
- **Ghost:** Transparent background with `#F66748` text, used for tertiary navigation.

### Inputs & Fields
- Fields should use the `#FFFFFF` surface color with a 1px border of `#E8DCCC`. 
- On focus, the border transitions to `#F66748` with a soft glow.

### Cards
- White backgrounds (`#FFFFFF`) on the cream page background (`#FFF9EC`).
- Padding should be generous (`md` or `lg`) to prevent content crowding.
- Use `rounded-lg` (16px) for main content cards.

### Chips & Tags
- Used for categories or status indicators.
- Light tint backgrounds using 10% opacity of the primary or secondary colors to keep them subtle and integrated.

### List Items
- Separated by soft `#E8DCCC` horizontal rules.
- Include generous vertical padding to facilitate easy mobile tapping.