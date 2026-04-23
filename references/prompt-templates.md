# Prompt Templates by Scenario

Ready-to-adapt templates for generating production-ready AI prompts. Select the template matching the user's scenario and fill in the bracketed sections with extracted requirements.

## Template A: Website Clone / Replication

Use when the user wants to 1:1 replicate an existing website from a URL or screenshot.

```markdown
You are a [design_style] full-stack development engineer, now required to **1:1 pixel-perfect replicate [TARGET_URL]**,
strictly restoring its "[KEY_VISUAL_CHARACTERISTIC_1] + [KEY_VISUAL_CHARACTERISTIC_2] + [KEY_VISUAL_CHARACTERISTIC_3]"
aesthetic, with core implementation of [CORE_FEATURE_1], [CORE_FEATURE_2], [CORE_FEATURE_3], and complete page animations.

---

## 1. Core Visual Style (Strictly Replicate Original Site)

### 1.1 Color System (Unique Palette, No Additional Colors)
- Background base: #[HEX] ([Description])
- Primary device/surface color: #[HEX] ([Description])
- Accent color: #[HEX] ([Description], usage restrictions)
- Text color: #[HEX] ([Context]), #[HEX] ([Context])
- Auxiliary colors: Grayscale range from #[HEX] to #[HEX], used for [ELEMENTS]
- Style: [DESIGN_STYLE_KEYWORDS], reject [FORBIDDEN_STYLES]

### 1.2 Typography System
- Background oversized title: [FONT_FAMILY], weight [WEIGHT], size `clamp([MIN], [PREFERRED], [MAX])`, [TRANSFORM], [COLOR/OPACITY], z-layer behavior
- Device/screen text: [FONT_FAMILY], weight [WEIGHT], size [SIZE], color [COLOR]
- Button/control text: [FONT_FAMILY], weight [WEIGHT], size [SIZE], color behavior
- Body/description text: [FONT_FAMILY], weight [WEIGHT], size [SIZE], sample: "[EXAMPLE_TEXT]"
- All text strictly aligned to [GRID_SYSTEM]

### 1.3 Visual Elements
- Core element: [MAIN_COMPONENT], including:
  - [REGION_1]: [SUB_ELEMENTS]
  - [REGION_2]: [SUB_ELEMENTS]
  - [REGION_3]: [SUB_ELEMENTS]
- Background decorations:
  - [POSITION_1]: [ELEMENT_DESCRIPTION]
  - [POSITION_2]: [ELEMENT_DESCRIPTION]
- Layout:
  - [BACKGROUND_TREATMENT]
  - Center: [MAIN_ELEMENT] ([SIZE_PERCENTAGE], alignment)
  - Surrounding: [SECONDARY_ELEMENTS]

### 1.4 Animation Style
- [ELEMENT_TYPE] interaction:
  - Hover [ELEMENT]: [EFFECT_DESCRIPTION] (exact values: rotate ±[DEG]°, translate [X]px, brightness [VALUE])
  - [TRIGGER]: [EFFECT] with timing [DURATION]ms [EASING]
- Scroll parallax:
  - [ELEMENT] displacement/scale behavior
  - Module fade-in sequence
- Page transitions: [TRANSITION_TYPE], duration [VALUE]

## 2. Page Structure (1:1 Complete Long-Page Replication)

### 2.1 Homepage (Hero Section)
- Background: [DESCRIPTION]
- Central element: [DESCRIPTION]
- Text elements: [LIST_WITH_POSITIONS]

### 2.2 Complete Scrolling Page Modules
- **[MODULE_1]**: [DESCRIPTION]
- **[MODULE_2]**: [DESCRIPTION]
- **[MODULE_3]**: [DESCRIPTION]
- **[MODULE_N]**: [DESCRIPTION]

## 3. Core Interactions & Technical Requirements

### 3.1 [Core Interactive Element]
- Implement with [TECH_LIBRARY]
- Mouse event listeners:
  - Hover [ELEMENT]: [EFFECT]
  - Click [ELEMENT]: [EFFECT]
- Mouse movement: [EFFECT]

### 3.2 Scroll Parallax & Page Interaction
- Listen `scroll` event, implement [ELEMENT] parallax displacement
- Module fade-in on scroll
- Navigation: [MENU_BEHAVIOR]

### 3.3 Responsive Adaptation
- PC: [EXPERIENCE_DESCRIPTION]
- Mobile: [ADAPTATIONS]
- Touch: [GESTURE_SUPPORT]

## 4. Tech Stack

- Frontend: [FRAMEWORK] + [LANGUAGE] + [BUILD_TOOL]
- [SPECIALIZED_DOMAIN]: [LIBRARY] ([PURPOSE])
- Styling: [CSS_SOLUTION]
- Animation: [ANIMATION_LIBRARY]
- Fonts: [FONT_1] + [FONT_2] + [FONT_3]
- Deployment: [PLATFORM]
- Backend: [STACK] (if applicable)
- Database: [DATABASE] (if applicable)

## 5. Must-Replicate Details

1. **[DETAIL_1]**: [EXACT_REQUIREMENT]
2. **[DETAIL_2]**: [EXACT_REQUIREMENT]
3. **[DETAIL_3]**: [EXACT_REQUIREMENT]
4. **[DETAIL_4]**: [EXACT_REQUIREMENT]
5. **[DETAIL_5]**: [EXACT_REQUIREMENT]
6. **[DETAIL_6]**: [EXACT_REQUIREMENT]

## 6. Deliverables

- Visual 1:1 replication of original site aesthetic
- Interaction 1:1 replication (animations, transitions, hover states)
- Clean, maintainable, production-ready code
- Responsive across PC/tablet/mobile/touch devices
- Smooth performance, no jank/frame drops
- Fully functional (navigation, interactions, forms)
```

## Template B: Full-Stack Application

Use when the user wants to build a complete web application from scratch (dashboard, SaaS, tool, platform).

```markdown
You are a senior full-stack engineer. Build a complete [APP_TYPE] application.

## 1. Product Overview

- **Product Name**: [NAME]
- **Core Purpose**: [ONE_SENTENCE_DESCRIPTION]
- **Target Users**: [USER_PERSONA]
- **Key Differentiator**: [UNIQUE_VALUE]

## 2. Functional Requirements

### 2.1 Authentication & Authorization
- [METHOD: OAuth/email-password/Magic Link]
- Role-based access: [ROLES]
- Session management: [APPROACH]

### 2.2 Core Features
| Feature | Description | Priority |
|---------|-------------|----------|
| [Feature 1] | [Description] | P0 |
| [Feature 2] | [Description] | P0 |
| [Feature 3] | [Description] | P1 |

### 2.3 Data Models
- **User**: [FIELDS]
- **[Entity 1]**: [FIELDS]
- **[Entity 2]**: [FIELDS]
- **Relationships**: [DESCRIPTION]

## 3. UI/UX Design

### 3.1 Design System
- Style: [MINIMAL/MODERN/ENTERPRISE/PLAYFUL]
- Primary color: #[HEX]
- Surface colors: [LIST]
- Typography: [FONT_FAMILY] for headings, [FONT_FAMILY] for body
- Spacing scale: [BASE_UNIT]px (e.g., 4px base, multiples of 4)

### 3.2 Page Inventory
- **/[ROUTE]**: [PURPOSE], [KEY_COMPONENTS]
- **/[ROUTE]**: [PURPOSE], [KEY_COMPONENTS]
- **/[ROUTE]**: [PURPOSE], [KEY_COMPONENTS]

### 3.3 Component Library
- Reusable components: [LIST: Button, Card, Modal, Table, Form, etc.]
- Layout components: [LIST: Sidebar, Header, PageContainer, etc.]
- Data display: [LIST: Charts, Lists, Grids, Calendars]

## 4. Technical Architecture

### 4.1 Frontend
- Framework: [REACT/VUE/SVELTE]
- State management: [ZUSTAND/REDUX/PINIA]
- Data fetching: [REACT_QUERY/SWR/TRPC]
- UI library: [SHADCN/MUI/ANTD/TAILWIND]
- Form handling: [REACT_HOOK_FORM]
- Validation: [ZOD/YUP]

### 4.2 Backend
- Runtime: [NODE/DENO/BUN]
- Framework: [EXPRESS/FASTIFY/NESTJS]
- API style: [REST/GRAPHQL/TRPC]
- Authentication: [NEXT_AUTH/LUCIA/CLERK]

### 4.3 Database & Storage
- Primary database: [POSTGRESQL/MYSQL/MONGODB]
- ORM: [PRISMA/DRIZZLE/TYPEORM]
- File storage: [S3/CLOUDINARY/LOCAL]
- Caching: [REDIS/MEMORY]

### 4.4 DevOps
- Deployment: [VERCEL/RAILWAY/AWS]
- CI/CD: [GITHUB_ACTIONS]
- Environment variables: [REQUIRED_VARS_LIST]

## 5. API Specification

### 5.1 Endpoints
```
[METHOD] /api/[resource] - [Description]
[METHOD] /api/[resource]/:id - [Description]
```

### 5.2 Request/Response Schemas
- Use [ZOD/JSON_SCHEMA] for validation
- Include error response format

## 6. Implementation Order

1. **[Phase 1]**: [TASKS] (MVP)
2. **[Phase 2]**: [TASKS]
3. **[Phase 3]**: [TASKS]

## 7. Quality Standards

- TypeScript strict mode enabled
- 80%+ test coverage for critical paths
- Lighthouse score: Performance >90, Accessibility >95
- Responsive: Mobile-first, breakpoints at 640/768/1024/1280px
```

## Template C: 3D / Interactive Experience

Use when the user wants immersive 3D websites, WebGL experiences, or heavy animation-driven sites.

```markdown
You are a creative developer specializing in 3D web experiences and interactive animations.

## 1. Concept & Mood

- **Experience Type**: [PRODUCT_SHOWCASE/PORTFOLIO/IMMERSIVE_STORY]
- **Visual Mood**: [Descriptors: futuristic, organic, brutalist, ethereal]
- **Reference Sites**: [URL_1], [URL_2]
- **Core Metaphor**: [DESCRIBE_THE_EXPERIENCE_CONCEPT]

## 2. 3D Elements

### 2.1 Scene Composition
- **Camera**: [PERSPECTIVE/ORTHOGRAPHIC], FOV [VALUE], position [X,Y,Z], lookAt [TARGET]
- **Lighting**:
  - Ambient: [COLOR], intensity [VALUE]
  - Directional: [COLOR], position [X,Y,Z], castShadow [true/false]
  - Point/Spot: [DETAILS]
- **Environment**: [HDRi/Generated], tone mapping [TYPE], exposure [VALUE]

### 2.2 Meshes & Materials
- **Primary Model**: [DESCRIPTION], format [GLB/OBJ/PROCEDURAL]
- **Material style**: [PBR/TOON/MATTE/GLASS], roughness [VALUE], metalness [VALUE]
- **Secondary elements**: [LIST]

### 2.3 Particle Systems
- **Type**: [DUST/FIRE/SPARKLES/CUSTOM]
- **Count**: [NUMBER]
- **Behavior**: [EMITTER_SHAPE, MOVEMENT_PATTERN]
- **Interaction**: [MOUSE_REPEL/ATTRACT/CLICK_BURST]

## 3. Interactions

- **Mouse hover**: [EFFECT_ON_3D_ELEMENTS]
- **Mouse drag**: [ORBIT/PAN/ZOOM_BEHAVIOR]
- **Scroll**: [CAMERA_MOVEMENT/OBJECT_ANIMATION]
- **Click**: [TRIGGER_ACTION]

## 4. Animation Timeline

- **Entry sequence**: [DESCRIPTION], duration [VALUE]
- **Idle animations**: [DESCRIPTION]
- **Transition between sections**: [DESCRIPTION]

## 5. Tech Stack

- 3D Engine: [THREE.JS/REACT_THREE_FIBER/BABYLON]
- Animation: [GSAP/FRAMER_MOTION/REACT_SPRING]
- Physics: [CANNON/REACT_THREE_CANNON/AMMO] (if needed)
- Post-processing: [BLOOM/DOF/SSAO/CHROMATIC_ABERRATION]
- Build tool: [VITE/NEXT.JS]

## 6. Performance Budget

- Target FPS: [60/30]
- Max draw calls: [NUMBER]
- Texture resolution limit: [VALUE]
- Lazy load 3D assets above the fold
- Use LOD (Level of Detail) for complex meshes
```

## Template D: Mobile App (React Native / Flutter)

Use when the user wants a cross-platform mobile application.

```markdown
You are a senior mobile developer. Build a [IOS/ANDROID/CROSS_PLATFORM] app.

## 1. App Overview

- **App Name**: [NAME]
- **Platform**: [IOS_AND_ANDROID]
- **Framework**: [REACT_NATIVE/FLUTTER]
- **App Category**: [CATEGORY]

## 2. Screens

| Screen | Purpose | Key UI |
|--------|---------|--------|
| [Screen 1] | [Purpose] | [Components] |
| [Screen 2] | [Purpose] | [Components] |

## 3. Navigation

- Structure: [STACK/TAB/DRAWER/BOTTOM_SHEET]
- Deep linking: [SCHEMA]

## 4. State Management

- Global state: [ZUSTAND/REDUX/PROVIDER]
- Local state: [USESTATE/USEREDUCER]
- Persistence: [ASYNC_STORAGE/SHARED_PREFERENCES]

## 5. Native Features

- [FEATURE_1]: [CAMERA/LOCATION/PUSH_NOTIFICATIONS/BIOMETRICS]
- [FEATURE_2]: [DESCRIPTION]

## 6. Backend Integration

- API base URL: [URL]
- Auth method: [JWT/OAUTH]
- Real-time: [WEBSOCKET/SSE/FIREBASE]

## 7. Design System

- Follow [MATERIAL_DESIGN/CUpertino/HUMAN_INTERFACE]
- Colors: [PRIMARY, SECONDARY, BACKGROUND, SURFACE, ERROR]
- Typography: [HEADING, BODY, CAPTION]
- Spacing: [VALUES]
```

## Template E: Data Visualization Dashboard

Use when the user wants analytics dashboards, admin panels, or data-heavy interfaces.

```markdown
You are a frontend engineer specializing in data visualization. Build an analytics dashboard.

## 1. Dashboard Purpose

- **Domain**: [BUSINESS_DOMAIN]
- **Primary KPIs**: [LIST]
- **Update frequency**: [REAL_TIME/DAILY/WEEKLY]
- **User types**: [ADMIN/MANAGER/ANALYST]

## 2. Widget Inventory

| Widget | Chart Type | Data Source | Refresh |
|--------|-----------|-------------|---------|
| [Widget 1] | [LINE/BAR/PIE/HEATMAP/NUMBER] | [API_ENDPOINT] | [INTERVAL] |
| [Widget 2] | [TYPE] | [ENDPOINT] | [INTERVAL] |

## 3. Interactions

- **Date range picker**: [PRESETS: Today, 7D, 30D, Custom]
- **Drill-down**: [CLICK_BEHAVIOR]
- **Export**: [CSV/PDF/IMAGE]
- **Real-time**: [WEBSOCKET/SSE_POLLING]

## 4. Visualization Library

- Primary: [D3.JS/RECHARTS/VICTORY/ECHARTS]
- Maps: [MAPBOX/LEAFLET]
- Tables: [TANSTACK_TABLE/AG_GRID]

## 5. Tech Stack

- Frontend: [REACT/VUE]
- Styling: [TAILWIND/ANTD/MUI]
- Data fetching: [REACT_QUERY/SWR]
- State: [ZUSTAND]
```

## Template F: Landing Page / Marketing Site

Use when the user wants a promotional or portfolio website with emphasis on conversion and brand storytelling.

```markdown
You are a conversion-focused frontend developer. Build a high-converting landing page.

## 1. Brand & Positioning

- **Brand**: [NAME]
- **Value Proposition**: [ONE_SENTENCE]
- **Target Audience**: [PERSONA]
- **Tone of Voice**: [DESCRIPTORS]

## 2. Sections (in order)

1. **Hero**: [HEADLINE], [SUBHEADLINE], [CTA_1], [CTA_2], [HERO_IMAGE/VIDEO]
2. **Social Proof**: [LOGOS/TESTIMONIALS/STATS]
3. **Problem/Solution**: [PAIN_POINTS], [HOW_IT_WORKS]
4. **Features**: [3-6_FEATURES_WITH_ICONS]
5. **Pricing**: [TIERS], [FEATURE_LIST_COMPARISON]
6. **FAQ**: [ACCORDION_ITEMS]
7. **Final CTA**: [URGENCY_ELEMENT]
8. **Footer**: [LINKS/SOCIAL/NEWSLETTER]

## 3. Conversion Elements

- **Primary CTA color**: #[HEX] (high contrast, used sparingly)
- **Secondary CTA**: [STYLE]
- **Form fields**: [MINIMUM_FIELDS]
- **Trust signals**: [BADGES/SECURITY_ICONS/GUARANTEES]

## 4. Animations

- **Scroll reveals**: [FADE_UP/STAGGER]
- **Hero entrance**: [SEQUENCE]
- **Micro-interactions**: [HOVER_STATES]

## 5. SEO & Performance

- **Meta title/description**: [COPY]
- **Open Graph image**: [DIMENSIONS]
- **Core Web Vitals targets**: [LCP/CLS/FID]
- **Schema markup**: [TYPE]
```

## Customization Guidelines

When filling templates:

1. Replace ALL bracketed placeholders with concrete values
2. Remove sections that don't apply to the project
3. Add project-specific sections for unique requirements
4. Ensure numeric values include units (px, rem, ms, deg)
5. Specify library versions when compatibility matters (e.g., React Three Fiber v8, Three.js r154)
6. Include explicit "DO NOT" statements for anti-patterns
