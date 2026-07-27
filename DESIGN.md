---
name: Instrument Index Portfolio
colors:
  surface: '#f4f5f4'
  surface-dim: '#d6dad6'
  surface-bright: '#f8f9f8'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#eef0ee'
  surface-container: '#e9ebe9'
  surface-container-high: '#e4e7e4'
  surface-container-highest: '#dde1dd'
  on-surface: '#1b1c1a'
  on-surface-variant: '#444748'
  inverse-surface: '#30312e'
  inverse-on-surface: '#f2f0ec'
  outline: '#6e746e'
  outline-variant: '#c9cec9'
  surface-tint: '#5f5e5e'
  primary: '#0b0c0c'
  on-primary: '#ffffff'
  primary-container: '#222222'
  on-primary-container: '#8a8989'
  inverse-primary: '#c8c6c5'
  secondary: '#1f6f4f'
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
  background: '#f4f5f4'
  on-background: '#1b1c1a'
  surface-variant: '#dde1dd'
typography:
  display:
    fontFamily: Bricolage Grotesque
    fontSize: 64px
    fontWeight: '400'
    lineHeight: '1.1'
    letterSpacing: -0.02em
  headline-lg:
    fontFamily: Bricolage Grotesque
    fontSize: 40px
    fontWeight: '400'
    lineHeight: '1.2'
  headline-lg-mobile:
    fontFamily: Bricolage Grotesque
    fontSize: 32px
    fontWeight: '400'
    lineHeight: '1.2'
  headline-md:
    fontFamily: Bricolage Grotesque
    fontSize: 28px
    fontWeight: '400'
    lineHeight: '1.3'
  body-lg:
    fontFamily: Archivo
    fontSize: 18px
    fontWeight: '400'
    lineHeight: '1.6'
  body-md:
    fontFamily: Archivo
    fontSize: 16px
    fontWeight: '400'
    lineHeight: '1.6'
  label-caps:
    fontFamily: JetBrains Mono
    fontSize: 12px
    fontWeight: '600'
    lineHeight: '1.0'
    letterSpacing: 0.1em
  caption:
    fontFamily: Archivo
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
The design system is an **instrument index**: the visual language of statistical graphics, lab notation, and engineering drawing, applied to a quantitative builder's portfolio. It deliberately refuses the warm-cream ground, display-serif headline, and tracked-mono label arrangement that this category (and most generated portfolio UI) defaults to.

The aesthetic is **precise, contemporary, and technical** — confident grotesk display, cool neutral grounds, plotted dot-grid texture, and a single signal green that carries live state. The emotional response should be competence and clarity, not literary calm.

## Colors
The palette reads as instrument neutrals plus one signal.

- **Ground (Cool Neutral):** `#f4f5f4` — a faintly green-grey white. Cooler and more precise than the warm ivory it replaced.
- **Ink (Graphite):** `#0b0c0c` for primary type; `#444748` for secondary text.
- **Signal (Deep Green):** `#1f6f4f` is the one accent and it must do real work — scroll progress, active navigation, live/hover state on work rows, and the availability marker. It is never decorative.
- **Panels & Rules:** layered cool greys (`#eef0ee` → `#dde1dd`) with `#c9cec9` 1px rules for the drawn, drafted feel.

## Typography
A three-register grotesk system, chosen against the training-data defaults (EB Garamond, Plus Jakarta Sans, IBM Plex, Space Grotesk and friends are deliberately not used).

- **Display — `Bricolage Grotesque` (700):** oversized and tightly tracked (-0.045em at 82px). Carries all headlines. It has enough character to be recognizable without ornament.
- **Text — `Archivo` (400/500):** a sturdy, quiet workhorse for body copy at 16–18px / 1.65.
- **Data & Notation — `JetBrains Mono` (400/500):** every metadata pair, section number, tag, date, and button label. Monospace is the *data register* here, not a costume — it marks anything that behaves like a value.
- **Hierarchy:** size and weight do the work; generous space above headings signals new chapters.

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
- **Soft Shadows:** If shadows are necessary for cards, use "Ambient Shadows"—extremely low opacity (`0.03 - 0.05`), very large blur radius, and a tint of the signal green or graphite.
- **Outlines:** Prefer 1px borders over shadows for most components to maintain the "Editorial/Drafting" aesthetic.

## Shapes
The shape language is **Sharp (0)**. 

To maintain the architectural and editorial feel of a printed page, use 0px border-radii for all primary containers, buttons, and images. This reinforces the grid and creates a sense of precision. Circular elements should only be used for specific functional items like "Play" buttons or "Scroll to Top" indicators to provide a singular point of visual contrast.

## Components
- **Buttons:** Rectangular, no radius. Primary buttons use a charcoal fill with ivory text. Secondary buttons use a 1px charcoal border with a transparent background. Hover states shift to the signal green or fill with graphite or a slight background tint change.
- **Cards:** Defined by 1px borders or simple whitespace. Images within cards should have no rounding. Titles for cards use the display grotesk.
- **Input Fields:** Bottom-border only (underlined style) to mimic a physical form. Labels should be small, all-caps, positioned above the field.
- **Chips/Labels:** Small, rectangular boxes with 1px borders. Use for tags or categories.
- **Section Numbers:** Use small monospace `label-caps` numbers (e.g., *01/*) placed in the left margin or above section titles to reinforce the editorial structure.
- **Dividers:** Horizontal or vertical 1px lines (`#c9cec9`). Never use heavy shadows to separate content.