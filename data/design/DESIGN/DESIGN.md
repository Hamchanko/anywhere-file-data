---
name: Vivit Cyber-Pop
colors:
  surface: '#131313'
  surface-dim: '#131313'
  surface-bright: '#3a3939'
  surface-container-lowest: '#0e0e0e'
  surface-container-low: '#1c1b1b'
  surface-container: '#201f1f'
  surface-container-high: '#2a2a2a'
  surface-container-highest: '#353534'
  on-surface: '#e5e2e1'
  on-surface-variant: '#e5bcc4'
  inverse-surface: '#e5e2e1'
  inverse-on-surface: '#313030'
  outline: '#ac878f'
  outline-variant: '#5c3f45'
  surface-tint: '#ffb1c3'
  primary: '#ffb1c3'
  on-primary: '#66002c'
  primary-container: '#ff4b89'
  on-primary-container: '#590026'
  inverse-primary: '#bb0058'
  secondary: '#d3fbff'
  on-secondary: '#00363a'
  secondary-container: '#00eefc'
  on-secondary-container: '#00686f'
  tertiary: '#dfb7ff'
  on-tertiary: '#4b007e'
  tertiary-container: '#ba6bff'
  on-tertiary-container: '#41006f'
  error: '#ffb4ab'
  on-error: '#690005'
  error-container: '#93000a'
  on-error-container: '#ffdad6'
  primary-fixed: '#ffd9e0'
  primary-fixed-dim: '#ffb1c3'
  on-primary-fixed: '#3f0019'
  on-primary-fixed-variant: '#8f0041'
  secondary-fixed: '#7df4ff'
  secondary-fixed-dim: '#00dbe9'
  on-secondary-fixed: '#002022'
  on-secondary-fixed-variant: '#004f54'
  tertiary-fixed: '#f1daff'
  tertiary-fixed-dim: '#dfb7ff'
  on-tertiary-fixed: '#2d004f'
  on-tertiary-fixed-variant: '#6b00b0'
  background: '#131313'
  on-background: '#e5e2e1'
  surface-variant: '#353534'
  neon-lime: '#CCFF00'
  electric-yellow: '#FFF500'
  glitch-white: '#F0F0F0'
  deep-void: '#150020'
typography:
  display-xl:
    fontFamily: anton
    fontSize: 96px
    fontWeight: '400'
    lineHeight: 90px
    letterSpacing: -0.02em
  headline-lg:
    fontFamily: anton
    fontSize: 48px
    fontWeight: '400'
    lineHeight: 48px
    letterSpacing: 0.05em
  headline-lg-mobile:
    fontFamily: anton
    fontSize: 36px
    fontWeight: '400'
    lineHeight: 36px
  headline-md:
    fontFamily: anton
    fontSize: 32px
    fontWeight: '400'
    lineHeight: 32px
  body-lg:
    fontFamily: spaceGrotesk
    fontSize: 18px
    fontWeight: '500'
    lineHeight: 28px
  body-md:
    fontFamily: spaceGrotesk
    fontSize: 16px
    fontWeight: '400'
    lineHeight: 24px
  label-caps:
    fontFamily: jetbrainsMono
    fontSize: 12px
    fontWeight: '700'
    lineHeight: 16px
    letterSpacing: 0.1em
  technical-data:
    fontFamily: jetbrainsMono
    fontSize: 14px
    fontWeight: '400'
    lineHeight: 20px
spacing:
  unit: 4px
  gutter: 24px
  margin-mobile: 16px
  margin-desktop: 48px
  slant-angle: 3deg
---

## Brand & Style

This design system embodies a "Cyber-Pop-Punk" aesthetic, characterized by a hyper-saturated, high-energy visual language. It targets an audience that thrives on disruption, digital subculture, and provocative aesthetics. The UI should feel electric, rebellious, and "vivit"—pulsating with life and digital noise.

The style is a fusion of **High-Contrast / Bold** and **Brutalism**, with a heavy emphasis on glitch-inspired elements. It avoids the polished sterility of modern SaaS in favor of a gritty, over-stimulated interface that feels like a hackable broadcast signal. Key motifs include halftone patterns, scanlines, chromatic aberration effects, and "sticker-slap" layering where elements overlap in a chaotic but intentional hierarchy.

## Colors

The palette is anchored in a high-contrast dark mode. **Neon Pink** serves as the primary driver for action and energy, while **Cyan** provides a digital, synthetic counterpoint. **Deep Purple** and **Deep Void** create the necessary darkness to allow the neon accents to "pop" with maximum intensity.

Avoid traditional semantic colors for success or warning unless they are pushed to their most vibrant extremes. Use **Neon Lime** for success/positive states and **Electric Yellow** or the primary **Neon Pink** for warnings. Black is never flat; it should feel "heavy" and "ink-like," providing a dense backdrop for the glowing UI elements.

## Typography

Typography in this design system is aggressive and functional. **Anton** is used for massive, impactful headlines that demand attention. It should frequently be used in all-caps with tight line heights to create "walls of text" that feel structural.

**Space Grotesk** handles body copy, providing a geometric, technical feel that remains legible amidst the visual noise. **JetBrains Mono** is reserved for labels, metadata, and "system readouts," reinforcing the cyberpunk theme. To enhance the "vivit" style, headlines can occasionally utilize "glitch" treatments, such as slight horizontal offsets or dual-color strokes.

## Layout & Spacing

The layout philosophy rejects standard symmetry in favor of a **Dynamic Fluid Grid**. Use a 12-column system, but intentionally break the grid with overlapping elements and slanted containers. 

A "Slant" motif (roughly 3 degrees) should be applied to major section dividers and button edges to create a sense of forward motion and instability. Spacing is tight and compact; padding should feel intentional rather than generous. Backgrounds should utilize a "noise" or "dot-matrix" texture to fill whitespace, ensuring no part of the screen feels "empty" or "safe."

## Elevation & Depth

Depth is conveyed through **Tonal Layers** and **Hard-Drop Shadows**. This design system avoids soft, natural blurs. Instead:
- **Solid Offsets:** High-elevation elements (like active cards or buttons) use a solid offset shadow in a contrasting brand color (e.g., a Pink card with a Cyan solid shadow).
- **Inner Glows:** Use thin, vibrant inner borders or "neon pulses" to indicate active states.
- **Backdrop Noise:** Background layers should use semi-transparent overlays with scanlines or halftone patterns to create a sense of physical, digital texture.
- **Glassmorphism:** Reserved strictly for "HUD" elements, using a heavy backdrop blur with a high-contrast stroke.

## Shapes

The shape language is strictly **Sharp (0px)**. Rounded corners are non-existent in this design system, as they soften the rebellious "punk" edge. 

To add complexity without using curves, employ "clipped corners" (chamfered edges) on containers and buttons. This 45-degree cut reinforces the technical, aggressive nature of the UI. Use thick, bold strokes (2px - 4px) for borders to ensure elements remain distinct against chaotic backgrounds.

## Components

### Buttons
Buttons are heavy blocks of solid color. The default state should use **Primary Pink** or **Secondary Cyan** with black text. On hover, the button should "glitch"—shifting the color fill or triggering a rapid chromatic aberration animation. The "Slant" or "Clipped Corner" should be used on at least one edge.

### Cards
Cards are containers for data and art. They feature a 2px border in **Glitch White** and often include a "header tab" that looks like a file folder or a mechanical clip. Backgrounds for cards should be slightly transparent to let the grid/noise patterns underneath peek through.

### Inputs & Form Fields
Fields are represented by a single bottom border or a full-stroke box with a monospaced label. When focused, the border should pulse between **Primary Pink** and **Secondary Cyan**. 

### Chips & Tags
Small, all-caps labels using **JetBrains Mono**. They should look like physical dymo-labels or digital tags, often utilizing a "negative" color treatment (black background with neon text).

### Lists
Lists should be separated by thin, dashed lines or "scanline" dividers. Active list items should be highlighted with a full-width neon bar and a "hard" offset shadow.

### Additional Components: "The Glitch Overlay"
A decorative component that randomly appears over images or headers. It consists of thin horizontal slices of the content shifted left or right, styled with a purple/cyan color bleed.