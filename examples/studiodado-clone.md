# Example: Studio DADO Website Clone Prompt

A high-fidelity website clone prompt for Studio DADO's minimalist editorial interior design portfolio. This demonstrates the Website Clone template (Template A) with focus on gallery-like photography presentation, editorial typography, and warm human-centered aesthetics.

---

## Generated Prompt

You are a full-stack development engineer specializing in editorial minimalist aesthetics, gallery-like photography presentation, and warm human-centered design. Now required to **1:1 pixel-perfect replicate https://www.studiodado.com/**, strictly restoring its "monochrome minimalism + full-bleed photography + editorial typography + Form Follows Feeling philosophy" aesthetic, with core implementation of immersive image grids, smooth hover reveals, and sophisticated scroll-driven storytelling.

---

## 1. Core Visual Style (Strictly Replicate Original Site)

### 1.1 Color System (Restrained Palette, Photo-Driven)
- Background base: #FFFFFF (pure white, letting photography breathe)
- Secondary background: #EEEEEE (very light gray, subtle section separation)
- Text primary: #313131 (warm dark gray, NOT pure black)
- Text secondary: #666666 (medium gray, captions and metadata)
- Text muted: #999999 (light gray, labels and dividers)
- Accent: #32373C (dark charcoal, buttons and CTAs)
- Button text: #FFFFFF (white on dark buttons)
- Divider: #313131 at 15% opacity, or decorative "* * *" asterisk separators
- Style: Editorial minimalism, gallery-white, photo-first. Reject bright colors, reject gradients on backgrounds, reject heavy UI chrome. Let photography be the color.

### 1.2 Typography System (Editorial, Human, Refined)
- Display/Hero: Custom or premium sans-serif (Neue Haas Grotesk, Söhne, or Inter as fallback), weight 400, size `clamp(2.5rem, 5vw, 4rem)`, letter-spacing -0.02em, line-height 1.15, color #313131
- H2/Section titles: Same family, weight 400, size `clamp(1.5rem, 3vw, 2.25rem)`, letter-spacing -0.01em, line-height 1.2
- H3/Project titles: Weight 400, size 1.5rem, line-height 1.3
- Body large: Weight 400, size 1.125rem (18px), line-height 1.7, color #313131
- Body regular: Weight 400, size 1rem (16px), line-height 1.6, color #666666
- Caption/Meta: Weight 400, size 0.875rem (14px), line-height 1.5, color #999999
- Nav links: Weight 400, size 1rem, letter-spacing 0.02em, uppercase optional
- All text uses refined editorial spacing, generous line-height, generous paragraph margins

### 1.3 Visual Elements (Photography as Hero)
- **Project thumbnails**: Full-bleed photography, aspect-ratio 3:2 or 16:10, object-fit cover
- **Hover treatment on images**: Subtle scale(1.03) + brightness(1.02) transition, 600ms, ease-out. NO heavy overlays, NO darkening gradients
- **Image captions**: Below image, small text (14px), project name + category
- **Decorative dividers**: Three asterisks "* * *" centered, color #999999, used between major sections
- **Arrow icons**: Simple "→" or thin SVG arrow for CTAs, not button-heavy
- **Buttons**: Pill-shaped, `border-radius: 9999px`, bg #32373C, text white, padding `calc(0.667em + 2px) calc(1.333em + 2px)`, font-size 1.125em. Hover: slight opacity reduction
- **Background discipline**: Predominantly white. Sections alternate white and #EEEEEE sparingly

### 1.4 Animation Style (Quiet Confidence, Editorial Pace)
- **Image reveals**: Fade in + subtle translateY(20px to 0) as images enter viewport, duration 800ms, easing `cubic-bezier(0.25, 0.1, 0.25, 1)`
- **Text reveals**: Staggered fade-in for headlines and body text, 100ms stagger, 600ms duration
- **Hover on project cards**: Image scale(1.03), title color shifts to slightly darker, 400ms ease
- **Nav menu overlay**: Full-screen white overlay, slides in from right or fades in, links appear with stagger
- **Page transitions**: None (single-page portfolio), content loads instantly
- **Scroll behavior**: Smooth scrolling enabled, gentle parallax on hero images (optional, subtle)

## 2. Page Structure (1:1 Complete Long Page)

### 2.1 Navigation (Fixed or Static Top)
- Height: ~80px, background transparent over hero, becomes white on scroll (optional)
- Left: Logo "Studio DADO" in refined sans-serif, weight 400, tracking slightly tight
- Right: Hamburger menu icon (3 horizontal lines, minimal) OR text links (Work, Studio, Journal, Contact)
- Mobile: Hamburger only, opens full-screen overlay menu

### 2.2 Hero Section
- Full viewport height (100vh) OR generous padding-top (~120px)
- Large hero image: Full-bleed architectural interior photography, warm lighting, lived-in space
- Overlaid text (if any): Centered or bottom-left, "Interior design for hospitality" — small uppercase eyebrow + large headline
- Text style: Eyebrow 12px uppercase tracking 0.15em, Headline `clamp(2rem, 4vw, 3.5rem)` weight 400
- NO dark overlay on image — text should be placed on naturally light areas of photo, or use subtle text-shadow

### 2.3 About Teaser / Introduction
- Background: #FFFFFF
- Padding: 120px vertical (desktop), 80px (mobile)
- Content: Large body text (20-22px) centered or left-aligned, max-width 720px
- Text: "We create innovative interior design experiences that prioritize human connection and emotional resonance."
- CTA: "Approach →" text link, not button, color #313131, hover underline

### 2.4 Philosophy Section — "Form Follows Feeling"
- Background: #EEEEEE (very light gray, subtle break from white)
- Padding: 160px vertical
- Headline: "Form Follows Feeling" — centered, large display size, weight 400
- Body: Two paragraphs explaining the philosophy, max-width 640px, centered
- Key quote: "Empathy shapes everything we create, from the first impression to the final detail."
- Decorative "* * *" divider above or below

### 2.5 Featured Projects Grid
- Background: #FFFFFF
- Section label: "Selected Work" or similar, small uppercase, tracking 0.1em, color #999999
- Grid: 2 columns (desktop), 1 column (mobile), gap 24px
- Each project card:
  - Image: Full-width within column, aspect-ratio 3:2, object-fit cover
  - Title below: Project name, 18px, weight 400, color #313131
  - Category: "Hospitality / Residential" etc, 14px, color #999999
  - Hover: Image scale(1.03), 400ms
- 4-6 projects visible
- Projects: Hospitality interiors, residential spaces, commercial environments (use placeholder images with warm architectural photography)

### 2.6 Blog / Journal Section
- Background: #FFFFFF or #EEEEEE
- Section label: "Latest from the Journal"
- 3 article cards in row (desktop), stacked (mobile)
- Each card:
  - Image: 16:10 aspect ratio
  - Title: 20px, weight 400
  - Date/Category: 14px, #999999
  - Excerpt: 2 lines, 16px, #666666
- CTA: "View all articles →" text link

### 2.7 Studio Section
- Background: #FFFFFF
- Two-column layout (desktop): Image left (studio team or process shot), text right
- Text: "Studio DADO" heading + paragraph about the studio's approach and team
- Image: Warm, candid team photo or studio environment
- CTA: "Learn more about us →"

### 2.8 Footer CTA
- Background: #FFFFFF
- Large centered text: "Work together?" — display size, friendly and inviting
- Subtext: "We'd love to hear about your project."
- CTA: Pill button "Get in touch" or text link "Contact us →"

### 2.9 Footer
- Background: #FFFFFF
- Top border: 1px solid rgba(49,49,49,0.1)
- Padding: 80px vertical
- Content:
  - Left: Address (Miami, FL), email, phone
  - Center: Sitemap links (Work, Studio, Journal, Contact, Privacy)
  - Right: Social links (Instagram, LinkedIn, Pinterest) + Newsletter signup
- Bottom: Copyright "© 2026 Studio DADO. All rights reserved."
- All footer text: 14px, color #999999, hover #313131

## 3. Core Interactions & Technical Requirements

### 3.1 Image Loading & Reveal
- Use `loading="lazy"` for below-fold images
- Implement Intersection Observer for fade-in reveal
- Images fade from opacity 0 to 1 + translateY(20px to 0), 800ms, ease-out
- Preload hero image for LCP optimization

### 3.2 Project Card Hover
- CSS transform: scale(1.03) on image container
- Overflow hidden on container to clip scaled image
- Transition: 400ms cubic-bezier(0.25, 0.1, 0.25, 1)
- Title color: subtle darkening on hover

### 3.3 Mobile Menu Overlay
- Full-screen white overlay
- Menu links: Large (32px), centered vertically, stagger fade-in
- Close button: Top-right, X icon
- Scroll lock when menu open

### 3.4 Responsive Adaptation
- **Desktop (>1024px)**: Full layout, 2-column project grid, side-by-side studio section
- **Tablet (768-1024px)**: Single column projects, reduced padding (80px sections)
- **Mobile (<768px)**: Single column everything, hamburger nav, full-bleed images, 60px section padding
- Touch: Tap to navigate, swipe gallery if applicable

## 4. Tech Stack (Editorial Precision)

- Frontend: Next.js 14 (App Router) + TypeScript + React 18
- Styling: Tailwind CSS (custom config for exact editorial spacing)
- Animation: Framer Motion (scroll reveals, staggered text), CSS transitions (hover states)
- Fonts: Self-hosted premium sans-serif (Neue Haas Grotesk or Söhne) OR Inter as high-quality fallback
- Images: Next.js Image component with priority loading for hero, lazy for rest
- CMS: Sanity or Contentful (for projects, blog posts, studio info)
- Deployment: Vercel (edge-optimized image delivery)
- Analytics: Minimal, privacy-focused (optional Plausible)

## 5. Must-Replicate Details

1. **White space generosity**: Sections need ample vertical padding (120-160px desktop). Never cramped.
2. **Photo-first hierarchy**: Images must dominate. Text is secondary, elegant, unobtrusive.
3. **Warm dark gray text**: #313131, NOT pure #000000. Critical for the warm editorial feel.
4. **Pill buttons only**: All CTAs use border-radius 9999px. NO sharp-cornered buttons.
5. **Asterisk dividers**: "* * *" between major sections, centered, color #999999.
6. **Typography refinement**: Generous line-height (1.6-1.7), comfortable paragraph width (max 640px for body)
7. **Gallery hover**: Subtle image scale on project cards. NO overlays, NO text-on-image tricks.

## 6. Deliverables

- Visual 1:1 replication of Studio DADO's editorial minimalism
- Interaction 1:1 replication (image reveals, hover scales, menu overlay)
- Clean, maintainable Next.js 14 + TypeScript codebase
- Responsive across all breakpoints
- Optimized image loading (WebP, responsive srcset, lazy loading)
- Accessible: semantic HTML, alt text for all images, reduced-motion support
- Deployable to Vercel with zero config
