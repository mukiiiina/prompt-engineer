# Example: Linear.app Website Clone Prompt

A high-fidelity website clone prompt for Linear's developer-tool luxury dark-mode landing page. This demonstrates the Website Clone template (Template A) with deep analysis of CSS variables, animation systems, and Swiss typographic discipline.

---

## Generated Prompt

You are a full-stack development engineer specializing in developer-tool luxury aesthetics, dark-mode precision UI, and subtle motion design. Now required to **1:1 pixel-perfect replicate https://linear.app/**, strictly restoring its "deep space black + high-contrast typography + dot-matrix agent animations + Swiss grid discipline" aesthetic, with core implementation of animated dot-grid systems, scroll-driven reveals, and complete page interactions.

---

## 1. Core Visual Style (Strictly Replicate Original Site)

### 1.1 Color System (Unique Palette, No Additional Colors)
- Background base: #08070B (deep space black, NOT pure #000000)
- Elevated surface: #0F0F13 (cards, elevated sections)
- Border/divider: #1C1C21 (subtle separation)
- Text primary: #F7F8F8 (near-white, headings and primary body)
- Text secondary: #8A8F98 (mid-gray, descriptions)
- Text tertiary: #5C5F66 (muted gray, captions, labels)
- Text quaternary: #3C3F44 (very muted, meta info)
- Accent: #5E6AD2 (indigo, CTAs, links, interactive highlights)
- Accent hover: #4F5DBA (indigo darken for hover states)
- Success: #4ADE80 (green, status indicators)
- Error: #F87171 (red, error states)
- Style: Developer-tool luxury, Swiss precision, dark-mode dominant. Reject high saturation, reject gradients on backgrounds, reject decorative flourishes without functional meaning

### 1.2 Typography System (Swiss Discipline + Engineering Precision)
- Display/Hero: Inter, weight 500, size `clamp(3rem, 5vw, 4.5rem)`, letter-spacing -0.02em, line-height 1.1, color #F7F8F8
- H2/Section titles: Inter, weight 500, size `clamp(1.75rem, 3vw, 2.5rem)`, letter-spacing -0.01em, line-height 1.2
- H3/Feature titles: Inter, weight 500, size 1.25rem, letter-spacing -0.01em, line-height 1.3
- Body large: Inter, weight 400, size 1.125rem, line-height 1.6, color #8A8F98
- Body regular: Inter, weight 400, size 0.9375rem, line-height 1.6, color #8A8F98
- Caption/Labels: Inter, weight 400, size 0.8125rem, line-height 1.5, color #5C5F66
- Code/Mono: JetBrains Mono, weight 400, size 0.875rem, letter-spacing 0, color #8A8F98
- Tabular numbers: `font-variant-numeric: tabular-nums` + `font-feature-settings: "ss01"` for data display
- All text uses `text-wrap: balance` and `text-wrap: pretty` for refined line breaks

### 1.3 Visual Elements (Dot-Matrix Agent System as Core)
- **Hero dot-grid animation**: Two distinct 5x5 dot-matrix systems:
  - `"agent"` pattern: 3200ms step animation, diagonal wave propagation across grid coordinates (0-4 indexed), dots animate opacity 0.3 to 1.0
  - `"upDown"` pattern: 2800ms step animation, vertical oscillation, same opacity range
  - Dot size: 3-4px, spacing: 16-20px, color #5E6AD2 (indigo) or #F7F8F8 depending on context
- **Feature illustrations**: Animated dot-matrix representations of workflows (agent loops, sync operations, integrations)
- **Background**: Solid #08070B, NO gradients, NO images, pure color discipline
- **Cards/Containers**: Background #0F0F13, border 1px solid #1C1C21, border-radius 8px
- **CTA Buttons**:
  - Primary: bg #5E6AD2, text #FFFFFF, height 40px, padding 0 16px, border-radius 6px, font-size 0.875rem, weight 500
  - Secondary: bg transparent, border 1px solid #3C3F44, text #F7F8F8, same sizing

### 1.4 Animation Style (Systems Operating, Not Decorative)
- **Dot-grid animations**:
  - Continuous loop, step-timing (NOT smooth easing), conveying "systems operating"
  - Must feel like agent/AI workflows executing, not decorative flourish
- **Scroll reveals**:
  - Sections fade in + translateY(20px to 0) as they enter viewport
  - Duration 600ms, easing `cubic-bezier(0.16, 1, 0.3, 1)`
  - Stagger children by 100ms
- **Hover interactions**:
  - Links: color transition #8A8F98 to #F7F8F8, duration 150ms
  - Buttons: subtle scale(1.02) + brightness increase, duration 200ms
  - Cards: border-color #1C1C21 to #3C3F44, duration 200ms
- **Page transitions**: None (single-page marketing site), instant content switch

## 2. Page Structure (1:1 Complete Long Page)

### 2.1 Navigation (Fixed Top)
- Height: 64px, background rgba(8, 7, 11, 0.8), backdrop-filter blur(12px)
- Left: Linear logo (textmark or icon)
- Center: Nav links (Product, Solutions, Pricing, Company, Blog) -- font-size 0.875rem, weight 500, color #8A8F98
- Right: "Log in" (text link) + "Sign up" (primary button, small)
- Mobile: Hamburger menu, drawer from right

### 2.2 Hero Section
- Padding-top: 160px (desktop), 120px (mobile)
- Content centered, max-width 800px
- Eyebrow text: "LINEAR" (caption style, letter-spacing 0.1em, color #5C5F66)
- Headline: "The issue tracking tool you'll enjoy using" (display size)
- Subheadline: "Linear helps streamline software projects, sprints, tasks, and bug tracking. It's built for high-performance teams." (body large)
- CTA group: "Sign up for free" (primary) + "Talk to sales" (secondary)
- Below CTA: Product screenshot or UI mockup in dark container
- Background: #08070B with subtle dot-grid decoration

### 2.3 Logo Cloud / Social Proof
- "Trusted by forward-thinking companies"
- 5-6 company logos in grayscale, opacity 0.5
- Grid layout, centered, max-width 900px

### 2.4 Feature Grid (Key Capabilities)
- Section title: "Purpose-built for modern product teams"
- 6 feature cards in 3x2 grid (desktop), 2x3 (tablet), 1x6 (mobile)
- Each card:
  - Icon: 24px, color #5E6AD2
  - Title: H3 size, color #F7F8F8
  - Description: body regular, color #8A8F98
  - Animated dot-grid illustration (unique per feature)
- Features: Cycles & Sprints, Issues & Projects, Roadmaps, Insights, Git Integration, Notifications

### 2.5 Product Showcase Sections (Alternating)
- Alternating left-right layout (image + text)
- Images: Product UI screenshots in dark containers with subtle shadow
- Text: Eyebrow (caption) + Title (H2) + Description (body) + Link (accent color)
- 4-5 sections covering: Keyboard-first design, Command line, Git integration, Cycles, Insights

### 2.6 Testimonials / Quotes
- Large quote text: Inter, weight 500, size 1.5rem, color #F7F8F8
- Attribution: name + role + company logo
- Card layout, border 1px solid #1C1C21

### 2.7 Final CTA Section
- Background: slightly elevated #0A0A0F or gradient-free solid
- Headline: "Get started for free"
- Subheadline: "Join thousands of teams building better software"
- CTA: "Sign up" (large primary button, height 48px)
- Secondary: "Talk to sales" (text link)

### 2.8 Footer
- 5 columns: Product, Solutions, Company, Resources, Legal
- Link style: 0.875rem, color #5C5F66, hover #8A8F98
- Bottom row: Logo + copyright + social icons (Twitter, GitHub, Discord)
- Border-top: 1px solid #1C1C21

## 3. Core Interactions & Technical Requirements

### 3.1 Dot-Matrix Animation System (Site Soul)
- Implement 5x5 CSS grid or Canvas grid for dot animations
- `"agent"` pattern: Calculate diagonal wave using grid coordinates (x + y), stagger opacity 0.3->1.0 in 3200ms loops with step-timing
- `"upDown"` pattern: Vertical oscillation based on y-coordinate, 2800ms loops
- Dots must be DOM elements (not just CSS background) for accessibility and potential interaction
- Each feature card has unique dot pattern variation

### 3.2 Scroll-Driven Reveals
- Use Intersection Observer with threshold 0.1
- Elements animate: opacity 0->1, translateY 20px->0
- Duration 600ms, easing `cubic-bezier(0.16, 1, 0.3, 1)`
- Stagger children within sections by 100ms
- Respect `prefers-reduced-motion`: disable animations if user prefers

### 3.3 Responsive Adaptation
- **Desktop (>1280px)**: Full layout, 3-column grids, side-by-side showcases, all animations
- **Laptop (1024-1280px)**: 2-column grids, slightly reduced padding
- **Tablet (768-1024px)**: Single column feature grid, stacked showcases, hamburger nav
- **Mobile (<768px)**: Single column everything, reduced hero padding (80px top), hidden dot-grid decorations, simplified nav drawer
- Touch: Tap to hover states, swipeable nav drawer

## 4. Tech Stack (Precision Replication)

- Frontend: Next.js 14 (App Router) + TypeScript 5.3 + React 18
- Styling: Tailwind CSS (custom config for exact color palette and type scale)
- Animation: Framer Motion (scroll reveals, page transitions) + CSS keyframes (dot-grid loops)
- Fonts: Inter (Google Fonts or self-hosted, weights 400/500) + JetBrains Mono (weight 400)
- Icons: Lucide React (consistent stroke width 1.5px)
- Deployment: Vercel (static export or serverless)
- Backend: Not required for marketing site (static)
- Analytics: Vercel Analytics (optional)

## 5. Must-Replicate Details

1. **Deep space black**: #08070B background, NOT #000000 or #111111
2. **Text hierarchy**: 4 distinct text colors (#F7F8F8 -> #8A8F98 -> #5C5F66 -> #3C3F44), strictly applied
3. **Dot-grid animations**: Step-timing (not smooth), conveying system operations, exact 3200ms/2800ms durations
4. **Swiss typography**: Inter font, tight letter-spacing on headings, `text-wrap: balance`, tabular nums
5. **Border discipline**: All cards use exactly 1px solid #1C1C21, 8px border-radius
6. **No gradients on backgrounds**: Pure solid colors only, gradient-free aesthetic
7. **Developer-tool luxury mood**: Quiet confidence, technical credibility, zero decorative fluff

## 6. Deliverables

- Visual 1:1 replication of Linear's "developer luxury" dark aesthetic
- Interaction 1:1 replication (dot-grid animations, scroll reveals, hover states)
- Clean, maintainable Next.js 14 + TypeScript codebase
- Responsive across all breakpoints (mobile -> 4K desktop)
- 60fps animations, no jank
- Accessible: proper ARIA labels, reduced-motion support, semantic HTML
- Deployable to Vercel with zero config
