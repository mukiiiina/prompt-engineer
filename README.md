# Prompt Engineer / 提示词工程师

**English** | [中文](#中文介绍)

> Transform URLs, screenshots, and ideas into production-ready AI development prompts. Supports English, Chinese, and Bilingual output.
>
> 将网址、截图和想法转化为可直接用于 AI 开发的生产级提示词。支持英文、中文和双语输出。

---

## English

### What is Prompt Engineer?

Prompt Engineer is a **Claude Code skill** that bridges the gap between "I have an idea" and "AI, build this for me." 

Instead of spending hours crafting detailed prompts, simply:
- Paste a website URL
- Upload a screenshot  
- Describe your project in plain language

...and get back a **pixel-perfect, implementation-ready prompt** you can feed directly to Claude, GPT-4, Cursor, or any AI coding agent.

### Supported Scenarios

| Scenario | Input Example | Output |
|----------|--------------|--------|
| **Website Clone** | "Clone https://linear.app" | Exact hex colors, typography, animations, responsive breakpoints |
| **Full-Stack App** | "Build a SaaS dashboard" | Database schema, API spec, auth flow, component library |
| **3D/Interactive** | "3D sneaker configurator" | Three.js scene setup, lighting, camera, interaction mapping |
| **Mobile App** | "React Native fitness app" | Screens, navigation, native features, backend integration |
| **Data Visualization** | "Real-time analytics dashboard" | Chart types, WebSocket pipeline, widget specs |
| **Landing Page** | "High-converting marketing site" | Conversion elements, SEO, scroll reveals, A/B hooks |

### Quick Start

#### 1. Install

```bash
# macOS / Linux
git clone https://github.com/mukiiiina/prompt-engineer.git ~/.claude/skills/prompt-engineer

# Windows
git clone https://github.com/mukiiiina/prompt-engineer.git %USERPROFILE%\.claude\skills\prompt-engineer
```

Claude Code auto-discovers skills on launch.

#### 2. Use It

Just ask naturally. The skill triggers automatically.

**Example 1: Website Clone**
```
User: 帮我写个 prompt 复刻这个网站 https://www.midlife.engineering/
AI: [Analyzes URL... extracts colors, fonts, layout, animations]
AI: 你想要中文版还是英文版的 prompt？
User: 中文版
AI: [Generates 2000+ word Chinese prompt with exact hex values, timing, stack]
```

**Example 2: Full-Stack App**
```
User: Generate a prompt for a real-time analytics dashboard
AI: [Identifies scenario: Data Visualization + Full-Stack]
AI: What language do you want the prompt in? English / Chinese / Both?
User: English
AI: [Generates complete prompt with DB schema, API endpoints, widget specs]
```

**Example 3: From Screenshot**
```
User: [Uploads screenshot of a mobile app UI]
User: 帮我写个 prompt 做这样的 App
AI: [Vision analysis identifies layout, colors, components]
AI: 你要中文还是英文 prompt？
User: 双语
AI: [Generates side-by-side English/Chinese prompt]
```

### Language Selection

Before generating, the skill explicitly asks for your preferred output language:

- **English** (Default) — Best for Claude, GPT-4, Cursor, and most AI coding agents
- **Chinese (中文)** — For Chinese-speaking AI agents or when you prefer native language prompts
- **Bilingual (双语)** — Generates both English and Chinese versions side by side

### Live Demo: Website Clone

**Input:** `https://linear.app` (developer-tool luxury dark mode)

**Analysis Results:**
- Colors: #08070B (bg), #F7F8F8 (text), #5E6AD2 (accent), #8A8F98 (secondary)
- Typography: Inter (display/body), JetBrains Mono (code), 4-tier text hierarchy
- Animations: 5×5 dot-grid with 3200ms step-timing diagonal wave + 2800ms upDown oscillation
- Layout: Fixed nav (64px), hero (160px pt), feature grid (3×2), alternating showcases, footer

**Generated Prompt Preview:**

```markdown
You are a full-stack engineer specializing in developer-tool luxury aesthetics...

## 1. Core Visual Style
### 1.1 Color System
- Background: #08070B (deep space black, NOT #000000)
- Text primary: #F7F8F8, secondary: #8A8F98, tertiary: #5C5F66
- Accent: #5E6AD2 (indigo CTAs)
- Style: NO gradients, NO decorative fluff, pure solid colors

### 1.2 Typography
- Hero: Inter 500, clamp(3rem, 5vw, 4.5rem), letter-spacing -0.02em
- Body: Inter 400, 0.9375rem, line-height 1.6
- Code: JetBrains Mono 400, tabular-nums, "ss01" feature

### 1.3 Animations
- Dot-grid "agent": 3200ms step-timing, diagonal wave, opacity 0.3→1.0
- Dot-grid "upDown": 2800ms step-timing, vertical oscillation
- Scroll reveals: 600ms, cubic-bezier(0.16, 1, 0.3, 1), stagger 100ms

### 1.4 Tech Stack
- Next.js 14 + TypeScript + Tailwind CSS
- Framer Motion (reveals) + CSS keyframes (dot loops)
- Inter + JetBrains Mono fonts
- Deploy: Vercel
```

[Full prompt → `examples/linear-clone.md`](examples/linear-clone.md)

### Prompt Quality Standards

Every generated prompt guarantees:

| Standard | Example |
|----------|---------|
| Exact values | `color: #FF6633` not "orange accent" |
| Anti-patterns | `NO gradients`, `NO neon colors` |
| Numeric timing | `transition: 300ms cubic-bezier(0.4, 0, 0.2, 1)` |
| State flows | Hover → Active → Focus → Disabled |
| Responsive specs | Breakpoints at 640/768/1024/1280px |
| Performance | 60fps target, bundle <200KB |

### Example Gallery

| Example | Scenario | File |
|---------|----------|------|
| Midlife Engineering | Website Clone (Industrial Minimalist) | [`examples/midlife-engineering.md`](examples/midlife-engineering.md) |
| Linear Clone | Website Clone (Developer Luxury Dark) | [`examples/linear-clone.md`](examples/linear-clone.md) |
| SaaS Dashboard | Full-Stack App (Analytics) | [`examples/saas-dashboard.md`](examples/saas-dashboard.md) |
| 3D Sneaker Configurator | 3D Interactive (Product Showcase) | [`examples/3d-product-showcase.md`](examples/3d-product-showcase.md) |
| Fitness Tracker App | Mobile App (React Native) | [`examples/mobile-fitness-app.md`](examples/mobile-fitness-app.md) |
| Marketing Landing Page | Landing Page (Conversion) | [`examples/marketing-landing-page.md`](examples/marketing-landing-page.md) |

---

## 中文介绍

### Prompt Engineer 是什么？

Prompt Engineer 是一个 **Claude Code 技能（Skill）**，它帮你把"我有一个想法"变成"AI，帮我做出来"。

不再需要花几小时写详细的提示词，只需要：
- 粘贴一个网站链接
- 上传一张截图
- 用自然语言描述你的项目

...就能获得一个**像素级精确、可直接执行**的专业开发提示词，直接投喂给 Claude、GPT-4、Cursor 或任何 AI 编程助手。

### 支持的场景

| 场景 | 输入示例 | 输出内容 |
|------|---------|---------|
| **网站复刻** | "复刻 https://linear.app" | 精确 hex 色值、字体、动画、响应式断点 |
| **全栈应用** | "做个 SaaS 数据分析后台" | 数据库模型、API 规范、认证流程、组件库 |
| **3D/交互** | "3D 球鞋定制器" | Three.js 场景、灯光、相机、交互映射 |
| **移动应用** | "React Native 健身 App" | 页面、导航、原生功能、后端对接 |
| **数据可视化** | "实时数据仪表盘" | 图表类型、WebSocket 数据流、组件规格 |
| **落地页** | "高转化营销网站" | 转化元素、SEO、滚动动效、A/B 测试钩子 |

### 快速开始

#### 1. 安装

```bash
# macOS / Linux
git clone https://github.com/mukiiiina/prompt-engineer.git ~/.claude/skills/prompt-engineer

# Windows
git clone https://github.com/mukiiiina/prompt-engineer.git %USERPROFILE%\.claude\skills\prompt-engineer
```

Claude Code 启动时会自动发现技能。

#### 2. 使用

自然语言对话即可，技能会自动触发。

**示例 1：网站复刻**
```
用户：帮我写个 prompt 复刻这个网站 https://www.midlife.engineering/
AI：[分析网址...提取色彩、字体、布局、动画]
AI：你想要中文版还是英文版的 prompt？
用户：中文版
AI：[生成 2000+ 字中文提示词，包含精确色值、动画时长、技术栈]
```

**示例 2：全栈应用**
```
用户：Generate a prompt for a real-time analytics dashboard
AI：[识别场景：数据可视化 + 全栈]
AI: What language do you want the prompt in? English / Chinese / Both?
用户：英文
AI：[生成完整提示词，包含数据库模型、API 端点、组件规格]
```

**示例 3：从截图生成**
```
用户：[上传一张 App UI 截图]
用户：帮我写个 prompt 做这样的 App
AI：[视觉分析识别布局、色彩、组件]
AI：你要中文还是英文 prompt？
用户：双语
AI：[生成中英对照的提示词]
```

### 语言选择

生成前，技能会明确询问你想要的输出语言：

- **英文 (English)** — 默认选项，适合 Claude、GPT-4、Cursor 等大多数 AI 编程助手
- **中文 (Chinese)** — 适合中文 AI 助手，或你更习惯用中文描述需求
- **双语 (Bilingual)** — 同时生成英文和中文版本，左右对照

### 实战演示：网站复刻

**输入：** `https://linear.app` (开发者工具奢华深色风格)

**分析结果：**
- 色彩：#08070B（背景）、#F7F8F8（文字）、#5E6AD2（强调色）、#8A8F98（次要文字）
- 字体：Inter（标题/正文）、JetBrains Mono（代码）、4 级文字层级
- 动画：5×5 点阵网格，3200ms 步进式对角波浪 + 2800ms 上下振荡
- 布局：固定导航（64px）、首屏（160px padding）、特性网格（3×2）、交替展示、页脚

**生成的 Prompt 预览：**

```markdown
你是一位专注于开发者工具奢华美学的前端工程师...

## 一、核心视觉风格
### 1. 色彩系统
- 背景色：#08070B（深空黑，不是 #000000）
- 文字主色：#F7F8F8，次要：#8A8F98，三级：#5C5F66
- 强调色：#5E6AD2（靛蓝 CTA）
- 风格：禁止渐变，禁止装饰性元素，纯纯色块

### 1.2 排版体系
- 首屏标题：Inter 500, clamp(3rem, 5vw, 4.5rem), 字间距 -0.02em
- 正文：Inter 400, 0.9375rem, 行高 1.6
- 代码：JetBrains Mono 400, 等宽数字, "ss01" 字体特性

### 1.3 动效
- 点阵 "agent"：3200ms 步进式，对角波浪，透明度 0.3→1.0
- 点阵 "upDown"：2800ms 步进式，垂直振荡
- 滚动显现：600ms, cubic-bezier(0.16, 1, 0.3, 1), 子元素错峰 100ms

### 1.4 技术栈
- Next.js 14 + TypeScript + Tailwind CSS
- Framer Motion（显现动效）+ CSS 关键帧（点阵循环）
- Inter + JetBrains Mono 字体
- 部署：Vercel
```

[完整提示词 → `examples/linear-clone.md`](examples/linear-clone.md)

### Prompt 质量标准

每个生成的提示词都保证：

| 标准 | 示例 |
|------|------|
| 精确数值 | `color: #FF6633` 而不是 "橙色强调" |
| 反模式声明 | `禁止渐变`、`禁止霓虹色` |
| 数值化时间 | `transition: 300ms cubic-bezier(0.4, 0, 0.2, 1)` |
| 完整状态流 | 悬停 → 激活 → 聚焦 → 禁用 |
| 响应式规格 | 断点 640/768/1024/1280px |
| 性能指标 | 60fps 目标，打包 <200KB |

### 示例库

| 示例 | 场景 | 文件 |
|------|------|------|
| Midlife Engineering | 网站复刻（工业极简风） | [`examples/midlife-engineering.md`](examples/midlife-engineering.md) |
| Linear Clone | 网站复刻（开发者奢华暗黑） | [`examples/linear-clone.md`](examples/linear-clone.md) |
| SaaS 仪表盘 | 全栈应用（数据分析） | [`examples/saas-dashboard.md`](examples/saas-dashboard.md) |
| 3D 球鞋定制器 | 3D 交互（产品展示） | [`examples/3d-product-showcase.md`](examples/3d-product-showcase.md) |
| 健身追踪 App | 移动应用（React Native） | [`examples/mobile-fitness-app.md`](examples/mobile-fitness-app.md) |
| 营销落地页 | 落地页（高转化） | [`examples/marketing-landing-page.md`](examples/marketing-landing-page.md) |

---

## Skill Structure

```
prompt-engineer/
├── SKILL.md                              # 核心技能（触发器 + 工作流程 + 语言选择）
├── README.md                             # 本文件（双语文档 + 使用演示）
├── LICENSE                               # MIT 开源协议
├── references/
│   ├── web-clone-patterns.md             # 网站复刻分析框架
│   ├── prompt-templates.md               # 6 种场景 Prompt 模板（A-F）
│   └── tech-stack-guide.md               # 技术栈选择指南
└── examples/
    ├── midlife-engineering.md            # 网站复刻：工业极简音乐设备
    ├── linear-clone.md                   # 网站复刻：开发者工具奢华暗黑
    ├── saas-dashboard.md                 # 全栈应用：数据分析仪表盘
    ├── 3d-product-showcase.md            # 3D 交互：球鞋定制器
    ├── mobile-fitness-app.md             # 移动应用：健身追踪 App
    └── marketing-landing-page.md         # 落地页：高转化营销网站
```

## How It Works / 工作原理

```
Your Input (URL / Screenshot / Text Description)
           |
           v
   +-----------------------+
   | 1. Scenario Detection |  <- Identify project type
   +-----------------------+
           |
           v
   +-----------------------+
   | 2. Information Extract|  <- Colors, fonts, layout, animations
   +-----------------------+
           |
           v
   +-----------------------+
   | 3. Language Selection |  <- English / Chinese / Bilingual
   +-----------------------+
           |
           v
   +-----------------------+
   | 4. Analysis & Structure| <- Apply templates & frameworks
   +-----------------------+
           |
           v
   +-----------------------+
   | 5. Prompt Generation  |  <- Build structured prompt
   +-----------------------+
           |
           v
   +-----------------------+
   | 6. Validate & Enhance |  <- Quality checks
   +-----------------------+
           |
           v
   Production-Ready Prompt (copy & paste to AI coder)
```

## Contributing / 贡献

**English:** Found a scenario not covered? Want to improve a template? Fork this repo, add your example to `examples/`, and submit a PR.

**中文:** 发现有未覆盖的场景？想改进模板？Fork 本仓库，在 `examples/` 中添加你的示例，然后提交 PR。

## License / 许可证

MIT License — see [LICENSE](LICENSE) for details.

---

**Made with passion for AI-assisted development.**

> "Give me a URL, I'll give you a prompt."
> "给我一个链接，我给你一个提示词。"
