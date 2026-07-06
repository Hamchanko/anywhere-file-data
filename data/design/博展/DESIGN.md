---
name: Experiential Minimalism
colors:
  surface: '#f9f9f9'
  surface-dim: '#dadada'
  surface-bright: '#f9f9f9'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#f3f3f3'
  surface-container: '#eeeeee'
  surface-container-high: '#e8e8e8'
  surface-container-highest: '#e2e2e2'
  on-surface: '#1a1c1c'
  on-surface-variant: '#444748'
  inverse-surface: '#2f3131'
  inverse-on-surface: '#f1f1f1'
  outline: '#747878'
  outline-variant: '#c4c7c7'
  surface-tint: '#5f5e5e'
  primary: '#1e1e1e'
  on-primary: '#ffffff'
  primary-container: '#333333'
  on-primary-container: '#9c9b9b'
  inverse-primary: '#c8c6c6'
  secondary: '#5d5f5f'
  on-secondary: '#ffffff'
  secondary-container: '#dfe0e0'
  on-secondary-container: '#616363'
  tertiary: '#201e1c'
  on-tertiary: '#ffffff'
  tertiary-container: '#353331'
  on-tertiary-container: '#9f9b98'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#e4e2e1'
  primary-fixed-dim: '#c8c6c6'
  on-primary-fixed: '#1b1c1c'
  on-primary-fixed-variant: '#474747'
  secondary-fixed: '#e2e2e2'
  secondary-fixed-dim: '#c6c6c7'
  on-secondary-fixed: '#1a1c1c'
  on-secondary-fixed-variant: '#454747'
  tertiary-fixed: '#e7e1de'
  tertiary-fixed-dim: '#cac6c2'
  on-tertiary-fixed: '#1d1b1a'
  on-tertiary-fixed-variant: '#494644'
  background: '#f9f9f9'
  on-background: '#1a1c1c'
  surface-variant: '#e2e2e2'
  deep-charcoal: '#333333'
  pure-white: '#FFFFFF'
  system-gray: '#999999'
  subtle-ash: '#E0E0E0'
typography:
  display-xl:
    fontFamily: Be Vietnam Pro
    fontSize: 72px
    fontWeight: '700'
    lineHeight: 80px
    letterSpacing: -0.04em
  display-xl-mobile:
    fontFamily: Be Vietnam Pro
    fontSize: 40px
    fontWeight: '700'
    lineHeight: 48px
    letterSpacing: -0.02em
  headline-lg:
    fontFamily: Be Vietnam Pro
    fontSize: 32px
    fontWeight: '600'
    lineHeight: 40px
    letterSpacing: -0.01em
  headline-lg-mobile:
    fontFamily: Be Vietnam Pro
    fontSize: 24px
    fontWeight: '600'
    lineHeight: 32px
  body-lg:
    fontFamily: Noto Sans
    fontSize: 18px
    fontWeight: '400'
    lineHeight: 32px
  body-md:
    fontFamily: Noto Sans
    fontSize: 16px
    fontWeight: '400'
    lineHeight: 28px
  label-sm:
    fontFamily: Be Vietnam Pro
    fontSize: 12px
    fontWeight: '600'
    lineHeight: 16px
    letterSpacing: 0.1em
spacing:
  unit: 8px
  gutter: 24px
  margin-desktop: 80px
  margin-mobile: 20px
  max-width: 1440px
---

## Brand & Style

The design system is rooted in the philosophy of "Communication Design"—the intersection of physical space and digital precision. It targets a sophisticated audience of creators, brand managers, and architects who value clarity, intentionality, and the power of white space. 

The visual style is a rigorous **Minimalism** with a focus on high-end editorial aesthetics. It prioritizes the "stage" for content, allowing photography and case studies of physical exhibitions to become the primary visual driver. By utilizing a restricted palette and stark layouts, the UI evokes an emotional response of professional authority, quiet confidence, and avant-garde creativity. Every element is stripped of decorative excess to ensure that the experiential nature of the work remains the focal point.

## Colors

This design system employs a strictly monochrome palette to maintain a premium, gallery-like atmosphere. The primary color, a deep charcoal (#333333), is used for all essential structural elements and primary typography, providing a softer, more sophisticated alternative to pure black. 

The secondary color is pure white, used extensively for background surfaces to create "negative space" that guides the user's eye toward content. Accents should be used with extreme discipline; color is only introduced via high-resolution imagery or video of physical installations. In rare functional instances, a neutral system gray is utilized for secondary metadata or disabled states to maintain the hierarchical integrity of the monochrome theme.

## Typography

The typography system is built on a dual-font strategy that balances contemporary flair with global legibility. **Be Vietnam Pro** is used for headlines and labels; its geometric yet warm character provides a distinctive edge to the brand’s "experiential" narrative. High-contrast sizing between displays and body text creates a clear, architectural hierarchy.

**Noto Sans** (international variant) is used for all body copy to ensure maximum readability and cross-cultural compatibility, essential for global exhibitions. Text is generally set with generous line heights to preserve the feeling of openness. Labels and navigation items use uppercase styling with increased letter spacing to mirror the signage found in physical architectural environments.

## Layout & Spacing

This design system utilizes a **Fixed Grid** model for desktop and a **Fluid Grid** for mobile devices. The desktop layout is centered within a 1440px container with wide 80px side margins, mimicking the expansive feel of a gallery wall. 

A 12-column grid is the foundation, but content should frequently span 6 or 8 columns to create asymmetrical, dynamic compositions that suggest movement and depth. Spacing is governed by a strict 8px base unit. Vertical rhythm is intentionally exaggerated, with large gaps (120px–160px) between major sections to allow the user to "breathe" between different creative showcases.

## Elevation & Depth

To maintain a minimalist and sophisticated aesthetic, this design system avoids traditional drop shadows. Depth is instead communicated through **Tonal Layers** and **Low-contrast Outlines**. 

Surfaces are predominantly flat. When layering is required (such as in navigation bars or modals), the system uses subtle 1px borders in `subtle-ash` (#E0E0E0) or very slight shifts in background lightness. For high-interactivity moments, a "glass" effect may be used with a background blur, but only to signify a temporary overlay that does not distract from the primary content. The hierarchy is primarily "Z-axis through scale" rather than "Z-axis through shadow."

## Shapes

The shape language is strictly **Sharp (0)**. To reflect the precision of architectural design and exhibition structures, all containers, buttons, and image wrappers utilize 90-degree corners. This uncompromising geometry reinforces the brand's professional and structural identity. Circular elements are reserved exclusively for icon backgrounds or specific "interactive nodes" to create a deliberate contrast against the otherwise rectangular environment.

## Components

### Buttons
Primary buttons are solid `deep-charcoal` blocks with white uppercase `label-sm` text. They feature no rounding and use a "fill-to-border" hover animation. Secondary buttons are outlined (ghost) style with a 1px charcoal stroke.

### Input Fields
Inputs consist of a single bottom border (1px) rather than a full box. Labels sit above the line in a small, tracked-out uppercase font. The focus state is indicated by the border darkening and a subtle vertical expansion of the line.

### Cards
Cards for showcasing projects are "borderless." The image occupies the full width of the card, with metadata (title, category, date) placed below with significant padding. On hover, the image should subtly scale up within its sharp-edged container to create a "zoom-in" experiential effect.

### Chips & Tags
Tags are used for categorizing exhibitions. They are rendered as simple text strings separated by a vertical pipe (|) or placed in small, sharp-cornered boxes with a light gray background and no border.

### Navigation
The navigation is minimalist and persistent. It utilizes a "hidden until needed" or a very slim top-bar approach. Menu items use the `label-sm` style and change opacity on hover rather than changing color.