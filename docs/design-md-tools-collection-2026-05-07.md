# DESIGN.md 工具生态全景 · 六大工具横向对比

> 来源：[@ricouii on X](https://x.com/ricouii/status/2051853718145139002)
> 发布者：RicoUI — 网页设计师，探索 AI 和 Vibe Coding
> 整理时间：2026-05-07
> 原作者推荐：Refero Styles（最全面）、Neuform（视觉体验最佳）
> 来自hueshadow

---

## 简介

DESIGN.md 是 Google 推出的开源设计规范格式（Apache-2.0），将品牌视觉身份描述为 AI 编码代理可消费的文件——YAML 设计令牌 + Markdown 设计理念。它是连接「人类审美」与「AI 生成 UI」的桥梁，让 Cursor、Claude Code、Codex 等 AI 编码工具能按照统一的设计系统产出界面。

@ricouii 这条推文在 X 上获得 **12.2 万次查看、376 次转帖、2,320 次喜欢**，汇集了当前 DESIGN.md 工具生态系统中最值得关注的六个工具。本文对这六个工具进行深度横向对比，帮助你根据实际需求选择合适的方案。

---

## 内容清单总览

| 序号 | 工具 | 核心定位 | 输入 | 输出格式 | 推荐理由 |
|------|------|----------|------|----------|----------|
| 1 | **Refero Styles** | 设计系统灵感库 | 品牌/URL 搜索 | DESIGN.md + Tailwind v4 + CSS Variables + Design Tokens | 2000+精选设计，输出最全面 |
| 2 | **Neuform** | AI 落地页/设计系统一体 | Prompt 驱动 | 网页 + 移动端 + 设计系统 | 视觉体验最佳，16K+ 用户 |
| 3 | **DesignMD** | AI 一键生成 DESIGN.md | 任意 URL | DESIGN.md 规范文件 | 13,514+ 文件已生成，最成熟 |
| 4 | **designmd.supply** | 品牌风格指南生成器 | 域名 | Google DESIGN.md | 开源，Context.dev 驱动 |
| 5 | **getdesign.md** | DESIGN.md 文件档案馆 | 浏览/搜索 | 71 个生产级 DESIGN.md | 首个生态集合，覆盖面最广 |
| 6 | **design-md-chrome** | Chrome 扩展即开即用 | 当前网页 | DESIGN.md + SKILL.md | 零配置，一键提取 |

---

## 详细内容

### 1. Refero Styles — 设计系统灵感库

**来源**：[@refero_design](https://refero.design)
**链接**：[styles.refero.design](https://styles.refero.design)
**类型**：工具 + 设计灵感库

#### 核心功能

Refero 是一个专为 AI 代理构建的设计系统参考平台，核心理念是「让 AI 代理拥有真正的设计品味」。它提供：

- **2000+ 精选设计系统**：收录 ElevenLabs、Apple、Linear、Mercury、Cursor、Stripe、Superhuman、Anthropic、Raycast 等知名产品的真实设计风格
- **多维度搜索**：支持按品牌名称、情绪（mood）、色彩、字体、URL 进行搜索
- **最全面的输出格式**：同时生成 DESIGN.md、Tailwind v4 主题、CSS Variables、W3C Design Tokens
- **Refero MCP**：通过 Model Context Protocol 直接接入 Cursor、Claude、Windsurf 等 AI 编码工具

#### 发布者洞察

> @ricouii：*「个人推荐 refero，提供了 2,000+ DESIGN.md，以及支持 DESIGN.md、Tailwind v4、CSS Variables 和 Design Tokens 最全面的配置输出。」*

#### 独特优势

- 输出格式最丰富 —— 一份设计同时导出四种格式，前端工程化友好度最高
- MCP 集成最深入 —— AI 代理可以直接调用设计系统，无需手动复制文件
- 设计品味筛选 —— 收录的是真实高水准产品的设计，而非自动抓取的低质量数据

#### 适用场景

- 需要为 AI 编码代理提供「设计灵感」而非死板模板
- 前端项目需要 Tailwind 主题 / CSS Variables 等可直接引用的变量
- 团队成员使用不同 AI 编码工具（Cursor/Claude/Windsurf），需要一个统一的设计源

---

### 2. Neuform — Prompt 驱动的全栈设计工作流

**来源**：[@rob](https://x.com/rob)、[@mengto](https://x.com/mengto)
**链接**：[neuform.ai](https://neuform.ai)
**类型**：AI 设计工具

#### 核心功能

Neuform 的定位远超「生成 DESIGN.md」——它是一个 **Prompt-to-Production 设计工作流**。核心理念是用一个 Prompt 同时驱动网页、移动端和设计系统的产出。

- **Prompt 驱动**：输入一个提示词，同时生成网页布局、移动端适配和设计系统
- **Remix 机制**：可以在不丢失设计概念的前提下探索不同方向，快速试错
- **设计系统导出**：支持输入任意网站 URL 生成对应的设计规范和配置
- **16.3K 用户**：社区活跃，用户来自全球各地

#### 发布者洞察

> @ricouii：*「neuform 给我的视觉体验更好。」*

#### 独特优势

- 视觉生成质量一流 —— 不是简单的模板填充，而是有设计感的产出
- Remix 功能独一无二 —— 可以在已有设计基础上「重新混音」，探索不同变体
- 全栈输出 —— 同时覆盖 Web、Mobile、Design System 三个维度

#### 适用场景

- 从零开始构建产品，需要快速探索多个设计方向
- 需要一个「设计系统 + 落地页 + 移动端」的统一出口
- 重视视觉质感，不希望产出千篇一律的模板

---

### 3. DesignMD — 最成熟的 URL 转 DESIGN.md 工具

**来源**：[Crowdlinker](https://crowdlinker.com)
**链接**：[designmd.me](https://designmd.me)
**类型**：AI 工具 / SaaS

#### 核心功能

DesignMD 是目前生态中**运行时间最长、生成数量最多**的 DESIGN.md 生成工具。

- **URL 输入**：粘贴任何网站 URL，自动分析并生成 DESIGN.md
- **13,514+ 文件已生成**：是目前最成熟的 DESIGN.md 生成引擎
- **Discover 功能**：可以浏览其他用户生成的 DESIGN.md 文件，获取灵感
- **免费额度**：提供 3 次免费使用（注册后可能更多）
- **规范兼容**：严格遵循 Google DESIGN.md 规范

#### 独特优势

- 成熟度最高 —— 13K+ 次生成积累了大量的模型优化经验
- 即用即走 —— 不需要注册就能生成（3 次免费），适合尝鲜
- Discover 社区 —— 可以借鉴他人的设计系统

#### 适用场景

- 需要快速将某个参考网站的设计规范转化为 DESIGN.md
- 团队需要大量批量生成设计系统
- 希望通过社区发现获取设计灵感

---

### 4. designmd.supply — 开源品牌风格指南生成器

**来源**：[Context.dev](https://context.dev)
**链接**：[designmd.supply](https://designmd.supply)
**类型**：开源工具

#### 核心功能

designmd.supply 是最「硬核」的选项 —— 它通过 Context.dev 获取品牌标识、网站截图和实时 DOM 标记，然后塑造成 Google DESIGN.md 文档。

- **域名输入**：输入任意公开域名，自动提取品牌信息
- **Context.dev 驱动**：利用专业网页抓取技术获取完整的品牌标识
- **开源**：代码开放，可以自行部署或定制
- **品牌色提取**：自动识别并命名品牌色彩（如 Apple → Namara Grey、Dark Side of the Moon、Silver Polish）
- **企业级覆盖面**：示例涵盖 Apple、Microsoft、Google、Meta、Tesla、JPMorgan、Netflix 等巨头

#### 独特优势

- 开源可控 —— 可以了解生成逻辑、自行部署
- Context.dev 驱动 —— 抓取质量高，不像简单爬虫那样丢失动态内容
- 品牌色命名 —— 不只是输出 Hex 值，还给颜色起了有意义的名字

#### 适用场景

- 需要了解 DESIGN.md 生成逻辑的开发者和团队
- 企业级项目需要高质量的自动设计提取
- 希望定制生成流程的产品团队

---

### 5. getdesign.md — 首个 DESIGN.md 文件档案馆

**来源**：[VoltAgent 团队](https://github.com/VoltAgent)
**链接**：[getdesign.md](https://getdesign.md)
**类型**：内容档案馆 / 资源库

#### 核心功能

getdesign.md 自称「生态系统中第一个 DESIGN.md 集合」，它不「生成」设计系统，而是**策展和归档**生产级别的 DESIGN.md 文件。

- **71 个 DESIGN.md 文件**：涵盖 AI/LLM 平台、开发者工具、SaaS、设计工具、金融科技、电商、媒体、汽车等类别
- **品牌覆盖极广**：Vercel、Stripe、Figma、Notion、Supabase、Linear、Airbnb、Spotify、Apple、Uber、NVIDIA、BMW、SpaceX 等
- **「生产级」定位**：声称每个文件都有「真正的深度」，不是表面层的提取
- **开源爱好者友好**：GitHub `awesome-design-md` 仓库

#### 分类体系

| 类别 | 数量 | 代表品牌 |
|------|------|----------|
| AI & LLM Platforms | 12 | Claude、Cursor、xAI、Cohere、Mistral |
| Developer Tools & IDEs | 7 | Vercel、Warp、Sentry、Expo |
| Backend, Database & DevOps | 8 | Supabase、MongoDB、ClickHouse |
| Productivity & SaaS | 7 | Notion、Linear、Superhuman、Cal.com |
| Design & Creative Tools | 6 | Figma、Framer、Webflow、Miro |
| Fintech & Crypto | 7 | Stripe、Coinbase、Binance、Revolut |
| E-commerce & Retail | 5 | Shopify、Nike、Starbucks、Meta |
| Media & Consumer Tech | 12 | Spotify、Apple、Netflix、The Verge |
| Automotive | 7 | BMW、Ferrari、Lamborghini、Tesla、Bugatti |

#### 独特优势

- 策展质量高 —— 每个 DESIGN.md 都经过人工/半人工的深度提取
- 覆盖面最广 —— 71 个品牌、9 个行业类别
- 开箱即用 —— 直接下载 DESIGN.md 放入项目，不需要生成步骤

#### 适用场景

- 需要参考成熟品牌的设计系统来构建自己的设计语言
- 快速获取某个行业巨头（如 Stripe、Linear）的设计风格
- 作为 AI 编码代理的「设计系统素材库」

---

### 6. design-md-chrome — Chrome 扩展即开即用

**来源**：[@bergside](https://github.com/bergside)
**链接**：[GitHub: bergside/design-md-chrome](https://github.com/bergside/design-md-chrome)
**类型**：Chrome 浏览器扩展（开源 MIT）

#### 核心功能

这是最轻量的方案 —— 一个 Chrome 扩展，点击即可从当前网页提取设计样式并生成 DESIGN.md 或 SKILL.md 文件。

- **一键提取**：自动读取当前标签页的字体、颜色、间距、圆角、阴影、动效
- **双格式输出**：同时支持生成 DESIGN.md（设计系统文档）和 SKILL.md（代理就绪的技能文件）
- **基于 TypeUI**：采用 TypeUI 的 DESIGN.md 格式扩展，比官方规范更详细
- **零依赖**：安装扩展即可使用，不需要注册、API Key、付费

#### 生成文件结构

| 章节 | 说明 |
|------|------|
| Mission | 设计系统目标定义 |
| Brand | 产品/品牌背景、URL、受众 |
| Style Foundations | 视觉令牌和基础样式 |
| Accessibility | WCAG 2.2 AA 要求和交互约束 |
| Writing Tone | 实现就绪输出的指导基调 |
| Rules: Do / Don't | 允许和禁止的实现模式 |
| Component Rules | 强制交互/状态细节 |
| Quality Gates | 可测试的质量和一致性检查 |

#### 发布者洞察

> @ricouii：*「design-md-chrome 则是 chrome 的扩展适合即开即用。」*

#### 独特优势

- 真正零配置 —— 安装即用，无需注册任何服务
- 本地运行 —— 隐私友好，设计提取在本地完成
- 双格式 —— 同时生成 DESIGN.md（给人看）和 SKILL.md（给 AI 代理用）

#### 适用场景

- 临时需要提取某个网站的设计规范（应急场景）
- 不喜欢注册在线服务，希望完全本地化操作
- 需要快速为 AI 编码代理生成设计技能文件

---

## 资源汇总

### 所有工具链接

| 工具 | 链接 | 类型 |
|------|------|------|
| Refero Styles | [styles.refero.design](https://styles.refero.design) | Web App + MCP |
| Neuform | [neuform.ai](https://neuform.ai) | Web App |
| DesignMD | [designmd.me](https://designmd.me) | Web App |
| designmd.supply | [designmd.supply](https://designmd.supply) | Web App（开源） |
| getdesign.md | [getdesign.md](https://getdesign.md) | 内容档案馆 |
| design-md-chrome | [GitHub](https://github.com/bergside/design-md-chrome) | Chrome 扩展（开源 MIT） |

### 值得关注的人/账号

- **@ricouii** — 原帖作者，网页设计师，探索 AI 和 Vibe Coding。工具箱站点：[uiuxdeck.com](https://uiuxdeck.com)
- **@refero_design** — Refero 官方账号
- **@rob** — Neuform 作者
- **@mengto** — Neuform 联合创作者
- **@crowdlinker** — DesignMD 开发团队
- **@VoltAgent** — getdesign.md 维护团队
- **@bergside** — design-md-chrome 作者

### 相关资源

- **Google DESIGN.md 规范**：[github.com/google-labs-code/design.md](https://github.com/google-labs-code/design.md)（Apache-2.0）
- **TypeUI DESIGN.md 扩展**：[typeui.sh/design-md](https://www.typeui.sh/design-md)
- **awesome-design-md**：[github.com/VoltAgent/awesome-design-md](https://github.com/VoltAgent/awesome-design-md)

---

## 建议使用路径

根据你的需求场景，推荐以下使用路径：

### 🎯 场景一：为 AI 编码代理配置设计系统
1. 先上 **[getdesign.md](https://getdesign.md)** 浏览与你项目风格接近的品牌 DESIGN.md（如 Linear 的极简风、Stripe 的渐变紫）
2. 用 **[Refero Styles](https://styles.refero.design)** 搜索更精准的设计风格，获取 Tailwind/CSS Variables 等工程化输出
3. 将 DESIGN.md 放入项目根目录，AI 编码工具自动识别

### 🎨 场景二：从零设计一个新产品
1. 用 **[Neuform](https://neuform.ai)** 快速生成多个设计方向并 Remix 探索
2. 将满意的设计导出为 DESIGN.md
3. 用 **[design-md-chrome](https://github.com/bergside/design-md-chrome)** 补充提取参考网站的具体设计细节

### 🔧 场景三：快速提取参考网站设计规范
1. 即时需求 → **[design-md-chrome](https://github.com/bergside/design-md-chrome)**（零配置）
2. 批量生成 → **[DesignMD](https://designmd.me)**（成熟引擎，13K+ 生成量）
3. 企业级质量 → **[designmd.supply](https://designmd.supply)**（Context.dev 驱动，开源可控）

### 📚 场景四：设计灵感与研究
1. **[Refero Styles](https://styles.refero.design)** — 按品牌/情绪/色彩搜索，获取设计品味
2. **[getdesign.md](https://getdesign.md)** — 按行业分类浏览，系统了解不同领域的设计语言
3. **[DesignMD Discover](https://designmd.me/discover)** — 浏览社区生成的设计系统

---

## 工具选型决策矩阵

| 决策因素 | 推荐工具 |
|----------|----------|
| 输出最全面（多格式） | Refero Styles |
| 视觉体验最好 | Neuform |
| 零门槛快速试用 | DesignMD（3 次免费）或 design-md-chrome |
| 开源可定制 | designmd.supply 或 design-md-chrome |
| 策展内容最丰富 | getdesign.md（71 个品牌） |
| 与企业 CI/CD 集成 | Refero MCP 或 designmd.supply |
| 纯本地操作 | design-md-chrome |
| AI 代理深度集成 | Refero（MCP）|

---

## 附录：DESIGN.md 快速参考

### 什么是 DESIGN.md？

DESIGN.md 是 Google 推出的开源规范（Apache-2.0），一个文件同时包含：
- **YAML 前置元数据** — 机器可读的设计令牌（颜色、字体、间距等精确值）
- **Markdown 正文** — 人类可读的设计理念和用法说明

### DESIGN.md 示例框架

```yaml
---
version: alpha
name: My Design System
description: A clean, modern design language.
colors:
  primary: "#1A1C1E"
  secondary: "#6C7278"
  tertiary: "#B8422E"
  neutral: "#F7F5F2"
typography:
  h1:
    fontFamily: Public Sans
    fontSize: 3rem
    fontWeight: 700
---
```

### 与 AI 编码工具配合使用

将 DESIGN.md 放在项目根目录后，Cursor、Claude Code、Codex、Windsurf 等 AI 编码工具在生成 UI 时会自动读取并遵循其中的设计规范。这意味着：

- 不需要手动写 CSS 变量
- 不需要沟通「品牌色是什么」
- 不需要每次强调「字体用这个」
- AI 代理自动保持设计一致性

---

*来自hueshadow*
