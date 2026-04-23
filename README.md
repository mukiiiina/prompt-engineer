# Prompt Engineer

A Claude Code skill that transforms your requirements into production-ready AI development prompts. Drop a website URL, upload a screenshot, or describe your idea — get a detailed, structured prompt you can feed directly to Claude, GPT-4, Cursor, or any AI coding agent.

## Overview

This skill specializes in generating **pixel-perfect, implementation-ready prompts** for:

- **Website Cloning** — 1:1 replication of existing sites with exact colors, typography, animations
- **Full-Stack Applications** — SaaS platforms, dashboards, CRUD apps with auth & database
- **3D / Interactive Experiences** — WebGL, Three.js, immersive scroll-driven sites
- **Mobile Apps** — React Native / Flutter cross-platform applications
- **Data Visualization** — Real-time analytics dashboards, complex chart systems
- **Landing Pages** — High-converting marketing sites with conversion optimization

## How It Works

```
Your Input (URL / Screenshot / Text)
           |
           v
   +-------------------+
   |  Scenario Detection |
   +-------------------+
           |
           v
   +-------------------+
   |  Visual Analysis  |  <- Extract colors, fonts, layout, animations
   +-------------------+
           |
           v
   +-------------------+
   |  Prompt Generation |  <- Structured, explicit, AI-ready
   +-------------------+
           |
           v
   Production-Ready Prompt (copy & paste to AI coder)
```

## Quick Start

### 1. Install the Skill

Copy this repository into your Claude Code skills directory:

```bash
# macOS / Linux
git clone https://github.com/YOUR_USERNAME/prompt-engineer.git ~/.claude/skills/prompt-engineer

# Windows
 git clone https://github.com/YOUR_USERNAME/prompt-engineer.git %USERPROFILE%\.claude\skills\prompt-engineer
```

Claude Code will auto-discover the skill on next launch.

### 2. Use It

Just ask naturally — the skill triggers automatically:

| What You Say | What You Get |
|-------------|--------------|
| "帮我写个 prompt 复刻这个网站 https://example.com" | Complete website clone prompt with exact hex colors, font sizes, animation timings |
| "生成一个全栈 SaaS 应用的开发提示词" | Full-stack app prompt with database schema, API spec, component list |
| "我要做个 3D 产品展示页" | Three.js / R3F prompt with camera, lighting, interaction specs |
| "帮我写个 React Native 的 prompt" | Mobile app prompt with navigation, state management, native features |
| "这个截图帮我出个 prompt" | Vision-analyzed prompt extracting layout, colors, components from image |

### 3. Feed the Output

Copy the generated prompt and paste it into:
- **Claude Code** (`claude` CLI)
- **Cursor** (Ctrl+K / Cmd+K)
- **ChatGPT / GPT-4**
- **Any AI coding agent**

## Examples

### Example 1: Website Clone

**Input:**
> 帮我写个 prompt 1:1 复刻 https://www.midlife.engineering/

**Output:** See [`examples/midlife-engineering.md`](examples/midlife-engineering.md)

A 2000+ word prompt specifying:
- Exact hex color system (`#F0F0F0`, `#1A1A1A`, `#FF6633`)
- Typography with `clamp()` sizes (`clamp(8rem, 20vw, 15rem)`)
- 3D device model interactions (knob rotation 15deg, button depression 2px)
- Scroll parallax, typewriter animations, responsive breakpoints

**Result when fed to AI:**

```
✅ 工业极简科技风 1:1 还原
✅ Three.js 设备模型 + 拟物交互
✅ 滚动视差 + 打字机动效
✅ PC / 移动端完全适配
```

### Example 2: SaaS Dashboard

**Input:**
> 帮我写个全栈数据分析仪表盘的 prompt

**Output:** See [`examples/saas-dashboard.md`](examples/saas-dashboard.md)

Includes:
- Role-based auth (Admin / Analyst / Viewer)
- Real-time WebSocket data pipeline
- 8 widget types (line, bar, heatmap, KPI number, table)
- TanStack Table + ECharts + Zustand stack
- Responsive grid layout (1/2/3/4 columns by breakpoint)

### Example 3: 3D Product Showcase

**Input:**
> 我要做个 3D 球鞋定制器，写个 prompt

**Output:** See [`examples/3d-product-showcase.md`](examples/3d-product-showcase.md)

Includes:
- React Three Fiber scene setup
- Camera orbit controls + auto-rotate
- Material color picker interaction
- 360-degree product rotation
- AR view placeholder integration

## Skill Structure

```
prompt-engineer/
├── SKILL.md                              # Core skill file (triggers & workflow)
├── references/
│   ├── web-clone-patterns.md             # Website decomposition framework
│   ├── prompt-templates.md              # 6 scenario templates (A-F)
│   └── tech-stack-guide.md              # Stack selection matrix & pairings
└── examples/
    ├── midlife-engineering.md            # Website clone (industrial minimalist)
    ├── saas-dashboard.md                 # Full-stack SaaS dashboard
    └── 3d-product-showcase.md            # 3D interactive product configurator
```

## Prompt Quality Standards

Every generated prompt follows these rules:

| Rule | Example |
|------|---------|
| **Exact values, not descriptions** | `color: #FF6633` instead of `orange accent color` |
| **Anti-pattern declarations** | `NO gradients`, `NO neon colors`, `NO drop shadows` |
| **Numeric timing** | `transition: 300ms cubic-bezier(0.4, 0, 0.2, 1)` |
| **Complete state flows** | Hover → Active → Focus → Disabled |
| **Responsive specs** | Breakpoints at 640/768/1024/1280px with exact changes |
| **Performance targets** | 60fps, FCP <1.8s, LCP <2.5s |

## Supported Scenarios

| Scenario | Template | Key Sections |
|----------|----------|-------------|
| Website Clone | Template A | Visual identity, layout grid, animation taxonomy, asset spec |
| Full-Stack App | Template B | Data models, API spec, auth, component library |
| 3D / Interactive | Template C | Scene composition, lighting, interaction mapping, performance budget |
| Mobile App | Template D | Screens, navigation, native features, backend integration |
| Data Viz | Template E | Widget inventory, chart types, real-time pipeline |
| Landing Page | Template F | Conversion elements, SEO, scroll reveals, A/B testing hooks |

## Contributing

Found a scenario not covered? Want to improve a template?

1. Fork this repository
2. Add your example to `examples/` or improve `references/`
3. Submit a PR with a description of the scenario

## License

MIT License — see [LICENSE](LICENSE) for details.

---

**Made with ❤️ for AI-assisted development.**

> "Give me a URL, I'll give you a prompt."
