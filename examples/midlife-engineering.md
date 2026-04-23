# Example: Midlife Engineering Website Clone Prompt

This example demonstrates a high-fidelity website clone prompt for an industrial minimalist music device showcase. Use this as a reference for the depth, specificity, and structure expected in generated prompts.

---

## Generated Prompt

You are a full-stack development engineer specializing in industrial minimalist tech aesthetics, 3D product showcases, high-interaction UI, and animations. Now required to **1:1 pixel-perfect replicate https://www.midlife.engineering/**, strictly restore its "matte black device model + minimalist UI + orange accents + oversized bold background text + skeuomorphic interaction" industrial aesthetic. Core implementation includes 3D device model, knob/button interactions, scroll parallax, complete page, and full animation chain.

---

## 1. Core Visual Style (Strictly Replicate Original Site Industrial Minimalist Texture)

### 1.1 Color System (Unique Palette, No Additional Colors)
- Background base: #F0F0F0 (light gray matte, simulating industrial paper/device background)
- Primary device color: #1A1A1A (matte black, no reflection, device casing)
- Accent color: #FF6633 (bright orange, ONLY for indicator lights, logo dots, interaction feedback)
- Text color: #1A1A1A (pure black, titles/body), #FFFFFF (pure white, device screen text)
- Auxiliary colors: Various grays (#333 to #CCC), used for buttons, knobs, scales, simulating matte texture
- Style: Industrial minimalist, skeuomorphic, matte no reflection. Reject high saturation, reject gradients, use only light/shadow to express dimensionality

### 1.2 Typography System (Original Site Soul, Oversized Bold + Device UI Hierarchy)
- Background oversized title: Ultra-bold sans-serif (Helvetica Black / Monument Grotesk), weight 900, size `clamp(8rem, 20vw, 15rem)`, ALL CAPS, light gray semi-transparent, as background layer, partial letters obscured by device
- Device screen text: Monospace sans-serif (JetBrains Mono), weight 400, size 12px, pure white, displaying system status
- Device button text: Minimalist sans-serif, weight 500, size 10-12px, black/white, changes with button grayscale
- Description text: Sans-serif (Inter), weight 300, size 14px, lightweight, e.g., `Made for focus, rest, and everything in between.`
- All text strictly aligned to device UI grid, forming industrial device sense of order

### 1.3 Visual Elements (Device Model as Core)
- Core device: **Midlife Engineering music device 3D model**, matte black casing, includes:
  - Top-left: speaker grille (dot texture), camera/indicator light, `AUTOPLAY` button
  - Center: LCD screen (displaying system status text), 4 knobs (with orange indicator lights)
  - Keyboard area: number keys 1-0, `BAR` key, `BEATS` key, gray gradient drum pads, `RECORD SESSION` button
  - Bottom: function icon buttons (Twitter, Instagram, cloud, moon, etc.)
  - Right side: `Site of the Day` badge, vertical `midlife engineering` text, orange logo dot
- Background decorations:
  - Top-left: orange circular logo dot
  - Top-right: description text
  - Bottom-left: `& make harmony` text
  - Bottom-right: copyright `2026 made by 1042 Studio`
- Layout:
  - Full-screen light gray background, oversized background title
  - Center: device model (60% screen, centered)
  - Periphery: description text, logo, copyright info

### 1.4 Animation Style (Skeuomorphic, Restrained, Realistic)
- Device interaction (core):
  - Mouse hover knob: slight rotation (15deg), orange indicator brightens
  - Mouse hover button: slight depression (2px), simulating press effect, text brightens
  - Screen text: typewriter animation, character-by-character system status display
  - Device slight levitation: following mouse movement, device produces slight displacement/rotation, simulating 3D hover sensation
- Scroll parallax:
  - On scroll, device model slowly displaces/scales, background title fades in/out with scroll
  - Page modules fade in sequentially with scroll, maintaining industrial minimalist continuity
- Page transitions:
  - Fade in/out animation, no-refresh switching, device model maintains continuous interaction

## 2. Page Structure (1:1 Replicate Original Site Complete Long Page)

### 2.1 Homepage (Hero Section, Core Visual)
- Background: light gray + oversized light gray semi-transparent background title (`midlife engineering`)
- Central device model: Midlife Engineering music device, complete UI interaction
- Text elements:
  - Top-right: `Made for focus, rest, and everything in between.`
  - Bottom-left: `& make harmony`
  - Bottom-right: `2026 made by 1042 Studio`
- Top-left: orange circular logo dot
- Top-right: three-dot menu button

### 2.2 Complete Scrolling Page (All Modules Replicated)
- **Product Introduction Module**: device feature descriptions, industrial typography, with product detail images
- **Feature Module**: Autoplay, Record Session, Beats/Tracks feature introductions, with interactive demos
- **Technical Specifications Module**: device specs, interfaces, system info, monospace typography
- **User Reviews/Featured Module**: Product Hunt badge, user feedback
- **Purchase/Contact Module**: purchase buttons, contact form, minimalist industrial UI

## 3. Core Interactions & Technical Requirements (Must All Be Implemented)

### 3.1 Device Model & Skeuomorphic Interaction (Original Site Soul Function)
- Render device 3D model with Three.js / React Three Fiber, matte black texture, no reflection
- Listen to mouse events:
  - hover knob: slight rotation, indicator brightens
  - hover button: depression effect, simulating press
  - hover screen: typewriter text animation, character-by-character display
- Mouse movement: device slight displacement/rotation, simulating 3D hover sensation
- Device button click: trigger sound (optional), UI feedback (depression + text change)

### 3.2 Scroll Parallax & Page Interaction
- Listen to `scroll` event, implement device model/background title parallax displacement
- Page modules fade in with scroll, smooth transitions
- Navigation menu click: expand full-screen menu, industrial design

### 3.3 Responsive Adaptation
- PC: full-screen immersive, device model complete display, clear interaction
- Mobile: device model adaptive shrink, UI interaction simplified, background title hidden, text auto-scales
- Touch devices: support touch tap/swipe, trigger device interaction

## 4. Tech Stack (Precision Replication Specialized)

- Frontend: React + TypeScript + Vite
- 3D Rendering: Three.js / React Three Fiber (device model, interaction)
- Styling: Tailwind CSS (precision control of industrial colors, typography, spacing)
- Animation: Framer Motion / GSAP (parallax, device interaction, typewriter effect)
- Fonts: Helvetica Black (background title) + JetBrains Mono (device screen text) + Inter (description text)
- Deployment: Vercel / Netlify (static deployment, optimized 3D model loading)
- Backend: Node.js + Express (lightweight API, handling product/contact data)
- Database: MySQL 8.0 (storing user feedback, form data)

## 5. Must-Replicate Details (Determine 1:1 Replication Texture)

1. **Device Model**: matte black texture, button/knob/screen/grille details, must 1:1 replicate
2. **Background Title**: oversized bold semi-transparent text, partially obscured by device, typography consistent with original site
3. **Color System**: light gray background + matte black device + orange accent, no other extraneous colors
4. **Interaction Animation**: knob/button hover effects, screen typewriter, device levitation, fully match original site
5. **Typography Text**: description text, copyright info, device UI text, position/font/content must replicate
6. **Complete Page**: must replicate full long page from homepage to Footer, not just homepage

## 6. Deliverables

- Visual 1:1 replication of original site industrial minimalist skeuomorphic texture
- Interaction 1:1 replication of original site (device model interaction, scroll parallax, page transitions)
- Clean, maintainable, directly deployable code
- Responsive perfect adaptation for PC/mobile/touch devices
- 3D device rendering smooth, no lag/frame drops
- Full functionality available (navigation, interaction, forms)
- Complete replication of https://www.midlife.engineering/ full website, including all scrolling modules
