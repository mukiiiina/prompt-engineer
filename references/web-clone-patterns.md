# Website Clone Analysis Framework

A systematic approach to decomposing any website into a precise, implementable AI prompt. Use this framework when the user provides a URL, screenshot, or description of an existing website to replicate.

## 1. Visual Identity Extraction

### 1.1 Color System

Extract the complete palette with exact hex values:

- **Background colors**: Page background, section backgrounds, card backgrounds, overlay colors
- **Primary/Brand color**: Main CTA, logo, highlights
- **Text colors**: Headings, body text, captions, disabled text, link colors (default, hover, visited)
- **Border/Divider colors**: Separator lines, card borders, input borders
- **Semantic colors**: Success, error, warning, info states
- **Surface colors**: Elevated surfaces, modals, dropdowns

Document color application rules:
- Which elements use which colors
- Opacity values for overlays, disabled states, placeholders
- Gradient definitions (if any): direction, stops with exact colors and positions

**Anti-pattern declarations**: Explicitly state forbidden colors and effects (e.g., "NO gradients", "NO neon colors", "NO drop shadows on flat design").

### 1.2 Typography System

Identify all font families used:

- **Heading font**: Family, weights used (400/500/700/900), letter-spacing, line-height
- **Body font**: Family, weight, size, line-height, paragraph spacing
- **Mono font**: Code blocks, data displays, terminal text
- **Accent/Display font**: Decorative headings, hero text, special sections

Document the type scale:
- Hero title: `clamp()` or exact sizes with viewport breakpoints
- H1, H2, H3, H4: Exact font-size, weight, line-height, margin-bottom
- Body, Caption, Label: Exact sizes and weights
- Text transformations: uppercase, lowercase, capitalize rules per element type

### 1.3 Spacing System

Define the grid and spacing:

- **Container max-width**: px or rem values for each breakpoint
- **Page padding**: Horizontal and vertical padding at each breakpoint
- **Section spacing**: Gap between major sections (e.g., 120px desktop, 80px mobile)
- **Component gap**: Internal spacing within cards, forms, lists
- **Grid system**: Columns, gutter width, alignment rules

## 2. Layout Architecture

### 2.1 Page Structure

Map the complete page hierarchy:

- **Global elements**: Navbar, footer, floating buttons, modals, cookie banners
- **Section sequence**: Order of sections from top to bottom with IDs/names
- **Full-bleed vs contained**: Which sections span full viewport width vs constrained container
- **Sticky/Fixed elements**: Elements that remain visible during scroll

### 2.2 Component Inventory

List every UI component with its location:

- **Navigation**: Logo, menu items, CTA buttons, mobile hamburger menu
- **Hero section**: Layout type (split, centered, full-bleed), content alignment, media placement
- **Content sections**: Cards, lists, grids, feature showcases, testimonials
- **Forms**: Input fields, labels, validation states, submit buttons
- **Footer**: Columns, links, social icons, copyright, newsletter signup

For each component, specify:
- Exact dimensions or responsive behavior
- Positioning (absolute, relative, fixed) and z-index stacking
- Background treatments (color, image, video, pattern)

### 2.3 Responsive Behavior

Document breakpoint-specific changes:

- **Desktop (>1024px)**: Full layout, all interactions, complete visual effects
- **Tablet (768px-1024px)**: Layout shifts, navigation changes, font size adjustments
- **Mobile (<768px)**: Stacked layout, simplified interactions, hidden elements, hamburger menu
- **Touch adaptations**: Hover-to-tap conversions, swipe gestures, touch targets (min 44px)

## 3. Interaction & Animation Taxonomy

### 3.1 Micro-interactions

Catalog every interactive element:

- **Buttons**: Default, hover, active, focus, disabled states with exact style changes (color, scale, shadow, border)
- **Links**: Underline behavior, color transition, visited state
- **Inputs**: Focus ring, label animation, validation icons, error shake
- **Cards**: Hover lift, shadow change, border highlight, content reveal
- **Icons**: Rotation, scale, color fill on interaction

Specify exact timing for each transition:
- Duration in milliseconds (e.g., `transition: all 0.3s ease-out`)
- Easing function (ease, ease-out, cubic-bezier values)
- Transform properties (translateY, scale, rotate)

### 3.2 Scroll-Driven Effects

Document scroll-based animations:

- **Parallax layers**: Which elements move at different speeds, speed ratios
- **Reveal animations**: Fade-in, slide-up, scale-in triggers and thresholds
- **Sticky behavior**: Elements that pin during scroll, release points
- **Progress indicators**: Scroll bars, section counters, reading progress
- **Video/Animation playback**: Scroll-linked playhead control

### 3.3 Page Transitions

Define navigation transitions:

- **Route changes**: Fade, slide, wipe between pages
- **Modal/Drawer open**: Backdrop fade, panel slide, timing
- **Loading states**: Skeleton screens, spinners, progress bars

## 4. Asset Specification

### 4.1 Images

For each image:
- Dimensions (width x height) or aspect ratio
- Object-fit behavior (cover, contain, fill)
- Lazy loading strategy
- Placeholder/skeleton treatment
- Hover effects (zoom, grayscale, overlay)

### 4.2 Icons

- Icon library (Lucide, FontAwesome, Heroicons, custom SVG)
- Icon size scale (16px, 20px, 24px, 32px)
- Stroke width for outlined icons
- Color inheritance rules

### 4.3 Media

- Video: Autoplay, loop, muted, controls, poster image
- Audio: Trigger conditions, player UI
- 3D Models: Format (GLB/GLTF), lighting, camera position, interaction model
- Lottie/JSON animations: Trigger conditions, loop behavior

## 5. Technical Implementation Notes

### 5.1 Critical Implementation Details

Identify elements that make or break the clone's fidelity:

- Custom cursors
- Noise/grain textures
- Blend modes (multiply, screen, overlay)
- Clip-path or mask shapes
- CSS Houdini / Paint API usage
- WebGL/Canvas effects
- SVG animations

### 5.2 Performance Requirements

Specify targets:
- First Contentful Paint (FCP) target
- Largest Contentful Paint (LCP) target
- Animation frame rate (60fps minimum)
- Bundle size limits
- Image optimization requirements (WebP, responsive srcset)

## 6. Output Structure

When generating the final prompt, organize as:

1. **Role & Objective** - AI persona and 1:1 clone mandate
2. **Visual Style** - Color system, typography, spacing (exact values)
3. **Layout & Components** - Section-by-section breakdown with positioning
4. **Animations & Interactions** - State changes, scroll effects, transitions (exact timing/easing)
5. **Technical Stack** - Frameworks, libraries, fonts, deployment
6. **Asset List** - Required images, icons, media with specifications
7. **Responsive Strategy** - Breakpoint-specific behavior
8. **Deliverables** - File structure, component list, deployment steps
9. **Must-Have Details** - Critical fidelity checkpoints

## Screenshot Analysis Checklist

When analyzing a screenshot without URL access:

- [ ] Identify the overall layout pattern (F-pattern, Z-pattern, grid, split-screen)
- [ ] Count distinct colors and determine the primary palette
- [ ] Identify font types (serif, sans-serif, mono, display) and approximate hierarchy
- [ ] Map the grid structure (columns, alignment, spacing rhythm)
- [ ] Locate all interactive elements and hypothesize their hover/active states
- [ ] Identify animation hints (parallax indicators, transition clues, motion blur)
- [ ] Note any unusual or custom UI components
- [ ] Determine the likely tech stack based on visual complexity (3D = Three.js, heavy animations = GSAP, etc.)
