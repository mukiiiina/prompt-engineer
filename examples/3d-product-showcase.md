# Example: 3D Sneaker Configurator Prompt

A 3D interactive product showcase prompt demonstrating the 3D / Interactive Experience template (Template C).

---

## Generated Prompt

You are a creative developer specializing in 3D web experiences and interactive product configurators.

## 1. Concept & Mood

- **Experience Type**: Product Configurator (e-commerce)
- **Visual Mood**: Futuristic, premium, athletic energy
- **Reference Sites**: Nike By You (customization), Apple Product Pages (scroll-driven reveals)
- **Core Metaphor**: The user is a sneaker designer in a futuristic studio — rotating, customizing, and previewing their creation in real-time

## 2. 3D Elements

### 2.1 Scene Composition
- **Camera**: Perspective, FOV 45deg, initial position [3, 2, 5] looking at [0, 0, 0]
- **Lighting**:
  - Ambient: #FFFFFF, intensity 0.4
  - Key light (Directional): #FFF5E6, position [5, 10, 7], intensity 1.2, castShadow true, shadow-mapSize 2048x2048
  - Rim light (Spot): #4F8CFF, position [-5, 5, -5], intensity 0.8, angle 0.5, penumbra 0.5
  - Fill light (Point): #FFE4C4, position [0, 2, 5], intensity 0.3
- **Environment**: Studio HDRI (neutral gray), tone mapping ACESFilmic, exposure 1.0
- **Background**: Radial gradient CSS (#F8F9FA to #E9ECEF), subtle noise texture overlay (opacity 0.03)

### 2.2 Meshes & Materials
- **Primary Model**: High-poly sneaker GLB (~50K tris), separated into customizable parts:
  - Upper mesh (color customizable)
  - Midsole mesh (color customizable)
  - Outsole mesh (color customizable)
  - Laces mesh (color customizable)
  - Logo/Swoosh mesh (color customizable)
  - Eyelets mesh (metallic, fixed silver)
- **Material style**: PBR, roughness 0.6 (fabric upper), 0.3 (rubber sole), 0.1 (metallic accents)
- **Secondary elements**:
  - Rotating platform: Cylinder, radius 2.5, height 0.2, material #FFFFFF with subtle grid texture
  - Floating particles: 50 small spheres, slow vertical drift, random positions

### 2.3 Particle Systems
- **Type**: Dust motes / micro-fibers
- **Count**: 100
- **Behavior**: Cylindrical emitter (radius 4, height 6), slow upward drift (0.001 units/frame), random horizontal sway
- **Interaction**: Mouse repel (radius 1.5, force 0.02)
- **Material**: Semi-transparent white, size 0.02, additive blending

## 3. Interactions

- **Mouse hover mesh part**: Highlight with emissive glow (emissive #FFFFFF, intensity 0.3), show tooltip with part name
- **Mouse drag**: Orbit camera around product (damping 0.05, maxPolarAngle Math.PI / 2)
- **Mouse wheel**: Zoom in/out (min distance 2, max distance 10, smooth damping)
- **Scroll**: Camera zooms closer to product, particles intensify, UI panels slide in from edges
- **Click color swatch**: Animate color transition on corresponding mesh part (duration 400ms, easing easeInOutCubic)
- **Double-click**: Reset camera to default position (animated, duration 800ms)

## 4. Animation Timeline

- **Entry sequence** (0-3s):
  - 0.0s: Platform rises from below (translateY -5 to 0, duration 1.2s, easeOutBack)
  - 0.3s: Sneaker fades in (opacity 0 to 1, duration 0.8s) + scales up (0.8 to 1.0, duration 1.0s, easeOutElastic)
  - 0.6s: Lights turn on sequentially (intensity 0 to target, stagger 0.2s)
  - 1.5s: Particles spawn and begin drift
  - 2.0s: UI panels slide in (sidebar from left, color picker from right)

- **Idle animations** (looping):
  - Sneaker: Gentle float (translateY ±0.1, duration 4s, sine wave)
  - Platform: Slow rotation (0.1deg/frame)
  - Particles: Continuous drift

- **Color change transition**:
  - Mesh flash white (emissive #FFFFFF, intensity 0.5, duration 100ms)
  - Color interpolate to new value (duration 300ms)
  - Emissive fade out (duration 200ms)

## 5. UI Design

### 5.1 Color Picker Panel (Right Side)
- Width: 320px desktop, full-width drawer mobile
- Background: rgba(255,255,255,0.9), backdrop-blur 12px
- Sections:
  - **Part selector**: Horizontal scrollable chips (Upper, Midsole, Outsole, Laces, Logo)
  - **Color grid**: 6x4 swatches, selected state = ring + checkmark
  - **Custom picker**: Native color input with hex display
  - **Presets**: "Classic", "Neon", "Monochrome" one-click themes

### 5.2 Product Info Panel (Left Side)
- Width: 280px desktop, collapsible mobile
- Content:
  - Product name: "Air Velocity X1" (48px, weight 800)
  - Price: "$189.00" (32px, weight 600, color #0F172A)
  - Description: Lightweight performance runner with customizable colorways
  - Specs list: Weight, Drop, Cushioning level
  - CTA button: "Add to Cart" (full-width, height 56px, bg #0F172A, hover scale 1.02)

### 5.3 View Controls (Bottom Center)
- Icon buttons: 360 rotate, Auto-spin toggle, Reset view, AR view (placeholder)
- Style: Circular buttons, 48px, bg rgba(255,255,255,0.8), icon color #334155

## 6. Tech Stack

- 3D Engine: React Three Fiber (v8) + Three.js (r160)
- Helpers: @react-three/drei (Environment, ContactShadows, Html overlays)
- Animation: GSAP (entry timeline), @react-three/fiber useFrame (idle loops)
- Post-processing: @react-three/postprocessing (Bloom, Vignette, SMAA)
- State: Zustand (color config, selected part, camera state)
- Build tool: Vite 5 + TypeScript
- Styling: Tailwind CSS

## 7. Performance Budget

- Target FPS: 60 (desktop), 30 (mobile)
- Max draw calls: 200
- Texture resolution: 2048x2048 max, compressed with Basis Universal
- GLB file: <10MB total, Draco compressed
- Initial load: <3s on 4G
- Lazy load: Post-processing effects after initial render
- Use instanced mesh for particles
- LOD: Simplified mesh (<15K tris) for mobile

## 8. Responsive Behavior

- **Desktop (>1024px)**: Full 3D view, side panels visible, all interactions
- **Tablet (768-1024px)**: Panels collapsible to floating buttons, pinch-to-zoom enabled
- **Mobile (<768px)**: Bottom sheet for color picker, swipe to rotate, tap to select part, AR button hidden

## 9. Asset List

- `sneaker.glb` - Main product model (separated meshes)
- `studio.hdr` - Environment map
- `noise.png` - Background texture (512x512, tileable)
- `particle.png` - Soft circle sprite for particles
- `fonts/` - Inter font files (weights 400, 600, 800)

## 10. Deliverables

- Complete React + TypeScript source code
- Component structure: Scene, Model, ColorPicker, ProductInfo, ViewControls
- Custom hooks: useProductColors, useCameraAnimation, useParticleSystem
- Responsive layout with mobile-first approach
- Loading state with progress indicator
- Error boundary for 3D context loss
- Deployable to Vercel with static export
