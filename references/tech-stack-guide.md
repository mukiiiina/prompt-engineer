# Technology Stack Selection Guide

Recommend precise technology stacks based on project scenario, complexity, and performance requirements. Use this guide to fill the "Tech Stack" section of generated prompts.

## Web Clone / Replication

### Standard Marketing Site (No 3D)
- **Frontend**: React 18 + TypeScript + Vite
- **Styling**: Tailwind CSS (utility-first, easy to match arbitrary designs)
- **Animation**: GSAP + ScrollTrigger (scroll-driven animations), Framer Motion (React component animations)
- **Fonts**: Load from Google Fonts or self-host; specify exact weights
- **Icons**: Lucide React or Heroicons
- **Deployment**: Vercel (zero-config, edge network)

### 3D / WebGL Heavy Site
- **Frontend**: React 18 + TypeScript + Vite
- **3D Engine**: React Three Fiber (R3F) + Three.js
- **Styling**: Tailwind CSS + @react-three/drei (helpers)
- **Animation**: GSAP (UI), @react-three/fiber useFrame (3D animations)
- **Post-processing**: @react-three/postprocessing
- **Physics**: @react-three/cannon (if needed)
- **State**: Zustand (lightweight, works well with R3F)
- **Deployment**: Vercel (ensure GLB/GLTF assets are optimized)

### E-commerce Clone
- **Frontend**: Next.js 14 (App Router) + TypeScript
- **Styling**: Tailwind CSS + shadcn/ui
- **Cart**: Custom Zustand store or Shopify Storefront API
- **Payments**: Stripe Elements
- **CMS**: Sanity or Contentful (for product data)
- **Deployment**: Vercel

## Full-Stack Application

### Modern SaaS / Dashboard
- **Frontend**: Next.js 14 (App Router) + TypeScript
- **Styling**: Tailwind CSS + shadcn/ui component library
- **Forms**: React Hook Form + Zod validation
- **Data Fetching**: TanStack Query (React Query) v5
- **State**: Zustand (server state in TanStack Query, client state in Zustand)
- **Auth**: NextAuth.js v5 (beta) or Clerk
- **Backend**: Next.js API Routes or tRPC
- **Database**: PostgreSQL + Prisma ORM (or Drizzle for edge compatibility)
- **File Storage**: AWS S3 or Cloudinary
- **Real-time**: Ably or Pusher (if needed)
- **Deployment**: Vercel (frontend) + Railway/Render (DB) or Vercel Postgres

### Content-Heavy Platform
- **Frontend**: Next.js 14 + TypeScript
- **Styling**: Tailwind CSS
- **CMS**: Sanity, Strapi, or Directus
- **Search**: Algolia or Meilisearch
- **Comments**: Giscus or Disqus
- **Deployment**: Vercel

### API-Heavy Backend Service
- **Runtime**: Node.js 20 LTS
- **Framework**: Fastify (performance) or NestJS (enterprise structure)
- **API**: REST or tRPC
- **Validation**: Zod
- **Auth**: Lucia Auth or custom JWT
- **Database**: PostgreSQL + Prisma or MongoDB + Mongoose
- **Caching**: Redis (Upstash for serverless)
- **Queue**: BullMQ + Redis (background jobs)
- **Deployment**: Railway, Render, or Fly.io

## 3D / Interactive Experience

### Product Showcase (3D Configurator)
- **Frontend**: React 18 + Vite
- **3D**: React Three Fiber + Three.js
- **Helpers**: @react-three/drei (environment, controls, loaders)
- **Post-processing**: @react-three/postprocessing
- **Animation**: GSAP (UI), custom useFrame loops (3D)
- **State**: Zustand
- **Deployment**: Vercel

### Immersive Storytelling
- **Frontend**: React 18 + Vite or Next.js
- **3D/WebGL**: React Three Fiber + Three.js
- **Scroll**: GSAP ScrollTrigger (pin sections, scrub animations)
- **Text**: React + GSAP SplitText (character-level animations)
- **Sound**: Howler.js or Web Audio API
- **Deployment**: Vercel

### Generative Art / Shader Playground
- **Frontend**: React 18 + Vite
- **Shaders**: React Three Fiber + custom GLSL
- **Math**: glslify, simplex-noise
- **Recording**: canvas-capture (export videos)
- **Deployment**: Vercel

## Mobile Application

### Cross-Platform (iOS + Android)
- **Framework**: React Native 0.73 + Expo SDK 50
- **Navigation**: Expo Router
- **Styling**: NativeWind (Tailwind for RN) or StyleSheet
- **State**: Zustand
- **Data Fetching**: TanStack Query
- **Auth**: Expo Auth Session or Clerk Expo
- **Storage**: AsyncStorage + SecureStore
- **Push Notifications**: Expo Notifications
- **Deployment**: EAS Build + App Store / Play Store

### Performance-Critical Mobile Game
- **Framework**: Flutter 3.19 + Dart
- **State**: Riverpod or Bloc
- **Graphics**: Flutter Flame (2D games) or custom CustomPainter
- **Storage**: Hive (local) + Firebase (cloud)
- **Deployment**: Codemagic CI/CD

## Data Visualization

### Real-Time Analytics Dashboard
- **Frontend**: React 18 + TypeScript + Vite
- **Styling**: Tailwind CSS
- **Charts**: ECharts or Victory (React-friendly)
- **Maps**: Mapbox GL JS or Leaflet
- **Tables**: TanStack Table v8
- **Real-time**: WebSocket or Server-Sent Events
- **State**: Zustand
- **Deployment**: Vercel

### Scientific / Complex Visualization
- **Frontend**: React 18 + TypeScript
- **Canvas**: D3.js (data manipulation + SVG) or custom HTML5 Canvas
- **WebGL**: Three.js (3D data viz) or deck.gl (geospatial)
- **Large datasets**: Web Workers + DuckDB-Wasm
- **Deployment**: Vercel or Netlify

## Landing Page / Portfolio

### Designer Portfolio
- **Frontend**: Next.js 14 or Astro (static generation)
- **Styling**: Tailwind CSS
- **Animations**: GSAP + ScrollTrigger, Lenis (smooth scroll)
- **Images**: Next.js Image optimization or Cloudinary
- **CMS**: Sanity or MDX (content)
- **Deployment**: Vercel

### High-Converting SaaS Landing Page
- **Frontend**: Next.js 14 (App Router)
- **Styling**: Tailwind CSS + shadcn/ui
- **Forms**: React Hook Form + Zod
- **Analytics**: Vercel Analytics + Plausible
- **A/B Testing**: Vercel Flags or PostHog
- **Deployment**: Vercel

## Database Selection Matrix

| Scenario | Recommendation | Why |
|----------|---------------|-----|
| Relational data, complex queries | PostgreSQL 16 | ACID, JSON support, full-text search |
| Serverless/Edge functions | PostgreSQL + Prisma or Drizzle | Connection pooling, edge-compatible ORMs |
| Rapid prototyping | SQLite (local) → PostgreSQL (prod) | Zero-config start, easy migration |
| Document store, flexible schema | MongoDB Atlas | Schema evolution, nested documents |
| Real-time sync | Firebase Firestore or Supabase | Built-in real-time subscriptions |
| Caching / Sessions | Redis (Upstash) | Sub-millisecond reads, TTL support |
| Search | Meilisearch or Algolia | Typo-tolerance, faceted search |

## Common Pairings

### The "Modern React" Stack (Recommended Default)
- Next.js 14 + TypeScript + Tailwind CSS + shadcn/ui
- TanStack Query + Zustand
- Prisma + PostgreSQL
- NextAuth.js or Clerk
- Vercel

### The "Lightweight" Stack (Simple Projects)
- React 18 + Vite + TypeScript
- Tailwind CSS
- Zustand
- Static JSON or localStorage
- Vercel or Netlify

### The "3D Studio" Stack
- React 18 + Vite
- React Three Fiber + Three.js + Drei
- GSAP
- Zustand
- Vercel

### The "Mobile-First" Stack
- React Native + Expo
- NativeWind
- TanStack Query
- Zustand
- Supabase or Firebase

## Version Pinning Guidelines

When specifying versions in prompts:

- Use **major versions** for stability (e.g., React 18, Next.js 14)
- Use **specific minor versions** for cutting-edge features (e.g., Three.js r160)
- Always specify **TypeScript** as the language (not JavaScript)
- Specify **Node.js 20 LTS** as the runtime for backend projects
- Specify **npm** or **pnpm** as the package manager (prefer pnpm for monorepos)

## Deployment Recommendations

| Platform | Best For | Features |
|----------|----------|----------|
| **Vercel** | Next.js, React, static sites | Edge network, serverless functions, preview deploys |
| **Netlify** | Static sites, JAMstack | Forms, Identity, edge functions |
| **Railway** | Backend services, databases | Easy PostgreSQL/Redis, auto-deploy from Git |
| **Render** | Full-stack apps, cron jobs | Static sites, web services, PostgreSQL |
| **Fly.io** | Docker containers, global edge | Close to users, persistent volumes |
| **Supabase** | Firebase alternative | PostgreSQL, auth, storage, real-time |
