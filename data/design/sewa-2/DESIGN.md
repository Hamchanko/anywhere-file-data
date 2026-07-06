---
name: Global Community Design System
colors:
  surface: '#fcf9f8'
  surface-dim: '#dcd9d9'
  surface-bright: '#fcf9f8'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#f6f3f2'
  surface-container: '#f0eded'
  surface-container-high: '#eae7e7'
  surface-container-highest: '#e5e2e1'
  on-surface: '#1b1b1c'
  on-surface-variant: '#434655'
  inverse-surface: '#303030'
  inverse-on-surface: '#f3f0ef'
  outline: '#737686'
  outline-variant: '#c3c5d7'
  surface-tint: '#0451de'
  primary: '#004ed9'
  on-primary: '#ffffff'
  primary-container: '#3269f5'
  on-primary-container: '#fdfaff'
  inverse-primary: '#b5c4ff'
  secondary: '#725c00'
  on-secondary: '#ffffff'
  secondary-container: '#ffd746'
  on-secondary-container: '#735d00'
  tertiary: '#5a5c5c'
  on-tertiary: '#ffffff'
  tertiary-container: '#737474'
  on-tertiary-container: '#fbfbfb'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#dbe1ff'
  primary-fixed-dim: '#b5c4ff'
  on-primary-fixed: '#00164d'
  on-primary-fixed-variant: '#003cac'
  secondary-fixed: '#ffe07e'
  secondary-fixed-dim: '#e9c332'
  on-secondary-fixed: '#231b00'
  on-secondary-fixed-variant: '#564500'
  tertiary-fixed: '#e2e2e2'
  tertiary-fixed-dim: '#c6c6c7'
  on-tertiary-fixed: '#1a1c1c'
  on-tertiary-fixed-variant: '#454747'
  background: '#fcf9f8'
  on-background: '#1b1b1c'
  surface-variant: '#e5e2e1'
  surface-subtle: '#F6F6F6'
  link-blue: '#3269F5'
  accent-yellow: '#FFD746'
  text-main: '#1F1F1F'
  white: '#FFFFFF'
typography:
  display-lg:
    fontFamily: Plus Jakarta Sans
    fontSize: 48px
    fontWeight: '700'
    lineHeight: '1.1'
    letterSpacing: -0.02em
  headline-lg:
    fontFamily: Plus Jakarta Sans
    fontSize: 32px
    fontWeight: '700'
    lineHeight: '1.2'
  headline-lg-mobile:
    fontFamily: Plus Jakarta Sans
    fontSize: 28px
    fontWeight: '700'
    lineHeight: '1.2'
  headline-md:
    fontFamily: Plus Jakarta Sans
    fontSize: 24px
    fontWeight: '600'
    lineHeight: '1.3'
  body-lg:
    fontFamily: Be Vietnam Pro
    fontSize: 18px
    fontWeight: '400'
    lineHeight: '1.6'
  body-md:
    fontFamily: Be Vietnam Pro
    fontSize: 16px
    fontWeight: '400'
    lineHeight: '1.6'
  body-sm:
    fontFamily: Be Vietnam Pro
    fontSize: 14px
    fontWeight: '400'
    lineHeight: '1.5'
  label-lg:
    fontFamily: Be Vietnam Pro
    fontSize: 14px
    fontWeight: '600'
    lineHeight: '1.2'
  label-md:
    fontFamily: Be Vietnam Pro
    fontSize: 12px
    fontWeight: '500'
    lineHeight: '1.2'
rounded:
  sm: 0.25rem
  DEFAULT: 0.5rem
  md: 0.75rem
  lg: 1rem
  xl: 1.5rem
  full: 9999px
spacing:
  base: 8px
  container-max: 1200px
  gutter: 24px
  margin-desktop: 40px
  margin-mobile: 20px
  stack-xs: 4px
  stack-sm: 8px
  stack-md: 16px
  stack-lg: 32px
  stack-xl: 64px
---

## Brand & Style

The brand personality is rooted in warmth, hospitality, and the bridging of cultures. It is designed to evoke feelings of optimism, trust, and inclusivity, catering to a global community where communication is the primary bridge. The visual language balances a professional foundation with a friendly, human-centric touch.

This design system follows a **Corporate / Modern** style infused with **Humanist** elements. It prioritizes clarity and accessibility while using vibrant color accents and generous whitespace to create an inviting atmosphere. The design avoids cold industrialism, opting instead for soft geometry and high-legibility layouts that facilitate cross-generational and cross-cultural interaction.

## Colors

The palette is built on a foundation of trust and energy. 

- **Primary Blue (#3269F5):** Represents reliability and global connectivity. It is the primary color for interactive elements and brand signaling.
- **Secondary Yellow (#FFD746):** Provides a warm, sunny accent that signals hospitality and community energy. It is used sparingly for highlights, secondary actions, and badges.
- **Neutrals:** The system uses a deep charcoal (#1F1F1F) for high-contrast typography and a very light gray (#F6F6F6) for surface separation, ensuring the UI feels airy and clean.

The default color mode is **light**, emphasizing a "clean slate" feel that supports readability for users of all ages.

## Typography

The typography system uses a pairing of two contemporary sans-serifs to achieve a balance of character and utility.

- **Headlines (Plus Jakarta Sans):** Chosen for its soft, rounded terminals and modern geometric construction. It feels welcoming and optimistic in large formats.
- **Body & Labels (Be Vietnam Pro):** A highly legible, professional typeface that maintains a friendly tone. It excels in long-form text and UI labels, providing a warm but functional reading experience.

The scaling logic prioritizes comfortable line heights (1.5x - 1.6x for body text) to ensure content remains accessible to a diverse, global audience.

## Layout & Spacing

This design system utilizes a **Fixed Grid** approach for desktop environments to maintain a curated, editorial feel, while transitioning to a **Fluid Grid** for mobile devices.

### Grid & Breakpoints
- **Desktop (1200px+):** A 12-column grid with a 1200px max-width container. 24px gutters provide ample breathing room between content blocks.
- **Tablet (768px - 1199px):** An 8-column fluid grid with 20px gutters.
- **Mobile (< 767px):** A 4-column fluid grid. Margins are reduced to 20px to maximize screen real estate.

The spacing rhythm is built on an **8px base unit**, ensuring consistent vertical and horizontal rhythm across all components and layout containers.

## Elevation & Depth

Depth in this design system is created through **Tonal Layers** and **Ambient Shadows** to maintain a soft, approachable feel.

- **Tonal Layers:** The background uses the neutral tertiary color (#F6F6F6), while primary content containers use white (#FFFFFF). This creates a natural hierarchy without relying on heavy borders.
- **Shadows:** Use extremely soft, low-opacity shadows (e.g., `box-shadow: 0 4px 20px rgba(31, 31, 31, 0.05)`). Shadows should feel like a subtle lift rather than a hard drop.
- **Interactive States:** On hover, elements should slightly increase their shadow spread or shift background color to a lighter tint of the primary color, reinforcing the tactile nature of the UI.

## Shapes

The shape language is consistently **Rounded**, reinforcing the friendly and community-focused brand personality. 

- **Standard Elements (Buttons, Inputs):** 0.5rem (8px) corner radius.
- **Large Containers (Cards, Modals):** 1rem (16px) corner radius.
- **Special Elements (Chips, Search Bars):** Use the full `rounded-xl` (1.5rem / 24px) or pill-shaped rounding to differentiate them from structural content blocks.

Avoid sharp 0px corners, as they conflict with the welcoming narrative of the design system.

## Components

### Buttons
- **Primary:** Filled with Primary Blue (#3269F5), White text. 8px radius. Bold, clear weight.
- **Secondary:** Filled with Secondary Yellow (#FFD746), Dark Gray text. Use for supportive actions like "Save" or "Share."
- **Ghost:** Transparent background with Primary Blue text and border.

### Cards
Cards are the primary vehicle for community content. They should feature a white background, the "Soft" 16px corner radius, and a subtle ambient shadow. Padding should be generous (24px or 32px) to ensure a premium feel.

### Input Fields
Inputs use a light gray border (#E0E0E0) that shifts to Primary Blue on focus. Labels should always be visible above the field using the `label-lg` typography style.

### Chips & Badges
Used for user interests or language levels. These should be pill-shaped with light background tints (e.g., 10% opacity of the Primary Blue) and dark text.

### Community Lists
Use generous vertical spacing (stack-md) and subtle horizontal dividers in #F6F6F6 to separate user profiles or conversation threads.