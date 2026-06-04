---
name: Lumina Synth
colors:
  surface: '#0c1324'
  surface-dim: '#0c1324'
  surface-bright: '#33394c'
  surface-container-lowest: '#070d1f'
  surface-container-low: '#151b2d'
  surface-container: '#191f31'
  surface-container-high: '#23293c'
  surface-container-highest: '#2e3447'
  on-surface: '#dce1fb'
  on-surface-variant: '#bbc9cd'
  inverse-surface: '#dce1fb'
  inverse-on-surface: '#2a3043'
  outline: '#859397'
  outline-variant: '#3c494c'
  surface-tint: '#2fd9f4'
  primary: '#8aebff'
  on-primary: '#00363e'
  primary-container: '#22d3ee'
  on-primary-container: '#005763'
  inverse-primary: '#006877'
  secondary: '#ddb8ff'
  on-secondary: '#490081'
  secondary-container: '#62259b'
  on-secondary-container: '#d1a1ff'
  tertiary: '#ffd0e3'
  on-tertiary: '#620040'
  tertiary-container: '#ffa6cf'
  on-tertiary-container: '#8f1e62'
  error: '#ffb4ab'
  on-error: '#690005'
  error-container: '#93000a'
  on-error-container: '#ffdad6'
  primary-fixed: '#a2eeff'
  primary-fixed-dim: '#2fd9f4'
  on-primary-fixed: '#001f25'
  on-primary-fixed-variant: '#004e5a'
  secondary-fixed: '#f0dbff'
  secondary-fixed-dim: '#ddb8ff'
  on-secondary-fixed: '#2c0051'
  on-secondary-fixed-variant: '#62259b'
  tertiary-fixed: '#ffd8e7'
  tertiary-fixed-dim: '#ffafd3'
  on-tertiary-fixed: '#3d0026'
  on-tertiary-fixed-variant: '#85145a'
  background: '#0c1324'
  on-background: '#dce1fb'
  surface-variant: '#2e3447'
typography:
  display-score:
    fontFamily: JetBrains Mono
    fontSize: 48px
    fontWeight: '800'
    lineHeight: 48px
    letterSpacing: -0.02em
  headline-lg:
    fontFamily: Sora
    fontSize: 32px
    fontWeight: '700'
    lineHeight: 40px
  headline-md:
    fontFamily: Sora
    fontSize: 24px
    fontWeight: '600'
    lineHeight: 32px
  body-lg:
    fontFamily: Sora
    fontSize: 18px
    fontWeight: '400'
    lineHeight: 28px
  body-md:
    fontFamily: Sora
    fontSize: 16px
    fontWeight: '400'
    lineHeight: 24px
  data-label:
    fontFamily: JetBrains Mono
    fontSize: 14px
    fontWeight: '500'
    lineHeight: 20px
    letterSpacing: 0.05em
  data-value:
    fontFamily: JetBrains Mono
    fontSize: 14px
    fontWeight: '700'
    lineHeight: 20px
  headline-lg-mobile:
    fontFamily: Sora
    fontSize: 24px
    fontWeight: '700'
    lineHeight: 32px
rounded:
  sm: 0.125rem
  DEFAULT: 0.25rem
  md: 0.375rem
  lg: 0.5rem
  xl: 0.75rem
  full: 9999px
spacing:
  playfield-margin: 1rem
  gutter: 1rem
  unit: 4px
  component-padding-x: 1.5rem
  component-padding-y: 0.75rem
---

## Brand & Style

The design system for this browser game is built on a **Retro-Futuristic / Vaporwave** aesthetic, filtered through a modern, high-performance lens. The target audience consists of competitive gamers and enthusiasts of the "synthwave" subculture who value speed, precision, and immersive visuals. 

The UI should evoke a sense of high-energy momentum and "digital physicalness," where every element feels like it is powered by an internal light source. By mixing **Glassmorphism** with **High-Contrast Bold** elements, the interface achieves maximum legibility against the chaotic motion of gameplay while maintaining a cohesive, atmospheric depth.

## Colors

The palette is anchored by **Obsidian (#020617)** to provide an infinite-depth backdrop, ensuring that the neon accents achieve maximum luminous efficacy. 

- **Cyber Cyan (#22d3ee)**: Used for primary actions, player status, and "safe" interactive zones.
- **Electric Purple (#c084fc)**: Used for secondary UI elements, level indicators, and progression tracking.
- **Neon Pink (#f472b6)**: Reserved for high-alert items, power-ups, and critical game state changes.

All colors should be implemented with corresponding "glow" variants (20% opacity fills and outer glows) to simulate light emission.

## Typography

The typography strategy employs a dual-font approach to distinguish between navigation and data. 

**Sora** provides a high-tech, geometric feel for all standard UI elements, buttons, and instructional text. Its wide apertures ensure readability even at small sizes against dark backgrounds. 

**JetBrains Mono** is utilized for all "readout" data, such as scores, timers, and technical stats. This monospaced choice reinforces the "coded" futuristic theme and ensures that shifting numerical values do not cause visual "jitter" in the layout.

## Layout & Spacing

This design system utilizes a **Fixed Grid** approach for HUD elements to ensure player muscle memory, while the central playfield remains fluid. 

The spacing rhythm is tight, based on a **4px scale**, to minimize the footprint of the UI and maximize the active gameplay area. 
- **Desktop**: A 12-column layout with 16px gutters, primarily used for menus and post-game screens.
- **Mobile**: A simplified overlay system with 16px safe-area margins.
- **HUD**: Elements are pinned to the corners of the viewport with a consistent 24px inset from the screen edge.

## Elevation & Depth

Depth is conveyed through **Glassmorphism** and **Light Emission** rather than traditional shadows. 

1.  **Background**: Solid #020617.
2.  **Surface Tier**: Semi-transparent panels (10% white or primary color) with a 12px backdrop blur.
3.  **Border Tier**: 1px solid borders using the primary or secondary color at 40% opacity.
4.  **Active Tier**: Elements that are "on" or "active" utilize an outer glow (`box-shadow: 0 0 15px [color]`) and a 100% opaque border.

This creates a "layered glass" effect where the UI feels like it's floating above the game world.

## Shapes

The shape language is **Soft (0.25rem)**. While the overall vibe is "sharp," purely square corners are avoided to prevent a dated "8-bit" look. A subtle radius on panels and buttons gives the light-emitting edges a more polished, modern-technical feel. 

Large containers like game cards or the main HUD wrapper should use `rounded-lg` (0.5rem) to differentiate them from smaller interactive components.

## Components

- **Buttons**: Rendered as ghost buttons with a 1px primary color border. On hover, the button fills with a 20% primary color tint and gains a neon outer glow.
- **Chips/Badges**: Small, solid-fill containers with JetBrains Mono text. Used for status effects or "New Record" indicators.
- **Input Fields**: Dark backgrounds (#0f172a) with a bottom-only 2px border in Cyber Cyan.
- **Progress Bars**: High-contrast fills with a "pulse" animation. The track is a low-opacity version of the fill color.
- **Cards**: Minimalist glass panels with a backdrop-filter blur and a subtle top-left gradient highlight to simulate a light source from above.
- **Score HUD**: A transparent container with a thick, high-contrast border on the left side only, featuring large Display-Score typography.