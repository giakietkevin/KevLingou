---
name: Zen Study
colors:
  surface: '#fcf9f8'
  surface-dim: '#dcd9d9'
  surface-bright: '#fcf9f8'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#f6f3f2'
  surface-container: '#f0eded'
  surface-container-high: '#eae7e7'
  surface-container-highest: '#e4e2e1'
  on-surface: '#1b1c1c'
  on-surface-variant: '#444840'
  inverse-surface: '#303030'
  inverse-on-surface: '#f3f0f0'
  outline: '#74786f'
  outline-variant: '#c4c8bd'
  surface-tint: '#516447'
  primary: '#45573b'
  on-primary: '#ffffff'
  primary-container: '#5d7052'
  on-primary-container: '#ddf3cd'
  inverse-primary: '#b8cda9'
  secondary: '#5f5e5b'
  on-secondary: '#ffffff'
  secondary-container: '#e1dfda'
  on-secondary-container: '#63635f'
  tertiary: '#6b4858'
  on-tertiary: '#ffffff'
  tertiary-container: '#856070'
  on-tertiary-container: '#ffe6ee'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#d4e9c4'
  primary-fixed-dim: '#b8cda9'
  on-primary-fixed: '#0f1f09'
  on-primary-fixed-variant: '#3a4c30'
  secondary-fixed: '#e4e2dd'
  secondary-fixed-dim: '#c8c6c2'
  on-secondary-fixed: '#1b1c19'
  on-secondary-fixed-variant: '#474743'
  tertiary-fixed: '#ffd8e7'
  tertiary-fixed-dim: '#e7bacc'
  on-tertiary-fixed: '#2d1320'
  on-tertiary-fixed-variant: '#5e3d4c'
  background: '#fcf9f8'
  on-background: '#1b1c1c'
  surface-variant: '#e4e2e1'
typography:
  display-lg:
    fontFamily: Geist
    fontSize: 48px
    fontWeight: '600'
    lineHeight: '1.2'
    letterSpacing: -0.02em
  display-lg-mobile:
    fontFamily: Geist
    fontSize: 32px
    fontWeight: '600'
    lineHeight: '1.2'
  headline-md:
    fontFamily: Geist
    fontSize: 24px
    fontWeight: '500'
    lineHeight: '1.4'
  body-lg:
    fontFamily: Geist
    fontSize: 18px
    fontWeight: '400'
    lineHeight: '1.6'
  body-md:
    fontFamily: Geist
    fontSize: 16px
    fontWeight: '400'
    lineHeight: '1.6'
  japanese-display:
    fontFamily: Noto Sans JP
    fontSize: 64px
    fontWeight: '500'
    lineHeight: '1.2'
  label-sm:
    fontFamily: Geist
    fontSize: 12px
    fontWeight: '600'
    lineHeight: '1'
    letterSpacing: 0.05em
rounded:
  sm: 0.25rem
  DEFAULT: 0.5rem
  md: 0.75rem
  lg: 1rem
  xl: 1.5rem
  full: 9999px
spacing:
  unit: 8px
  container-max: 1120px
  gutter: 24px
  margin-desktop: 64px
  margin-mobile: 20px
---

## Brand & Style

This design system centers on the Japanese concept of *Ma* (negative space), creating a digital environment that reduces cognitive load for language learners. The brand personality is calm, intentional, and scholarly yet accessible. 

The design style is **Minimalist** with a focus on tactile refinement. It avoids the frantic gamification typical of learning apps, instead opting for a "digital zendo" atmosphere. High whitespace, deliberate typography, and a restricted color palette ensure the student remains focused on the curriculum. Visual interest is generated through subtle transitions and perfect alignment rather than decorative elements.

## Colors

The palette is rooted in organic, earthy tones that mimic high-quality stationery and natural materials.

- **Primary (Matcha):** Used exclusively for progress indicators, primary actions, and "correct" states. It represents growth and focus.
- **Secondary (Washi):** A warm, textured off-white used for cards and containers to separate them from the base background without harsh contrast.
- **Neutral (Charcoal):** Used for primary text to ensure high legibility while being softer on the eyes than pure black.
- **Background (Stone):** A very light, warm gray that provides a grounding foundation for the entire UI.
- **Functional Colors:** Use a muted terracotta (#B86B5D) for errors/incorrect answers to maintain the calm aesthetic even during mistakes.

## Typography

Typography is the primary vehicle for the design's hierarchy. **Geist** provides a technical, precise feel for the UI, while **Noto Sans JP** is used for Japanese characters to ensure maximum clarity across all stroke weights.

Japanese characters should always be rendered 15-20% larger than accompanying English text to compensate for visual density. Use generous line height (1.6+) for body text to allow "breathable" reading sessions. Key vocabulary words should use the `japanese-display` role to emphasize stroke order and detail.

## Layout & Spacing

The design system employs a **fixed grid** on desktop to maintain a sense of a structured "page," switching to a fluid model on mobile. 

The spacing rhythm is based on an 8px base unit. Emphasize wide outer margins to pull the user's eye toward the center of the screen. Layouts should favor verticality and single-column structures for lesson content to prevent distraction. For the "Streak Heatmap," use a tight 4px grid to visualize consistency over time, mirroring the density of a traditional physical calendar.

## Elevation & Depth

Depth is achieved through **tonal layers** rather than heavy shadows. The base layer is the Stone background; interactive cards sit atop this using the Washi (Secondary) color.

- **Level 1 (Surface):** Default state. Use a subtle 1px border (#E2E2E2) instead of a shadow.
- **Level 2 (Active/Hover):** Apply an ambient, extra-diffused shadow (0px 4px 20px rgba(0,0,0,0.04)) to suggest the element is lifted.
- **Level 3 (Modal/Focus):** A semi-transparent overlay with a light backdrop blur (4px) to keep the context visible while isolating the task.

## Shapes

The shape language uses **Rounded** (Level 2) corners to soften the technical precision of the typography. This creates a friendly, approachable feel that reduces the "intimidation factor" of learning a new language. 

- **Cards & Inputs:** 0.5rem (8px) radius.
- **Primary Buttons:** 1rem (16px) radius to distinguish them as high-intent interaction points.
- **Progress Bars:** Fully rounded (pill-shaped) to represent a continuous, smooth journey.

## Components

### Buttons
Primary buttons use the Matcha Green background with white text. Secondary buttons are "Ghost" style—clear backgrounds with a 1px Charcoal border. All buttons should have a subtle 200ms transition on hover, shifting the background color slightly deeper.

### Cards (Study Tiles)
Cards are the primary container for vocabulary. They use the Washi background color. In "Quiz Mode," cards should have a distinct focus state where the border changes to Matcha Green.

### Streak Heatmap
A GitHub-inspired 52-week grid. Empty days are a light gray (#EAEAEA). Active days scale from a pale Matcha to a deep Forest green based on the intensity of study (XP/Time).

### Input Fields
Inputs should be minimalist: a single bottom border that thickens and turns Matcha Green when focused. This mimics writing on a lined notebook.

### Progress Indicators
Thin, horizontal bars at the top of the viewport. The track is a light gray, and the progress fill is Matcha Green. Avoid "percentage numbers" unless necessary; focus on the visual movement of the bar.