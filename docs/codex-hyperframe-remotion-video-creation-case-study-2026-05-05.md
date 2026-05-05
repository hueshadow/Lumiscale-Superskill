# Codex + HyperFrame/Remotion 视频创作实战：从零到 Apple 宣传片级出品

> 来源：X/Twitter @Saccc_c  
> 整理时间：2026-05-05  
> 来自翡冷翠

---

## 简介

2026年5月4日，X 博主 **@Saccc_c**（18.1K 关注者，AI Native 创作者）发布了一条引爆技术圈的视频帖子：他用 **Codex + HyperFrame** 的组合，以纯编码的方式制作了一支 Apple 风格的宣传片。不到24小时，视频获得 **8.2万次观看、794次书签、578个喜欢**。

这不是孤例。两天前（5月2日），他还用 **Codex + Remotion** 在不到1小时内制作了一支电影票房排行榜短视频——Codex 负责自动找素材、下载片段，Remotion 负责动画衔接和画面编排。

更值得关注的是：**Claude 官方账号**也在通过 Remotion、HyperFrame 这类工具制作视频内容，累计获得了超过 **1000万次流量（10M+）**。

这标志着一个重要的范式转变：**视频创作正在从「手动剪辑工具」（Premiere/剪映）迁移到「代码驱动视频生成」（Codex + React 视频框架）**。即使是零视频剪辑经验的小白，也能在1小时内产出专业级视频。

---

## 核心工具技术栈

### 1. OpenAI Codex — AI 编程 Agent

Codex 是 OpenAI 推出的命令行 AI 编程助手，能够理解自然语言指令并执行复杂的编码任务。在视频创作场景中，Codex 扮演「导演+执行者」的角色：

- **素材获取**：根据描述自动搜索、下载视频素材和图片资源
- **脚本编写**：理解需求后生成 Remotion/HyperFrame 的视频代码
- **自动化编排**：插件系统支持直接调用 Remotion、HyperFrame 等视频框架

Codex 的插件生态是其核心优势——通过 Remotion 插件和 HyperFrame 插件，用户只需用自然语言描述想要的视频效果，Codex 就会生成完整的可执行代码。

> **发布者原话**："Codex 负责找素材、下载片段，Remotion 负责衔接动画和画面编排。只需要表达清楚目标效果，就能做出完成度还不错的动画成片。"

### 2. Remotion — 用 React 写视频

Remotion 是一个开源框架，允许开发者**用 React 组件的方式编程创建视频**（[remotion-dev/remotion](https://github.com/remotion-dev/remotion)）。

| 指标 | 数据 |
|------|------|
| GitHub Stars | 45.8k |
| Forks | 3.1k |
| 安装方式 | `npx create-video@latest` |
| 技术栈 | React + Node.js |
| 授权 | 特殊商业授权（公司使用需购买） |

**为什么用 React 做视频？**

- **利用 Web 技术栈**：CSS、Canvas、SVG、WebGL 全部可用
- **利用编程能力**：变量、函数、API、数学算法创造新效果
- **利用 React 生态**：可复用组件、热更新、NPM 包生态

**知名案例：**
- **Fireship**（YouTube 知名技术频道）：使用 Remotion 制作技术讲解视频
- **GitHub Unwrapped**：年度回顾个性化视频

### 3. HyperFrame — Codex 视频插件

HyperFrame 是 Codex 生态中的视频创作插件，专注于**高级视频特效和动态画面生成**。

与 Remotion 的关系：
- **Remotion** 更适合「结构化视频」——如数据可视化动画、教程视频、排行榜
- **HyperFrame** 更适合「创意视频」——如宣传片、品牌视频、电影级特效

> **发布者原话**："用纯编码的形式手搓各种视频，真tm的太爽了。Codex + HyperFrame is eating video editors."

---

## 案例演示：@Saccc_c 的两个实战项目

### 案例一：Apple 风格宣传片（Codex + HyperFrame）

**产出**：一段 Apple 风格的品牌宣传片（时长约 1 分 15 秒）

**工作流**：
1. 用自然语言向 Codex 描述想要的视频风格和内容（"Apple 宣传片风格"）
2. Codex 调用 HyperFrame 插件生成视频代码
3. HyperFrame 处理动画、转场、特效
4. 迭代调整——不满意的地方再次用自然语言描述修改需求

**数据表现**：
- 观看量：8.2万
- 书签数：794（说明大量用户收藏了这条内容作为参考）
- 喜欢数：578
- 转帖数：73

**发布者洞察**：@Saccc_c 本人并非专业视频编辑，而是通过 Codex 的编码能力弥补了视频制作经验的不足。"用纯编码的形式手搓各种视频"——这句话揭示了新范式的本质：**视频创作变成了代码编写，门槛从「学会使用复杂编辑软件」降低到「能描述清楚想要什么」**。

### 案例二：电影票房排行榜短视频（Codex + Remotion）

**产出**：一段电影票房排行榜动画短视频（制作时间 < 1 小时）

**工作流**：
1. Codex 自动搜索票房数据、下载相关电影海报/片段
2. Codex 编写 Remotion 代码，定义动画序列和画面编排
3. 排行榜数字从低到高依次出现，带动画转场效果
4. 输出完整视频文件

> **发布者原话**："我一个视频剪辑小白，不到 1h 做出了下面这个电影票房排行榜短视频。视频创作的门槛又一次被拉低了 🤩"

**关键洞察**：这个案例展示了代码驱动视频的核心优势——**数据驱动的自动化**。传统视频编辑需要手动输入每个数字、手动添加动效；而 Remotion 可以直接读取数据源，自动生成排行榜变化动画。这种「数据→视频」的管道化能力是传统剪辑工具无法比拟的。

---

## Claude 官方账号的验证

@Saccc_c 在帖子中提到：**"Claude 官推通过 Remotion、HyperFrame 这类工具制作视频已经撸了至少 10M 流量"**。

这是一个重要的信号：
- Anthropic（Claude 开发者）自己的官方社媒账号也在使用这套工具链
- 10M+ 流量证明了代码驱动视频在社媒传播中的效果
- 官方背书降低了工具链的采用风险

---

## 适用场景矩阵

| 场景 | 推荐工具 | 为什么 |
|------|----------|--------|
| 数据可视化视频（排行榜、财报、年度回顾） | Codex + Remotion | 数据驱动，自动生成动画 |
| 品牌宣传片 / 产品发布视频 | Codex + HyperFrame | 高级特效，电影级画质 |
| 教程 / 技术讲解视频 | Codex + Remotion | 结构化内容，代码示例展示 |
| 社媒短视频（抖音/小红书/Reels） | Codex + HyperFrame | 快节奏特效，吸引眼球 |
| 新闻/资讯类视频 | Codex + Remotion | 自动获取数据，批量生成 |
| 营销广告 | Codex + HyperFrame | 品牌调性，视觉冲击力 |

---

## 对内容创作者的建议

@Saccc_c 在帖子中给出了明确建议：

> "我真心建议所有自媒体人、运营人以及市场人都花时间学一学"

**为什么要学？**

1. **效率革命**：手动剪辑 2 小时的工作 → Codex 5 分钟搞定
2. **门槛降低**：不需要学 Premiere/After Effects，会描述需求即可
3. **质量提升**：编程方式保证了动画一致性、数据准确性、品牌统一性
4. **规模化**：一个脚本可以批量生成 N 个变体视频（不同语言、不同尺寸、不同平台）
5. **差异化竞争**：当大多数人还在手动剪辑时，代码驱动视频产出量和质量都会形成碾压

**学习路径建议：**

```
第1步：安装 Codex CLI → 熟悉基础命令
第2步：用 Codex + Remotion 练手 → 做一个简单的文字动画
第3步：逐步增加复杂度 → 数据图表动画 → 排行榜视频
第4步：尝试 HyperFrame → 品牌宣传片级别出品
```

---

## 资源汇总

### GitHub 仓库

| 项目 | 链接 | Star |
|------|------|------|
| Remotion | https://github.com/remotion-dev/remotion | 45.8k |
| Remotion Showcase | https://remotion.dev/showcase | - |
| Remotion Fireship 案例 | https://github.com/wcandillon/remotion-fireship | - |
| GitHub Unwrapped | https://github.com/remotion-dev/github-unwrapped | - |

### 工具入口

| 工具 | 入口 |
|------|------|
| Codex CLI | https://codex.openai.com |
| Remotion | `npx create-video@latest` |
| Remotion 文档 | https://remotion.dev/docs |
| Remotion API | https://remotion.dev/api |

### 值得关注的人

| 账号 | 简介 |
|------|------|
| @Saccc_c | AI Native 创作者，Codex 视频创作先驱，18.1K followers |
| @remotion | Remotion 官方账号 |
| Claude 官方账号 | 也在使用 Remotion/HyperFrame 制作视频 |

---

## 快速上手指南

**最快开始**：安装 Codex CLI，然后对 Codex 说：
> "帮我用 Remotion 做一个 15 秒的视频，内容是三个数字从小到大依次弹出，最后显示一个标题"

**最全面参考**：访问 [Remotion Showcase](https://remotion.dev/showcase) 查看所有案例和源代码。

---

*来自翡冷翠*
