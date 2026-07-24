---
name: Paper & Grid Portfolio
colors:
  surface: '#fbf9f5'
  surface-dim: '#dbdad6'
  surface-bright: '#fbf9f5'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#f5f3ef'
  surface-container: '#efeeea'
  surface-container-high: '#eae8e4'
  surface-container-highest: '#e4e2de'
  on-surface: '#1b1c1a'
  on-surface-variant: '#444748'
  inverse-surface: '#30312e'
  inverse-on-surface: '#f2f0ec'
  outline: '#747878'
  outline-variant: '#c4c7c7'
  surface-tint: '#5f5e5e'
  primary: '#0b0c0c'
  on-primary: '#ffffff'
  primary-container: '#222222'
  on-primary-container: '#8a8989'
  inverse-primary: '#c8c6c5'
  secondary: '#526255'
  on-secondary: '#ffffff'
  secondary-container: '#d2e4d4'
  on-secondary-container: '#566759'
  tertiary: '#040e07'
  on-tertiary: '#ffffff'
  tertiary-container: '#19251c'
  on-tertiary-container: '#7f8d81'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#e5e2e1'
  primary-fixed-dim: '#c8c6c5'
  on-primary-fixed: '#1b1c1c'
  on-primary-fixed-variant: '#474746'
  secondary-fixed: '#d5e7d6'
  secondary-fixed-dim: '#b9cbbb'
  on-secondary-fixed: '#101f15'
  on-secondary-fixed-variant: '#3b4b3e'
  tertiary-fixed: '#d8e6d9'
  tertiary-fixed-dim: '#bccabd'
  on-tertiary-fixed: '#121e16'
  on-tertiary-fixed-variant: '#3d4a40'
  background: '#fbf9f5'
  on-background: '#1b1c1a'
  surface-variant: '#e4e2de'
typography:
  display:
    fontFamily: EB Garamond
    fontSize: 64px
    fontWeight: '400'
    lineHeight: '1.1'
    letterSpacing: -0.02em
  headline-lg:
    fontFamily: EB Garamond
    fontSize: 40px
    fontWeight: '400'
    lineHeight: '1.2'
  headline-lg-mobile:
    fontFamily: EB Garamond
    fontSize: 32px
    fontWeight: '400'
    lineHeight: '1.2'
  headline-md:
    fontFamily: EB Garamond
    fontSize: 28px
    fontWeight: '400'
    lineHeight: '1.3'
  body-lg:
    fontFamily: Plus Jakarta Sans
    fontSize: 18px
    fontWeight: '400'
    lineHeight: '1.6'
  body-md:
    fontFamily: Plus Jakarta Sans
    fontSize: 16px
    fontWeight: '400'
    lineHeight: '1.6'
  label-caps:
    fontFamily: Plus Jakarta Sans
    fontSize: 12px
    fontWeight: '600'
    lineHeight: '1.0'
    letterSpacing: 0.1em
  caption:
    fontFamily: Plus Jakarta Sans
    fontSize: 13px
    fontWeight: '400'
    lineHeight: '1.4'
spacing:
  unit: 8px
  container-max: 1280px
  gutter: 24px
  margin-desktop: 64px
  margin-mobile: 20px
  border-thin: 1px
---

## Brand & Style
The design system is rooted in the philosophy of Japanese editorial minimalism, emphasizing intentionality, quietude, and the tactile quality of physical paper. It is designed for a premium personal portfolio that values content over decoration.

The aesthetic blends **Modern Minimalism** with **Tactile/Skeuomorphic** nuances. It avoids digital "perfection" in favor of organic warmth, utilizing subtle textures and a layout reminiscent of high-end independent magazines like *Kinfolk*. The emotional response should be one of calm, professional authority, and timelessness.

## Colors
The palette is inspired by natural materials: rice paper, charcoal, and botanical greens.

- **Background (Ivory/Rice Paper):** Use `#F8F6F2` as the base for all primary surfaces to create a warm, organic feel compared to pure white.
- **Text (Charcoal):** Use `#222222` for all primary communication to ensure high contrast while remaining softer than pure black.
- **Accents (Sage & Forest):** Muted Sage (`#6B7C6E`) is used for subtle highlights or active states. Deep Forest (`#3E4B41`) is reserved for grounding elements or secondary buttons.
- **Functional Neutrals:** Soft Gray and Warm Beige are used for dividers, borders, and secondary backgrounds to maintain the "paper-on-paper" layered effect.

## Typography
The typography system relies on a high-contrast pairing between a graceful, classical serif and a contemporary, approachable sans-serif.

- **Headlines:** `EB Garamond` provides an authoritative, literary feel. Use it for all major headings and display text. It should feel airy and expansive.
- **Body Copy:** `Plus Jakarta Sans` offers exceptional legibility. Its slightly rounded forms prevent the design from feeling too sterile or rigid.
- **Editorial Details:** Use `label-caps` for section numbering (e.g., 01, 02), margin notes, and metadata labels. This creates the "editorial" aesthetic.
- **Hierarchy:** Ensure generous vertical rhythm. Headings should have significant whitespace above them to signal the start of new "chapters."

## Layout & Spacing
This design system utilizes a **Fixed Grid** model for desktop, transitioning to a fluid container for mobile. 

- **The Grid:** A 12-column grid with 24px gutters. Elements should align strictly to these columns.
- **Fine Dividers:** Use 1px charcoal or gray lines to separate sections, mimicking the printed lines of a ledger or high-end stationery.
- **Margins:** Large outer margins (`64px` on desktop) are essential to create the "gallery" feel.
- **Asymmetry:** Encourage the use of empty columns to create a sense of breath and focus. Avoid "filling" the screen; let the ivory background be a structural element.

## Elevation & Depth
Depth in this design system is achieved through physical metaphors rather than digital light sources.

- **Tonal Layering:** Use slightly darker beige or gray backgrounds to indicate container depth.
- **Subtle Texture:** Apply a very fine, low-opacity paper grain SVG overlay to the entire UI to reduce "digital flatness."
- **Soft Shadows:** If shadows are necessary for cards, use "Ambient Shadows"—extremely low opacity (`0.03 - 0.05`), very large blur radius, and a tint of the secondary green or charcoal.
- **Outlines:** Prefer 1px borders over shadows for most components to maintain the "Editorial/Drafting" aesthetic.

## Shapes
The shape language is **Sharp (0)**. 

To maintain the architectural and editorial feel of a printed page, use 0px border-radii for all primary containers, buttons, and images. This reinforces the grid and creates a sense of precision. Circular elements should only be used for specific functional items like "Play" buttons or "Scroll to Top" indicators to provide a singular point of visual contrast.

## Components
- **Buttons:** Rectangular, no radius. Primary buttons use a charcoal fill with ivory text. Secondary buttons use a 1px charcoal border with a transparent background. Hover states should involve a subtle shift to Sage Green or a slight background tint change.
- **Cards:** Defined by 1px borders or simple whitespace. Images within cards should have no rounding. Titles for cards should use the Serif typeface.
- **Input Fields:** Bottom-border only (underlined style) to mimic a physical form. Labels should be small, all-caps, positioned above the field.
- **Chips/Labels:** Small, rectangular boxes with 1px borders. Use for tags or categories.
- **Section Numbers:** Use small `label-caps` serif numbers (e.g., *01/*) placed in the left margin or above section titles to reinforce the editorial structure.
- **Dividers:** Horizontal or vertical 1px lines (`#D1D1D1`). Never use heavy shadows to separate content.