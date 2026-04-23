---
name: Prompt Engineer
version: 0.1.0
description: This skill should be used when the user asks to "write a prompt", "generate a prompt", "create a development prompt", "help me write an AI prompt", "I want to clone this website", "replicate this site", "build a website like this", "generate a full-stack prompt", or provides a website URL/screenshot and asks for a detailed development prompt. Also triggers when the user mentions "prompt engineering", "提示词", "帮我写prompt", or requests to convert requirements into an AI-ready instruction.
---

# Prompt Engineer

Transform user requirements into professional, production-ready AI development prompts. This skill specializes in generating detailed, structured prompts for web cloning, full-stack development, mobile apps, 3D/interactive experiences, and data visualization projects.

## Purpose

Convert vague or high-level user requests into precise, comprehensive prompts that can be directly fed to AI coding agents (Claude, GPT-4, Cursor, etc.) to generate production-quality code. Handle inputs ranging from simple text descriptions to website URLs and screenshots.

## Workflow

### Step 1: Identify the Scenario Type

Analyze the user's input to classify the project type:

| Scenario | Indicators |
|----------|------------|
| **Website Clone** | URL provided, screenshot uploaded, "clone", "replicate", "like this site" |
| **Full-Stack App** | CRUD operations, auth, database, dashboard, "build an app" |
| **Mobile App** | iOS, Android, React Native, Flutter, "mobile app" |
| **3D/Interactive** | Three.js, WebGL, animations, "3D", "interactive", "immersive" |
| **Data Visualization** | Charts, dashboards, D3.js, "visualize data", "analytics" |
| **Landing Page** | Marketing site, portfolio, "landing page", "showcase" |

### Step 2: Extract Input Information

Gather all available context from the user:

- **URL**: Fetch the site to analyze structure, content, and meta information
- **Screenshot**: Use vision capabilities to identify layout, colors, typography, components
- **Text Description**: Extract functional requirements, user flows, and business logic
- **References**: Identify style references, competitor sites, or design systems mentioned

### Step 3: Confirm Output Language

Before generating, explicitly ask the user which language they want the final prompt in:

- **English** — Default for feeding to most AI coding agents (Claude, GPT-4, Cursor)
- **Chinese (中文)** — For Chinese-speaking AI agents or when the user prefers native language prompts
- **Bilingual** — Generate both English and Chinese versions side by side

Wait for user confirmation before proceeding to generation.

### Step 4: Analyze and Structure

For each scenario, apply the corresponding analysis framework from `references/`:

- **Website Clone**: Use `references/web-clone-patterns.md` to decompose visual style, layout, interactions, and technical implementation
- **Full-Stack/Mobile/3D/DataViz**: Use `references/prompt-templates.md` for the base structure and `references/tech-stack-guide.md` for stack recommendations

### Step 5: Generate the Prompt

Construct the final prompt with the following sections (adapt based on scenario):

1. **Role Definition**: Define the AI's persona (e.g., "You are a full-stack engineer specializing in...")
2. **Core Objective**: Clear, actionable goal (e.g., "1:1 pixel-perfect clone of [URL]")
3. **Visual Style**: Colors, typography, spacing, design system (for clone: exact hex values, fonts, sizes)
4. **Layout & Structure**: Page hierarchy, sections, component breakdown, responsive behavior
5. **Interactions & Animations**: Hover states, scroll effects, transitions, micro-interactions, 3D behaviors
6. **Technical Stack**: Precise framework/library versions with justification
7. **Data & State**: API requirements, database schema, state management approach
8. **Asset Requirements**: Images, icons, fonts, 3D models, audio files
9. **Detailed Specifications**: Exact measurements, timing values, easing functions, breakpoints
10. **Deliverables**: Code structure, file organization, deployment instructions

### Step 6: Validate and Enhance

Before delivering the prompt:

- Ensure all hex colors, font names, and sizes are explicitly stated (no "similar to" or "approximately")
- Verify that animation timing, easing curves, and transition durations are specified numerically
- Confirm responsive breakpoints and mobile behavior are documented
- Check that the technical stack is cohesive and version-compatible
- Add edge case handling and error state descriptions where applicable

## Rules for High-Quality Prompts

- Be explicit, not suggestive. Use exact values (hex codes, px/rem, timing in ms/s) instead of descriptive adjectives
- Include anti-patterns: explicitly state what NOT to do (e.g., "NO gradients", "NO high-saturation colors")
- Specify relative positioning and z-index layers for complex layouts
- Define the complete user interaction flow (hover → active → focus → disabled states)
- Require 1:1 fidelity for clone projects; allow creative interpretation only for original builds
- Always include responsive/mobile adaptations
- Include performance requirements (FPS targets, lazy loading, bundle size limits) for interactive/3D projects

## Additional Resources

### Reference Files

- **`references/web-clone-patterns.md`** - Detailed decomposition framework for website cloning: color extraction, typography analysis, layout grid system, animation taxonomy, interaction mapping, and pixel-perfect specification methods
- **`references/prompt-templates.md`** - Ready-to-adapt prompt templates for each scenario type (web clone, full-stack app, mobile, 3D, data viz, landing page)
- **`references/tech-stack-guide.md`** - Technology stack selection guide with version recommendations, compatibility matrices, and deployment strategies for each scenario

### Examples

- **`examples/midlife-engineering.md`** - Complete example of a high-fidelity website clone prompt for an industrial minimalist music device showcase site
