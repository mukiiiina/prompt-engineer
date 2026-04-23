# Example: SaaS Analytics Dashboard Prompt

A full-stack data analytics dashboard prompt demonstrating the Full-Stack Application template (Template B).

---

## Generated Prompt

You are a senior full-stack engineer. Build a complete SaaS analytics dashboard application.

## 1. Product Overview

- **Product Name**: DataPulse
- **Core Purpose**: Real-time business intelligence dashboard for e-commerce operators to monitor sales, traffic, and conversion metrics
- **Target Users**: E-commerce store owners, marketing managers, data analysts
- **Key Differentiator**: Sub-100ms data updates via WebSocket, AI-powered anomaly detection alerts

## 2. Functional Requirements

### 2.1 Authentication & Authorization
- OAuth 2.0 + email-password hybrid
- Role-based access: Admin (full control), Analyst (read + create reports), Viewer (read-only)
- Session management: JWT with 7-day refresh token rotation
- SSO support: Google Workspace, Microsoft Entra ID

### 2.2 Core Features

| Feature | Description | Priority |
|---------|-------------|----------|
| Real-time Metrics | Live sales, traffic, conversion rate widgets | P0 |
| Custom Reports | Drag-and-drop report builder with 15+ chart types | P0 |
| Anomaly Alerts | AI-detected outliers push notifications | P1 |
| Data Export | CSV, PDF, Excel export with scheduling | P1 |
| Team Collaboration | Shared dashboards, comments, annotations | P2 |

### 2.3 Data Models

- **User**: id, email, name, avatar, role, createdAt, lastLogin, oauthProvider
- **Dashboard**: id, name, layout, widgets[], ownerId, sharedWith[], createdAt, updatedAt
- **Widget**: id, type, title, dataSource, config, position {x,y,w,h}, refreshInterval
- **DataSource**: id, name, type (shopify/stripe/custom-api), credentials (encrypted), schema
- **Alert**: id, widgetId, condition, threshold, channel (email/slack/webhook), status
- **ActivityLog**: id, userId, action, entityType, entityId, timestamp

## 3. UI/UX Design

### 3.1 Design System
- Style: Modern enterprise, clean, high information density
- Primary color: #0F172A (slate-900)
- Surface colors: #FFFFFF (card), #F1F5F9 (page bg), #E2E8F0 (border)
- Accent: #3B82F6 (blue-500) for primary actions, #10B981 (emerald) for positive trends, #EF4444 (red) for negative
- Typography: Inter for headings (600/700), Inter for body (400), JetBrains Mono for data (400)
- Spacing scale: 4px base (4, 8, 12, 16, 24, 32, 48, 64)

### 3.2 Page Inventory

| Route | Purpose | Key Components |
|-------|---------|---------------|
| /login | Authentication | OAuth buttons, email form, magic link |
| /dashboard | Main dashboard | Widget grid, date picker, refresh controls |
| /reports | Report builder | Chart picker, data source selector, preview |
| /alerts | Alert management | Rule builder, notification log, status toggle |
| /settings | App settings | Profile, team, billing, integrations |
| /data-sources | Connection management | API connectors, sync status, schema viewer |

### 3.3 Component Library

- **Layout**: Sidebar (collapsible, 240px/64px), Header (64px, sticky), PageContainer (max-w-7xl)
- **Data Display**: MetricCard, Sparkline, DataTable, ProgressBar, StatusBadge
- **Charts**: LineChart, BarChart, AreaChart, PieChart, Heatmap, FunnelChart, Gauge
- **Forms**: Input, Select, DateRangePicker, Switch, Slider, ColorPicker
- **Feedback**: Toast, Modal, Skeleton, EmptyState, LoadingSpinner
- **Navigation**: Breadcrumb, Tabs, Pagination, CommandPalette

## 4. Technical Architecture

### 4.1 Frontend
- Framework: Next.js 14 (App Router) + TypeScript 5.3
- State management: Zustand (client), TanStack Query (server)
- Data fetching: TanStack Query v5 with WebSocket fallback
- UI library: shadcn/ui + Tailwind CSS
- Forms: React Hook Form + Zod
- Charts: Recharts (primary), ECharts (complex)
- Tables: TanStack Table v8
- Date handling: date-fns

### 4.2 Backend
- Runtime: Node.js 20 LTS
- Framework: Next.js API Routes + tRPC
- Auth: NextAuth.js v5 (beta)
- Real-time: Ably or Socket.io for live data streaming

### 4.3 Database & Storage
- Primary database: PostgreSQL 16 + Prisma ORM
- Cache: Redis (Upstash) for sessions, query cache
- Search: Meilisearch for dashboard/document search
- File storage: AWS S3 (CSV exports, report PDFs)

### 4.4 DevOps
- Deployment: Vercel (frontend + API), Railway (PostgreSQL)
- CI/CD: GitHub Actions
- Monitoring: Vercel Analytics + Logflare

## 5. API Specification

### 5.1 tRPC Routers

```
dashboard.list      - GET    List user dashboards
dashboard.create    - POST   Create new dashboard
dashboard.update    - PATCH  Update layout/widgets
dashboard.delete    - DELETE Remove dashboard
widget.data         - GET    Fetch widget data (polling/WS)
alert.create        - POST   Create alert rule
alert.trigger       - POST   Manual alert test
export.csv          - POST   Generate CSV export
export.pdf          - POST   Generate PDF report
```

### 5.2 WebSocket Events

```
connect     - Client connects with JWT
subscribe   - Subscribe to dashboard widget updates
unsubscribe - Unsubscribe from widget
update      - Server pushes new data point
alert       - Server pushes anomaly alert
```

## 6. Widget Specifications

### 6.1 Metric Card
- Size: 1x1 grid unit (min 280px)
- Content: Label, current value, change %, sparkline (7d)
- Color: Positive #10B981, Negative #EF4444, Neutral #64748B
- Animation: Count-up on load (duration 800ms, easing easeOutExpo)

### 6.2 Line Chart
- Axes: X = time (hour/day/week), Y = value
- Lines: Primary #3B82F6, Comparison #8B5CF6
- Tooltip: Custom styled, shows exact value + change
- Brush: Allow zoom/pan on time axis
- Refresh: Real-time dot indicator (pulsing #10B981)

### 6.3 Data Table
- Pagination: 25/50/100 rows per page
- Sorting: Multi-column, server-side
- Filtering: Column-level text/date/number filters
- Row actions: Edit, Delete, Duplicate, Export row
- Selection: Checkbox multi-select with bulk actions

## 7. Responsive Strategy

- **Desktop (>1280px)**: Full sidebar, 4-column widget grid, all features
- **Laptop (1024-1280px)**: Collapsed sidebar, 3-column grid, charts simplified
- **Tablet (768-1024px)**: Hidden sidebar (drawer), 2-column grid, tables cardified
- **Mobile (<768px)**: Bottom nav, 1-column stack, swipe between widgets, export disabled

## 8. Implementation Order

1. **Phase 1 - MVP (Week 1-2)**
   - Auth (NextAuth + middleware)
   - Dashboard grid with 3 widget types (Metric, Line, Table)
   - PostgreSQL schema + Prisma setup
   - Mock data API

2. **Phase 2 - Core (Week 3-4)**
   - Real-time WebSocket data pipeline
   - Date range picker + data filtering
   - CSV export
   - Responsive optimization

3. **Phase 3 - Polish (Week 5-6)**
   - Alert system with AI anomaly detection
   - Report builder
   - PDF export
   - Performance optimization (React.memo, virtualization)

## 9. Quality Standards

- TypeScript strict mode enabled, no `any` types
- 80%+ unit test coverage for utils/hooks
- E2E tests for critical flows (Playwright)
- Lighthouse: Performance >90, Accessibility >95, SEO >90
- Bundle size: <200KB initial JS (excluding charts)
- API response time: P95 <200ms
- WebSocket latency: <100ms end-to-end
