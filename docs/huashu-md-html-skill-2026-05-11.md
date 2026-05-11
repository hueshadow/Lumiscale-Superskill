# huashu-md-html：花叔开源的 md/html/docx 多向转换流水线 — 完整解析

> 来源：[@AlchainHust on X](https://x.com/alchainhust/status/2053138946217930842) | GitHub: [alchaincyf/huashu-md-html](https://github.com/alchaincyf/huashu-md-html)
> 作者：花叔（Huasheng）
> 整理时间：2026-05-11
> 来自hueshadow

---

## 背景：一场关于 Markdown vs HTML 的争论

2026 年 5 月 9 日，Claude Code 团队的 **Thariq** 发了一篇爆文，标题是：**《HTML 是新的 Markdown》**。他说自己几乎不再写 `.md` 文件了，转而让 Claude Code 直接生成 HTML。这篇文章迅速在 AI 开发者圈引发激烈讨论 ——「md 过时了吗？」「HTML 更适合 AI 消费和展示吗？」

花叔（@AlchainHust）站了出来，用一句话终结了争论：

> **「别吵了！我给你们开源了一个 skill，随意转换 md 和 HTML。」**

他开源了 **[huashu-md-html](https://github.com/alchaincyf/huashu-md-html)**，一个将 md、html、docx 彻底打通的多向转换流水线。核心理念只用一句话：

> **「md 是源代码，html / docx 是产物。」**

---

## 为什么值得关注（核心价值主张）

### 解决什么问题

AI 时代，写作和分发首次解耦了。写作发生在 markdown（可 diff、AI 友好、版本可控），但分发需要不同形态 —— 精美网页、出版社审校稿、归档源文件。传统工具只能处理单向转换，而 huashu-md-html 打通了四条路径：

1. **万物 → md**：PDF、DOCX、PPTX、网页、YouTube、图片、音频……全部变成干净的 markdown
2. **md → 精美 html**：4 套出版社级主题，一键套版或 AI 定制
3. **html → md**：已发布的博客/网页无损拉回项目源
4. **md → 精美 docx**：出版社审校、投稿、纸质书定稿一条命令

### 独特价值点

这不是普通的格式转换工具，而是花叔自己在 AI 编程和内容创作中的**实战方法论产物**：

- **4 套 html 主题全部过了「反 AI slop」检查清单**：没有紫渐变、没有 emoji 当图标、没有 #0D1117 深蓝底，配色克制，有出版社品位
- **跨 Agent 通用**：Claude Code、Cursor、Codex、OpenClaw、Hermes 都能装（通过 skills.sh 生态）
- **能力 4（md → docx）是真正的出版终点**：pandoc 默认 md→docx 只能给 AI 看，不能给编辑改稿；这个脚本内置了出版社级排版预设 —— 封面、目录、页眉页脚、章节分页、代码块左侧色条

### 看完能获得什么

- 一个可以直接上手的 **md/html/docx 全链路工作流**
- 4 套可直接使用的 **html 排版主题**（article / report / reading / interactive）
- 一套**出版社可审校的 docx 生成方案**
- 对「AI 时代的文档工程」设计哲学的系统理解

---

## 四大能力详解

| 能力 | 入口脚本 | 底层工具 | 一句话说明 |
|------|---------|---------|-----------|
| **能力 1：万物 → md** | `scripts/any_to_md.py` | Microsoft markitdown | 20+ 格式输入 → 干净 md |
| **能力 2：md → 精美 html** | `scripts/md_to_html.py` | Pandoc + 4 套自调主题 | md 源 → 出版级网页（兜底 / 设计师双模式） |
| **能力 3：html → md** | `scripts/html_to_md.py` | html-to-markdown + trafilatura | 已发布网页拉回项目源 |
| **能力 4：md → 精美 docx** | `scripts/md_to_docx.py` | python-docx + 出版社排版预设 | 单文件或整本书 → 编辑可审校的 docx |

---

### 能力 1：万物 → md

支持 20+ 种格式的输入转 md，覆盖你遇到的几乎所有文件类型：

**支持的格式**：PDF、DOCX、PPTX、XLSX、HTML、CSV、JSON、XML、图片（EXIF / 可选 LLM 描述）、音频（可选语音转写）、YouTube URL（自动抓字幕）、普通网页 URL（带 YAML frontmatter）、EPub、ZIP（递归解包）、Outlook 邮件（.msg）

```bash
# 基本用法
python scripts/any_to_md.py input.pdf
python scripts/any_to_md.py input.docx -o output.md
python scripts/any_to_md.py "https://www.youtube.com/watch?v=xxx"

# 结构化网页保留 metadata + 标题层级 + 链接
python scripts/any_to_md.py "https://learn.microsoft.com/en-us/docs" -o doc.md

# 启用 LLM 图片描述
python scripts/any_to_md.py photo.jpg --llm-describe
```

**已知坑（作者已在文档中诚实标注）**：
- 扫描 PDF 不做 OCR，需要挂 LLM client 或 Azure Doc Intelligence
- 复杂表格（合并单元格/嵌套）会丢失语义
- PPTX 只保留文本+备注，动画排版完全丢
- 输出为 LLM 消费设计，给人读要再过一道排版

**URL 输入的双路径判断**（重要！）：

| 页面类型 | 走哪个能力 | 原因 |
|---------|-----------|------|
| **结构化页面**（产品详情、技术文档、API doc、证书页） | 能力 1（markitdown） | 保留 metadata、字段值、链接、标题层级 |
| **正文类页面**（博客、新闻、Essay、长文） | 能力 3（trafilatura） | 自动去导航/侧栏/广告，只留正文 |

> **判断捷径**：URL 里的内容是「读」的还是「查」的？读 → 能力 3（去噪），查 → 能力 1（保信息）。

---

### 能力 2：md → 精美 html

这个能力是花叔设计哲学的集中体现。它有两种模式：

| 模式 | 耗时 | Token | 何时用 |
|------|------|-------|--------|
| **兜底模式**（4 主题套版） | 5 秒 | 不耗 | 已知主题、要快 — `--theme xxx` 一条命令出活 |
| **设计师模式**（AI 注入定制） | 需要 | 耗 | AI 读懂内容 → 推荐 3 个方向 → 定制视觉表达 |

**4 套 html 主题**：

| 主题 | 哲学锚点 | 适合场景 |
|------|---------|---------|
| **article**（默认）| Tufte CSS 启发 · Pentagram 式信息建筑 | essay、博客、深度阅读、独立文章 |
| **report** | 出版社白皮书风 · 多表格密度型 | 技术报告、调研、白皮书、产品文档 |
| **reading** | Medium 风极简 · 单栏窄体大字 | 公众号转接、纯阅读、轻量分发 |
| **interactive** | 长文档导航型 · 折叠 + 目录 + 边栏 | 橙皮书章节、技术书籍、长教程 |

每套主题都是**自包含单 CSS**，HTML 打开即用，不依赖外部 CDN。

```bash
# 默认 article 模板
python scripts/md_to_html.py article.md

# 选模板
python scripts/md_to_html.py report.md --theme report    # 宽体多表格
python scripts/md_to_html.py article.md --theme reading  # Medium 极简
python scripts/md_to_html.py book.md --theme interactive # 折叠目录+边栏

# 图片处理
python scripts/md_to_html.py input.md --inline-images    # base64 嵌入（自包含单文件）
```

**排版底线（所有主题共享）**：

```
正文字体（中文）：PingFang SC, Source Han Serif, Noto Serif CJK
正文字体（英文）：Inter, IBM Plex Sans, et-book
代码字体：JetBrains Mono, Fira Code
行高（中文）：1.75 - 1.85
行高（英文）：1.6
字号（桌面）：17 - 18px
最大宽度（文章）：680 - 720px
最大宽度（报告）：760 - 820px
代码块底色：#F6F8FA（浅）/ #1F2428（深）
引用块：左 4px 色条 + 浅灰底
```

**禁用清单**：紫渐变、赛博霓虹、`#0D1117` 深蓝底、Comic Sans、emoji 作正式图标。

---

### 能力 3：html → md

反向归档能力 —— 把已发布的 html/网页拉回 markdown 源。

**最适合**：博客文章、新闻报道、Essay、公众号长文 —— 任何「正文是产品、其他都是噪声」的页面。会自动丢弃导航、侧栏、相关推荐、广告，只保留正文。

**不适合**：产品页、技术文档、API doc —— 这些走能力 1（markitdown），因为 trafilatura 会丢失字段值和层级结构。

```bash
# 本地 HTML 文件
python scripts/html_to_md.py input.html

# 博客/新闻 URL（自动 trafilatura 提取正文）
python scripts/html_to_md.py "https://example.com/article"

# 精细控制
python scripts/html_to_md.py input.html --bullets="-" --heading-style=atx --strip="script,style,nav,footer"
```

---

### 能力 4：md → 精美 docx ⭐

这是花叔最值得关注的能力创新。为什么单独做能力 4？

> pandoc 自带的 `md → docx` 默认 Calibri、无表格样式、无封面、章节首页平淡 —— 能给 AI 看，**不能给出版社编辑改稿**。

能力 4 内置了出版社级排版预设：

| 元素 | 预设 |
|------|------|
| 页面规格 | 大 32 开（176×240mm）或 A4 |
| 中文字体 | 思源宋体 CN（回退 Songti SC / PingFang SC） |
| 英文字体 | Georgia（衬线） |
| 代码字体 | JetBrains Mono（回退 Menlo） |
| 章标题（H1） | 24pt 黑色加粗 + 橙色底分隔线 + 上方章号小标 |
| 节标题（H2） | 17pt 黑色加粗 |
| 引用块 | 按 emoji 自动配色：💡 琥珀 / ✅ 青色 / ⚠️ 玫红 |
| 代码块 | 浅灰底（F5F5F0）+ 橙色左 16pt 色边 |
| 表格 | 表头底色 + 浅灰边框 + 居中对齐 |
| 配图 | 居中嵌入 + 灰色斜体图说 |
| 页眉 | 右对齐小字号书名（斜体灰色） |
| 页脚 | 居中自动页码 |

```bash
# 单文件转换
python3 scripts/md_to_docx.py article.md

# 整本书模式（封面 + 目录 + 页眉页脚 + 章节分页）
python3 scripts/md_to_docx.py ch*.md postscript.md appendix.md --book \
    --title "图解 Agent Skills" \
    --subtitle "让 AI 记住你的工作方式" \
    --author "花叔" \
    --images-dir ./images \
    -o book.docx

# 页面规格切换
python3 scripts/md_to_docx.py article.md --page-size a4   # A4 报告
python3 scripts/md_to_docx.py book.md --page-size book    # 大 32 开（纸质书）
```

**实战验证**：花叔用此脚本生成了《图解 Agent Skills》158 页出版社审校稿（9 章 + 后记 + 附录 + 57 张配图），一条命令搞定。

---

## 一条龙工作流（典型场景组合）

```bash
# 场景 1：PDF 白皮书 → 精美阅读 html
python scripts/any_to_md.py whitepaper.pdf -o whitepaper.md
python scripts/md_to_html.py whitepaper.md --theme report -o whitepaper.html

# 场景 2：YouTube 视频 → 文章博客
python scripts/any_to_md.py "https://youtube.com/watch?v=xxx" -o video.md
# 编辑 video.md...
python scripts/md_to_html.py video.md --theme article -o blog.html

# 场景 3：归档已发布的博客 → 项目源 md
python scripts/html_to_md.py "https://example.com/blog/article" -o article.md

# 场景 4：PDF 论文 → docx 投稿（能力 1 → 能力 4）
python scripts/any_to_md.py paper.pdf -o paper.md
# 编辑 paper.md 修正格式...
python scripts/md_to_docx.py paper.md --page-size a4 -o paper.docx

# 场景 5：橙皮书 md → 出版社审校 docx
python scripts/md_to_docx.py ch*.md postscript.md appendix.md --book \
    --title "书名" --author "花叔" --subtitle "副标题" \
    --images-dir ./images -o 出版社审校版.docx
```

---

## 设计哲学：为什么值得认真看

这个 skill 的存在源于一个深刻洞察：

> **AI 时代，文档的「生产格式」和「消费格式」第一次真正解耦了。**

大多数「转 X 到 Y」工具优化的是「转换保真度」。这个 skill 优化的是**写作者的循环**：

- **一份 md 是源** —— 所有创作和编辑都在 md 里，可 diff、AI 友好、版本可控
- **多套 html 是产物** —— 按场景挑主题，渲染精美 html，不依赖 CDN、打开即用
- **来回往返不丢结构** —— 把已发布的博客拉回项目源，把别人的好内容归档成 md
- **docx 是出版终点** —— 给人类编辑/出版社用的专业格式，不是给 AI 看的

继承自 [huashu-design](https://github.com/alchaincyf/huashu-design) 的反 AI slop 审美底线 —— 4 套主题各有一个克制的强调色和一个出版级的排印签名。

---

## 安装与启动

```bash
# 一行安装（跨 agent 通用）
npx skills add alchaincyf/huashu-md-html

# 依赖安装
python3 -m pip install 'markitdown[all]' html-to-markdown trafilatura python-docx Pillow
brew install pandoc
```

然后在 Claude Code / Cursor / Codex / Hermes 里直接说话：

- 「这个 PDF 转成 md」
- 「把这篇 md 做成精美 html，用 article 主题」
- 「这个博客 URL 转回 md，去掉导航和侧栏」
- 「把这些章节 md 做成出版社可审校的 docx」

---

## 关键注意事项

1. **URL 双路径判断**：结构化页面走能力 1，正文类页面走能力 3。判断方法：「读的」还是「查的」？
2. **macOS Python 环境陷阱**：`pip` 和 `python3` 可能指向不同版本。安装依赖必须用 `python3 -m pip install`，不要直接用 `pip install`
3. **Pandoc 3.0+**：推荐安装最新版 pandoc
4. **docx 是给人的**：给出版社/编辑/投稿系统用能力 4。html 适合自己分享，不适合编辑改稿
5. **输出为 LLM 消费设计**（能力 1）：markitdown 的 md 输出优先保证 LLM 可消费性，给人读要再过一道排版

---

## 关于作者：花叔（Huasheng）

花叔是 AI Native Coder、独立开发者、AI 自媒体博主，全平台累计粉丝 30 万+。**自称「完全不会编程」**，但用 Cursor 不到半年完成：

- 10+ 个网站
- 5+ Chrome 插件
- 4 个 iOS app
- 2 个小程序
- 10+ 本地自动化 Python 脚本
- 1 个 VSCode 插件

**代表作**：

| 作品 | 说明 |
|------|------|
| **小猫补光灯** | App Store 付费榜 Top 1 |
| **《一本书玩转 DeepSeek》** | AI 入门畅销书 |
| **nuwa-skill** | GitHub 12k+ stars，AI 编程 skill 集合 |
| **huashu-design** | 反 AI slop 的排版设计语言 |

**关注花叔**：

| 平台 | 链接 |
|------|------|
| X / Twitter | [@AlchainHust](https://x.com/AlchainHust) |
| B 站 | [花叔](https://space.bilibili.com/14097567) |
| YouTube | [花叔](https://www.youtube.com/@Alchain) |
| 小红书 | [花叔](https://www.xiaohongshu.com/user/profile/5abc6f17e8ac2b109179dfdf) |
| 官网 | [huasheng.ai](https://www.huasheng.ai/) |
| 开发者 Hub | [bookai.top](https://bookai.top) |

---

## 总结

huashu-md-html 不仅仅是又一个格式转换工具，而是花叔对 **「AI 时代的文档工程」** 的系统性回答。它的价值在于：

1. **四能力闭环**：md 始终是源，html/docx 是不同场景的产物
2. **反 AI slop 审美**：产出的 html 像出版社做的，不像 SaaS 落地页
3. **出版社级 docx**：真正能交付给人类编辑/出版社的专业格式
4. **跨 Agent 生态**：通过 skills.sh 实现 Claude Code / Cursor / Codex / Hermes 通用
5. **生产验证**：作者自己的 158 页书就是用这套流水线生成的

对于任何一个用 markdown 写作但需要在多端分发的创作者来说，这个 skill 提供了一个优雅的「md 生产，多端消费」方法论和即用工具链。

---

*来自hueshadow*
