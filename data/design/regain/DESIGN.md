---
name: Corporate Precision
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
  secondary: '#ba0032'
  on-secondary: '#ffffff'
  secondary-container: '#e41944'
  on-secondary-container: '#fffbff'
  tertiary: '#2f171c'
  on-tertiary: '#ffffff'
  tertiary-container: '#462c31'
  on-tertiary-container: '#b79298'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#e4e2e1'
  primary-fixed-dim: '#c8c6c6'
  on-primary-fixed: '#1b1c1c'
  on-primary-fixed-variant: '#474747'
  secondary-fixed: '#ffdada'
  secondary-fixed-dim: '#ffb3b5'
  on-secondary-fixed: '#40000b'
  on-secondary-fixed-variant: '#920025'
  tertiary-fixed: '#ffd9de'
  tertiary-fixed-dim: '#e5bcc2'
  on-tertiary-fixed: '#2c1519'
  on-tertiary-fixed-variant: '#5c3f44'
  background: '#f9f9f9'
  on-background: '#1a1c1c'
  surface-variant: '#e2e2e2'
  surface-white: '#FFFFFF'
  accent-red: '#FF3355'
  soft-pink: '#FFD5DB'
  text-primary: '#333333'
  bg-off-white: '#F8F8F8'
typography:
  display-lg:
    fontFamily: Inter
    fontSize: 48px
    fontWeight: '700'
    lineHeight: 56px
    letterSpacing: -0.02em
  display-lg-mobile:
    fontFamily: Inter
    fontSize: 32px
    fontWeight: '700'
    lineHeight: 40px
    letterSpacing: -0.01em
  headline-lg:
    fontFamily: Inter
    fontSize: 32px
    fontWeight: '600'
    lineHeight: 40px
  headline-lg-mobile:
    fontFamily: Inter
    fontSize: 24px
    fontWeight: '600'
    lineHeight: 32px
  headline-md:
    fontFamily: Inter
    fontSize: 24px
    fontWeight: '600'
    lineHeight: 32px
  body-lg:
    fontFamily: Noto Sans
    fontSize: 18px
    fontWeight: '400'
    lineHeight: 28px
  body-md:
    fontFamily: Noto Sans
    fontSize: 16px
    fontWeight: '400'
    lineHeight: 24px
  body-sm:
    fontFamily: Noto Sans
    fontSize: 14px
    fontWeight: '400'
    lineHeight: 20px
  label-md:
    fontFamily: Inter
    fontSize: 12px
    fontWeight: '600'
    lineHeight: 16px
    letterSpacing: 0.05em
  label-sm:
    fontFamily: Inter
    fontSize: 10px
    fontWeight: '500'
    lineHeight: 14px
rounded:
  sm: 0.125rem
  DEFAULT: 0.25rem
  md: 0.375rem
  lg: 0.5rem
  xl: 0.75rem
  full: 9999px
spacing:
  base: 8px
  container-max: 1200px
  gutter: 24px
  margin-mobile: 16px
  margin-desktop: 40px
  section-gap-lg: 80px
  section-gap-sm: 40px
---

## Brand & Style

The design system is engineered for a professional, high-trust corporate environment that balances Japanese precision with modern global aesthetics. It targets B2B stakeholders, focusing on reliability, structural integrity, and clarity.

The visual style is **Corporate / Modern** with a strong emphasis on **Minimalism**. It utilizes expansive white space, a structured grid, and a restrained color palette to ensure the content remains the primary focus. The aesthetic avoids unnecessary decoration, opting instead for crisp typography and subtle tonal changes to guide the user through complex information. The emotional response is one of stability, authority, and meticulous attention to detail.

## Colors

The palette is built on a foundation of high-contrast neutrals to maintain a professional "newsroom" or "consultancy" feel. 

- **Primary:** A deep charcoal (#333333) is used for primary typography and core structural elements, providing a softer, more sophisticated alternative to pure black.
- **Secondary/Accent:** A vibrant crimson (#FF3355) serves as the primary action color. It is used sparingly for call-to-action buttons, key highlights, and important status indicators to ensure high visibility against the neutral background.
- **Tertiary:** A muted pink (#FFD5DB) acts as a background tint for secondary containers or highlight regions, softening the impact of the primary red.
- **Neutrals:** White (#FFFFFF) and light gray (#F8F8F8) are the workhorses of the layout, used to create "breathing room" and distinguish different content sections through subtle tonal shifts.

## Typography

The typographic system leverages **Inter** for structural elements and headlines due to its geometric clarity and exceptional legibility at various weights. **Noto Sans** is utilized for body copy, providing a warm and readable experience for long-form content, particularly for multi-language support.

- **Headlines:** Use tight letter-spacing and bold weights for a commanding presence.
- **Body:** Prioritize line height (1.5x minimum) to enhance readability.
- **Mobile Scaling:** Large display styles scale down significantly for mobile devices to maintain a clean viewport without excessive horizontal overflow.
- **Hierarchy:** Use the Label-md style for small eyebrow text above headings to provide context without adding visual weight.

## Layout & Spacing

This design system uses a **Fluid Grid** model with a hard 8px baseline rhythm.

- **Desktop:** A 12-column grid with a 1200px max-width container. Margins are generous (40px) to maintain the minimalist aesthetic.
- **Mobile:** A 4-column grid with 16px side margins. Content is primarily stacked vertically.
- **Spacing Philosophy:** Use "Section Gaps" to clearly delineate different content areas. Large sections are separated by 80px on desktop, scaling to 40px on mobile. 
- **Alignment:** All elements should align to the 8px grid. Text should be left-aligned to maintain a formal, structured feel; center-alignment is reserved only for hero introductions.

## Elevation & Depth

Hierarchy is established through **Tonal Layers** rather than heavy shadows. This reinforces the minimalist, modern corporate identity.

- **Level 0 (Base):** The primary background color (#FFFFFF or #F8F8F8).
- **Level 1 (Subtle):** Use #F8F8F8 sections against a #FFFFFF background to create regional separation.
- **Outlines:** Use thin (1px), low-contrast borders (#E0E0E0) for card components to provide structure without adding visual "noise."
- **Shadows:** When necessary (e.g., active dropdowns or modals), use a single, highly diffused "Ambient Shadow": `0px 4px 20px rgba(0, 0, 0, 0.05)`. Avoid dark or high-opacity shadows.

## Shapes

The shape language is **Soft** and restrained.

- **Standard Elements:** Buttons, input fields, and small cards use a 4px (0.25rem) corner radius. This provides a professional "edge" that is approachable but not overly playful.
- **Large Containers:** Content blocks or larger cards use an 8px (0.5rem) radius to feel more integrated into the layout.
- **Interactive Elements:** Buttons never use pill shapes; they maintain a rectangular form with subtle rounding to align with the corporate architectural style.

## Components

### Buttons
- **Primary:** Solid #FF3355 background with white text. 4px roundedness. No gradient.
- **Secondary:** Transparent background with a 1px border of #333333 and #333333 text.
- **Hover States:** Primary buttons darken slightly; secondary buttons gain a very light gray (#F8F8F8) background fill.

### Input Fields
- **Styling:** White background, 1px border (#E0E0E0), 4px roundedness.
- **Focus:** Border color changes to #333333 with a subtle 2px outer glow of the same color at 10% opacity.

### Cards
- **Structure:** Flat background (#FFFFFF) with a thin #F8F8F8 or #E0E0E0 border.
- **Padding:** 24px internal padding for desktop, 16px for mobile.

### Chips & Tags
- **Styling:** Use the Soft Pink (#FFD5DB) background with dark text for categorizing content. No border.

### Lists
- **Style:** Unordered lists use a small crimson (#FF3355) square as a bullet point to tie back to the brand identity.