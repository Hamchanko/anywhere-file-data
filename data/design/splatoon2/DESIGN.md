---
name: Ink-Flow Modern
colors:
  surface: '#131313'
  surface-dim: '#131313'
  surface-bright: '#393939'
  surface-container-lowest: '#0e0e0e'
  surface-container-low: '#1b1c1c'
  surface-container: '#1f2020'
  surface-container-high: '#2a2a2a'
  surface-container-highest: '#353535'
  on-surface: '#e5e2e1'
  on-surface-variant: '#bbccb0'
  inverse-surface: '#e5e2e1'
  inverse-on-surface: '#303030'
  outline: '#85957c'
  outline-variant: '#3c4b36'
  surface-tint: '#32e500'
  primary: '#b9ffa0'
  on-primary: '#063900'
  primary-container: '#3bf010'
  on-primary-container: '#126800'
  inverse-primary: '#136e00'
  secondary: '#d3bbff'
  on-secondary: '#40008c'
  secondary-container: '#7600f8'
  on-secondary-container: '#dfccff'
  tertiary: '#ffe8e2'
  on-tertiary: '#5e1700'
  tertiary-container: '#ffc3b1'
  on-tertiary-container: '#a52f00'
  error: '#ffb4ab'
  on-error: '#690005'
  error-container: '#93000a'
  on-error-container: '#ffdad6'
  primary-fixed: '#79ff59'
  primary-fixed-dim: '#32e500'
  on-primary-fixed: '#022100'
  on-primary-fixed-variant: '#0c5300'
  secondary-fixed: '#ebdcff'
  secondary-fixed-dim: '#d3bbff'
  on-secondary-fixed: '#260059'
  on-secondary-fixed-variant: '#5c00c4'
  tertiary-fixed: '#ffdbd0'
  tertiary-fixed-dim: '#ffb59e'
  on-tertiary-fixed: '#3a0a00'
  on-tertiary-fixed-variant: '#852400'
  background: '#131313'
  on-background: '#e5e2e1'
  surface-variant: '#353535'
  neon-pink: '#FF007A'
  electric-yellow: '#E9FF00'
  ink-black: '#111111'
  paper-white: '#FFFFFF'
typography:
  headline-xl:
    fontFamily: Anybody
    fontSize: 48px
    fontWeight: '900'
    lineHeight: '1.1'
    letterSpacing: -0.04em
  headline-lg:
    fontFamily: Anybody
    fontSize: 32px
    fontWeight: '800'
    lineHeight: '1.2'
    letterSpacing: -0.02em
  headline-lg-mobile:
    fontFamily: Anybody
    fontSize: 28px
    fontWeight: '800'
    lineHeight: '1.2'
  body-md:
    fontFamily: Hanken Grotesk
    fontSize: 16px
    fontWeight: '500'
    lineHeight: '1.5'
  body-sm:
    fontFamily: Hanken Grotesk
    fontSize: 14px
    fontWeight: '400'
    lineHeight: '1.4'
  label-caps:
    fontFamily: Space Grotesk
    fontSize: 12px
    fontWeight: '700'
    lineHeight: '1'
    letterSpacing: 0.1em
rounded:
  sm: 0.125rem
  DEFAULT: 0.25rem
  md: 0.375rem
  lg: 0.5rem
  xl: 0.75rem
  full: 9999px
spacing:
  base: 4px
  xs: 8px
  sm: 16px
  md: 24px
  lg: 40px
  xl: 64px
  gutter: 16px
  margin-mobile: 20px
---

## Brand & Style

This design system captures the high-octane energy of urban street culture and competitive play. The brand personality is rebellious, youthful, and unapologetically vibrant. It targets a digital-native audience that values expression, movement, and bold aesthetics.

The visual style is a hybrid of **High-Contrast / Bold** and **Tactile / Splatter** aesthetics. It rejects the sterility of traditional corporate design in favor of dynamic, "ink-stained" interfaces. Expect heavy use of asymmetrical containers, thick borders that mimic marker strokes, and vibrant overlays that suggest a world freshly coated in color.

## Colors

The palette is anchored by a deep **Ink-Black (#222222)** background to ensure the neon "ink" colors achieve maximum luminosity. 

- **Primary (Green):** Used for critical actions and "team" success states.
- **Secondary (Purple):** Used for secondary interactions and depth.
- **Tertiary (Orange):** Reserved for warnings, alerts, and high-energy highlights.
- **Named Colors:** The "Neon-Pink" and "Electric-Yellow" function as alternative team colors, allowing for dynamic UI themes that shift based on context (e.g., different "matches" or "modes").

All colors should be applied with high saturation. Gradients should be used sparingly, favoring hard-edged transitions or halftone patterns to mimic screen-printing.

## Typography

The typography is built on a "variable-width" philosophy. **Anybody** serves as the primary headline face, chosen for its ability to feel stretched and compressed, much like graffiti tags. It should be used at heavy weights (800+) for maximum impact.

**Hanken Grotesk** provides a clean, contemporary contrast for body text, ensuring readability amidst the chaotic visual environment. **Space Grotesk** is used for technical labels and UI metadata, providing a "tech-street" vibe that feels precise yet modern.

Headlines should occasionally be rotated by 2-3 degrees to break the formal grid and enhance the dynamic feel.

## Layout & Spacing

This design system uses a **Fluid Grid** with a 4px base unit. For mobile-first implementation, a 4-column grid is standard, expanding to 12 columns on desktop.

The spacing philosophy is "dense but intentional." Elements should feel packed together to simulate the intensity of a match. Use **asymmetrical padding** (e.g., more padding on the left than the right) for containers to create a sense of forward motion. 

Margins on mobile should be kept tight (20px) to allow the content to dominate the screen. Negative margins are encouraged for "sticker" elements that overlap multiple sections.

## Elevation & Depth

Depth is conveyed through **Bold Borders** and **Offset Shadows** rather than realistic lighting.

- **Hard-Edge Shadows:** Instead of blurs, use solid color offsets (usually in Ink-Black or a darker shade of the primary color) at a 4px or 8px distance.
- **Tonal Layering:** Use the `neutral` color tiers to separate background elements, but always finish with a high-contrast border (2px to 4px thickness) to "cut" the element out from the background.
- **Ink Overlays:** Critical UI elements (like "Level Up" notifications) should use semi-transparent "ink splatter" masks as their background layer to feel integrated into the environment.

## Shapes

The shape language is "Calculated Chaos." While base components use a **Soft (0.25rem)** roundedness for structural integrity, secondary elements should utilize **organic, irregular clipping masks**.

Buttons should not be perfect rectangles; they should have slight "wobbles" or ink-drip protrusions at the corners. For standard containers, use a "cut-corner" or "slanted" edge style to maintain the aggressive, urban aesthetic. Circular elements should appear slightly hand-drawn or "splattered" rather than perfectly geometric.

## Components

- **Buttons:** Primary buttons must have a 3px solid border and a 4px offset "hard" shadow. On hover/active states, the button and its shadow should "squish" (translate Y +2px).
- **Chips/Tags:** Styled as "Stickers." These should have a slight rotation (-2 to +2 degrees) and a white "die-cut" border.
- **Input Fields:** Use a heavy bottom-border only (4px) in the primary color. The placeholder text should use the `label-caps` typography style.
- **Cards:** Cards do not use shadows; they use a "slanted" background container. The header of the card should be a high-contrast bar of color with the title in white.
- **Progress Bars:** Designed to look like "Ink Tanks." As the bar fills, the "liquid" should have a slight wave animation at the leading edge.
- **Modals:** Instead of standard fades, modals should "splash" onto the screen using a scale-in animation with an ink-blot mask.