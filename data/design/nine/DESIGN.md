---

name: Crystalline Portal

colors:

  surface: '#f9f9f9'

  surface-dim: '#dadada'

  surface-bright: '#f9f9f9'

  surface-container-lowest: '#ffffff'

  surface-container-low: '#f3f3f4'

  surface-container: '#eeeeee'

  surface-container-high: '#e8e8e8'

  surface-container-highest: '#e2e2e2'

  on-surface: '#1a1c1c'

  on-surface-variant: '#424750'

  inverse-surface: '#2f3131'

  inverse-on-surface: '#f0f1f1'

  outline: '#737781'

  outline-variant: '#c3c6d2'

  surface-tint: '#2e5fa0'

  primary: '#002c5a'

  on-primary: '#ffffff'

  primary-container: '#004282'

  on-primary-container: '#84b0f7'

  inverse-primary: '#a8c8ff'

  secondary: '#426276'

  on-secondary: '#ffffff'

  secondary-container: '#c6e7ff'

  on-secondary-container: '#48687c'

  tertiary: '#262e33'

  on-tertiary: '#ffffff'

  tertiary-container: '#3c4449'

  on-tertiary-container: '#a8b1b7'

  error: '#ba1a1a'

  on-error: '#ffffff'

  error-container: '#ffdad6'

  on-error-container: '#93000a'

  primary-fixed: '#d5e3ff'

  primary-fixed-dim: '#a8c8ff'

  on-primary-fixed: '#001b3c'

  on-primary-fixed-variant: '#0a4687'

  secondary-fixed: '#c6e7ff'

  secondary-fixed-dim: '#aacbe2'

  on-secondary-fixed: '#001e2d'

  on-secondary-fixed-variant: '#2a4a5d'

  tertiary-fixed: '#dbe4ea'

  tertiary-fixed-dim: '#bfc8ce'

  on-tertiary-fixed: '#151d22'

  on-tertiary-fixed-variant: '#40484d'

  background: '#f9f9f9'

  on-background: '#1a1c1c'

  surface-variant: '#e2e2e2'

  deep-ocean: '#002D5A'

  crystal-blue: '#E3F2FD'

  soft-border: '#D1E9FF'

typography:

  display-lg:

    fontFamily: Oswald

    fontSize: 80px

    fontWeight: '700'

    lineHeight: '1.1'

    letterSpacing: 0.05em

  headline-lg:

    fontFamily: Oswald

    fontSize: 48px

    fontWeight: '600'

    lineHeight: '1.2'

    letterSpacing: 0.02em

  headline-md:

    fontFamily: Oswald

    fontSize: 32px

    fontWeight: '500'

    lineHeight: '1.3'

  headline-sm:

    fontFamily: Oswald

    fontSize: 24px

    fontWeight: '500'

    lineHeight: '1.4'

  body-lg:

    fontFamily: Noto Serif

    fontSize: 18px

    fontWeight: '400'

    lineHeight: '1.7'

  body-md:

    fontFamily: Noto Serif

    fontSize: 16px

    fontWeight: '400'

    lineHeight: '1.6'

  label-lg:

    fontFamily: Plus Jakarta Sans

    fontSize: 14px

    fontWeight: '600'

    lineHeight: '1.2'

  label-sm:

    fontFamily: Plus Jakarta Sans

    fontSize: 12px

    fontWeight: '700'

    lineHeight: '1.2'

  display-lg-mobile:

    fontFamily: Oswald

    fontSize: 48px

    fontWeight: '700'

    lineHeight: '1.1'

  headline-lg-mobile:

    fontFamily: Oswald

    fontSize: 32px

    fontWeight: '600'

    lineHeight: '1.2'

spacing:

  container-max: 1200px

  gutter: 24px

  margin-x: 40px

  section-gap: 120px

  element-gap: 16px

  grid-unit: 8px

---

## Brand & Style

This design system is built upon the "Crystalline Airy" aesthetic, evoking a sense of lightness, transparency, and refined elegance. It moves away from traditional heavy gaming UI, instead adopting a style that feels like high-end editorial meets modern web application.

The visual narrative is driven by:

- **High-Key Composition:** Dominantly light and bright backgrounds to create an "airy" atmosphere.

- **Geometric Precision:** Utilizing diamond and checkered patterns as a signature structural motif.

- **Ethereal Transparency:** Soft glassmorphism and subtle gradients that mimic the refraction of light through crystal.

- **Sophisticated Professionalism:** A balance of sharp lines and spacious layouts that cater to a discerning audience.

The style is a hybrid of **Minimalism** and **Glassmorphism**, emphasizing clean whitespace and translucent layers without sacrificing structural clarity.

## Colors

The palette is centered on a "Crystalline Blue" spectrum, moving from pure white to deep, authoritative navy.

- **Primary:** A professional deep blue `#004282`) used for interactive elements and brand accents.

- **Surface & Backgrounds:** The UI relies on `#FFFFFF` and `#F0F8FF` (Alice Blue) to maintain a bright, high-key look.

- **Crystalline Accents:** `#E3F2FD` is used for large background areas and subtle gradients to provide depth without adding visual weight.

- **Interaction States:** Use `deep-ocean` for high-contrast text and active states, while `secondary` blue is reserved for softer supportive elements like tags or decorative patterns.

## Typography

Typography in this design system creates a contrast between structural modernism and literary elegance.

- **Headlines (Oswald):** Used for section titles and primary headers. The condensed, tall nature of Oswald provides a sharp, energetic feel that mirrors the crystalline theme.

- **Body Text (Noto Serif):** Brings a refined, editorial quality. Serifs are used for better readability in long-form descriptions and to add a layer of sophistication.

- **Labels & UI (Plus Jakarta Sans):** A clean sans-serif ensures that functional elements (buttons, navigation, metadata) remain legible and modern.

**Styling Note:** Large display headlines should often use low-opacity outlines or very light blue tints to act as "watermark" backgrounds behind content.

## Layout & Spacing

The layout philosophy emphasizes **Airiness** and **Horizontal Rhythm**.

- **Grid System:** A 12-column fixed grid for desktop `1200px` max-width) transitioning to a fluid 4-column grid for mobile.

- **Sectioning:** Large vertical gaps `120px+`) are encouraged between major sections to allow the background patterns to breathe.

- **Diamond Pattern Overlay:** Use a repeating 45-degree diamond/checkerboard pattern (using `#B0D1E8` at 10-15% opacity) as a background for headers and transitional sections.

- **Alignment:** Content is generally center-aligned to create a focused, portal-like experience.

## Elevation & Depth

This design system avoids heavy shadows in favor of **Tonal Layering** and **Glassmorphism**.

- **Surfaces:** Use high-transparency white surfaces `rgba(255, 255, 255, 0.8)`) with a `10px` backdrop-blur for cards and navigation bars.

- **Outlines:** Instead of shadows, use 1px solid borders in `soft-border` `#D1E9FF`) to define container boundaries.

- **Depth through Patterns:** Depth is communicated by layering text and images over the diamond background patterns, creating a sense of "etched glass" rather than "stacked paper."

- **Active State:** On hover, increase the opacity of the glass surface or add a very subtle glow using the primary color.

## Shapes

The shape language is strictly **Sharp and Geometric**. 

- **Corners:** 0px radius is the default for buttons, card containers, and input fields to maintain a precise, crystalline aesthetic. 

- **Diamond Accents:** UI elements such as bullet points, "Play" icons, and decorative dividers should utilize the 45-degree rotated square (diamond) shape.

- **Dividers:** Horizontal lines should be thin (1px) and may feature a small diamond in the center.

## Components

### Buttons

- **Primary:** Solid `#004282` with white `label-lg` text. Sharp corners.

- **Secondary:** Ghost style. 1px `#004282` border, transparent background, `#004282` text.

- **Hover State:** Subtle color shift to `#002D5A` or a light blue background fill for ghost buttons.

### Cards

- **News/Media Cards:** Sharp-edged containers with a 1px `soft-border`. Utilize a vertical layout with the image on top and a white background for the text area.

- **Character Cards:** High-transparency glassmorphism background with a vertical orientation and sharp edges.

### Inputs & Form Elements

- **Text Fields:** White background with a 1px `#B0D1E8` border. Sharp corners. Label text uses `label-sm` in primary blue.

- **Checkboxes:** Square, sharp-edged. When checked, use the primary blue with a white checkmark.

### Navigation

- **Header:** Transparent background with `backdrop-blur`. Use the diamond pattern as a subtle border-bottom or overlay.

- **Links:** `label-lg` typography. Active links should have a small diamond icon appearing below or beside them.

### Additional Elements

- **Video Play Buttons:** A white circular or diamond-shaped container with a primary blue play icon, featuring a soft crystalline glow on hover.

- **Section Headers:** Combine a large "Watermark" display text (Oswald, very low opacity) with a smaller, high-contrast headline on top.