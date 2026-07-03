# 女娲.skill 人物 Skill 合集 - 完整整理

> 来源：X/Twitter [@eastweb3eth](https://x.com/eastweb3eth/status/2072873659698700343)
> 整理时间：2026-07-03
> 来自hueshadow

---

## 简介

[@eastweb3eth](https://x.com/eastweb3eth)（Jealousy 尼卡，KITE AI）分享了使用「女娲.skill」蒸馏出的三款人物 Skill。女娲.skill 是一个开源工具，能像「女娲造人」一样将大模型赋予特定人物的「人性」——输入任何人名，自动完成调研、提炼、验证全流程，输出可运行的思维框架（Skill）。

这三款 Skill 分别蒸馏了 Paul Graham（创业/写作/产品）、Andrej Karpathy（AI/工程/教育）和张一鸣（产品/组织/全球化）的认知操作系统。它们不是语录合集，而是包含心智模型、决策启发式和表达 DNA 的完整思维框架。

---

## 内容清单总览

| 序号 | 人物 | 领域 | GitHub | Stars | Forks | 状态 |
|------|------|------|--------|-------|-------|------|
| 1 | Paul Graham | 创业/写作/产品/人生哲学 | [paul-graham-skill](https://github.com/alchaincyf/paul-graham-skill) | 77 | 24 | 已发布 |
| 2 | Andrej Karpathy | AI/工程/教育/开源 | [karpathy-skill](https://github.com/alchaincyf/karpathy-skill) | 252 | 78 | 已发布 |
| 3 | 张一鸣 | 产品/组织/全球化/人才 | 待发布 | - | - | 预告中 |

---

## 核心工具：女娲.skill

**GitHub**：[alchaincyf/nuwa-skill](https://github.com/alchaincyf/nuwa-skill)
**数据表现**：⭐ 26,700+ | Fork 3,800+

> 「你想蒸馏的下一个员工，何必是同事。蒸馏任何人的思维方式——心智模型、决策启发式、表达DNA。」

女娲.skill 是一个基于 Agent Skills 开放协议的思维蒸馏工具。它的核心能力：

- **输入**：任何人名（乔布斯、芒格、费曼、马斯克等）
- **输出**：完整的 SKILL.md 文件，包含心智模型、决策启发式、表达 DNA
- **流程**：自动完成调研 → 提炼 → 验证全流程
- **兼容**：支持 Claude Code、Codex、Cursor、OpenClaw、Hermes Agent 等 50+ runtime

安装方式：
```bash
npx skills add alchaincyf/nuwa-skill
```

---

## 详细内容

### 1. Paul Graham Skill — 创业/写作/产品/人生哲学

**GitHub**：[alchaincyf/paul-graham-skill](https://github.com/alchaincyf/paul-graham-skill)
**数据表现**：⭐ 77 | Fork 24
**安装**：`npx skills add alchaincyf/paul-graham-skill`

#### 蒸馏来源

基于 paulgraham.com 200+ 篇 essays、12 个播客/访谈、Twitter/X 分析、7 位核心批评者视角和完整人生时间线的深度调研。

#### 5 个核心心智模型

| 模型 | 一句话 | 来源 |
|------|--------|------|
| **Writing = Thinking** | 写作不是记录想法，写作本身就是思考过程 | Putting Ideas into Words、Writes and Write-Nots、30年essay实践 |
| **品味即认知工具** | 品味不是主观偏好，是可训练的判断力，让你在信息不完整时做更好的决策 | Blub Paradox、Viaweb用Lisp的竞争优势、AI时代「品味比执行力重要」 |
| **迭代发现** | 好东西不是设计出来的，是做的过程中发现的 | Viaweb从画廊网站pivot到在线商店、YC batch模式的意外诞生 |
| **超线性回报** | 某些领域投入翻倍产出四倍，找到这些领域然后持续投入 | 1%周增长 vs 5%周增长的四年差距、知识积累的复利效应 |
| **独立思考即生存** | 大多数人不是在想，是在想别人告诉他们的东西 | What You Can't Say、Keep Your Identity Small、最好的startup ideas看起来像坏主意 |

#### 8 条决策启发式

1. **Fund People Not Ideas** — 早期创始人品质比idea重要100倍。看determination、flexibility、imagination、naughtiness
2. **Make Something People Want** — YC的motto，不是做你觉得酷的，做用户真正想要的
3. **Do Things That Don't Scale** — 早期拥抱手工方式，用手摇曲柄启动引擎
4. **Default Alive or Default Dead?** — 随时知道公司状态，招人太快是融资后的头号杀手
5. **Stay Upwind** — 像滑翔机一样保持上风处，做有趣的事并保持选项开放
6. **Keep Your Identity Small** — 每多贴一个标签你在那个话题上就变蠢一点
7. **Maker's Schedule > Manager's Schedule** — 一个会议就能毁掉整个下午
8. **Am I Surprising Myself?** — 创作中有没有发现自己不知道的东西？没有就是在重复

#### 表达 DNA

- **句式**：短句为主，简单词表达 sophisticated ideas。大量使用 "you" 直接对读者说话
- **开篇**：个人轶事 / 常识+转折 / 直接陈述大胆论点 / 自问自答。绝不用定义开头
- **高频模板**："The way to X is not to Y. It's to Z." / "Most people don't realize..." / "It turns out..."
- **节奏**：探索式展开，不是结论先行。开放式结尾，不写总结段落
- **幽默**：学者式冷幽默，密度低。类比讽刺、冷面陈述、自嘲
- **确定性**：事实层面果断，推断层面谨慎（"I suspect", "I may be wrong"）

#### 内在矛盾（保留真实复杂性）

- Mean People Fail vs Jobs/Bezos的成功
- Founder Mode vs 自己2014年就退出YC
- Move to a Startup Hub vs 搬到英格兰乡下
- 提倡开放思维 vs Delve事件中的doubled down

#### 使用方式

装好后告诉 agent：
```
> 用PG的视角帮我分析这个创业方向
> Paul Graham会怎么看AI写作工具的前景？
> 切换到PG，我在纠结要不要辞职创业
```

---

### 2. Andrej Karpathy Skill — AI/工程/教育/开源

**GitHub**：[alchaincyf/karpathy-skill](https://github.com/alchaincyf/karpathy-skill)
**数据表现**：⭐ 252 | Fork 78
**安装**：`npx skills add alchaincyf/karpathy-skill`

#### 蒸馏来源

基于 20+ 篇博文（Software 2.0、Recipe for Training Neural Networks 等）、Lex Fridman / Dwarkesh Patel 等 16 段深度访谈、100+ 条 X 帖子、GitHub 项目 README 深度调研。

#### 6 个核心心智模型

| 模型 | 一句话 | 来源 |
|------|--------|------|
| **Software X.0 范式思维** | 编程语言在历史上只发生过两次根本性变化，我们正处于第三次 | Software 2.0博文(2017)、YC演讲(2025) |
| **构建即理解** | 理解的终极检验，是能否用最少的代码从零重建它 | nanoGPT(750行)、micrograd(100行)、费曼传统 |
| **LLM = 召唤的幽灵** | LLM不是你训练出来的动物，是你从互联网数据中召唤出来的人类思维幽灵 | YC演讲(2025)、Dream Machine推文 |
| **March of Nines** | 从90%到99.9%的工程爬坡，比从0到90%还要难 | Tesla AI Day、5年自动驾驶工程经验 |
| **锯齿状智能** | LLM的能力分布是锯齿状的——某些维度超人，某些维度犯蠢，没有规律 | Dwarkesh访谈(2025) |
| **Iron Man套装 > Iron Man机器人** | 构建AI应该给人穿上套装，而不是造一个替代人的机器人 | YC AI Startup School(2025) |

#### 8 条决策启发式

1. **时间轴拉长批评** — 不直接否定，把时间轴拉长
2. **从零构建验证** — 能用200行代码重建核心吗？
3. **数据飞轮优先** — 哪个方案能积累最多可复用数据
4. **imo标记主张** — 划清验证过的 vs 推断的边界
5. **Don't be a hero** — 遇到复杂问题，先用最简单的方法
6. **先看数据再训练** — 第一步不是碰模型代码，是检查数据
7. **补充语境而非认错** — 面对批评先解释被误读的地方
8. **在关键时刻参与** — 问「这是技术最关键的节点吗」而非「这个机构最大吗」

#### 表达 DNA

- **词汇**：朴素动词（gobbled up、chewing through、terraform）、精确参数+口语并存（3e-4、hands down）、互联网语气（imo、lol、skill issue）
- **句式**：短句独立成段（Strap in. / Don't be a hero. / I'm sorry.）、先震惊后解释、先接受通俗理解再逻辑反转
- **节奏**：RNN博客结构——先展示惊人结果再解释原理；时间轴压缩或拉长
- **确定性**：亲身验证过的斩钉截铁，预测类刻意留白（I have a very wide distribution here）

#### 2 对内在张力

- **Vibe Coding vs 构建式理解**：他一方面坚信从零构建，另一方面公开倡导 vibe coding
- **AGI悲观时间线 vs 热情使用AI工具**：说AGI还需10-15年，同时80%依赖AI Agent编程

#### 使用方式

装好后告诉 agent：
```
> 用Karpathy的视角帮我评估这个AI产品的可靠性
> Karpathy会怎么看vibe coding的未来？
> 切换到Karpathy，我想聊聊学习方法
```

---

### 3. 张一鸣 Skill — 产品/组织/全球化/人才

**状态**：⚠️ 预告中，GitHub 仓库尚未创建（`alchaincyf/zhangyiming-skill` 返回 404）

**预告领域**：产品、组织、全球化、人才

根据原帖图片信息，张一鸣 Skill 将覆盖字节跳动创始人的核心思维框架。具体内容待仓库发布后补充。

---

## 资源汇总

### 所有 GitHub 仓库

| 项目 | 链接 | Stars | 简介 |
|------|------|-------|------|
| 女娲.skill | [alchaincyf/nuwa-skill](https://github.com/alchaincyf/nuwa-skill) | 26.7k | 思维蒸馏工具——蒸馏任何人的思维方式 |
| Paul Graham Skill | [alchaincyf/paul-graham-skill](https://github.com/alchaincyf/paul-graham-skill) | 77 | PG的认知操作系统 |
| Karpathy Skill | [alchaincyf/karpathy-skill](https://github.com/alchaincyf/karpathy-skill) | 252 | Karpathy的认知操作系统 |

### 安装命令速查

```bash
# 女娲.skill（蒸馏工具）
npx skills add alchaincyf/nuwa-skill

# Paul Graham 思维框架
npx skills add alchaincyf/paul-graham-skill

# Andrej Karpathy 思维框架
npx skills add alchaincyf/karpathy-skill
```

### 值得关注的人/账号

- **@eastweb3eth**（Jealousy 尼卡）— KITE AI，女娲.skill 作者，持续发布蒸馏 Skill
- **@alchaincyf**（花叔）— 女娲.skill 的 GitHub 组织维护者
- **@paulg** — Paul Graham 本人，YC 创始人
- **@karpathy** — Andrej Karpathy 本人，Eureka Labs 创始人

---

## 使用场景速查

| 如果你需要... | 优先使用... |
|--------------|------------|
| 创业方向评估、产品决策 | Paul Graham Skill |
| AI 技术可靠性分析、学习方法 | Karpathy Skill |
| 组织管理、全球化战略 | 张一鸣 Skill（待发布） |
| 蒸馏自己关注的人物 | 女娲.skill |

---

## 分析洞察

### 1. 为什么这个合集值得关注

这不是简单的「名人语录合集」。女娲.skill 的蒸馏方法论有三个关键差异：

- **可运行性**：输出的是 SKILL.md 文件，可直接被 AI agent 加载执行，不是静态文本
- **系统性**：每个 Skill 包含心智模型 + 决策启发式 + 表达 DNA，形成完整的认知操作系统
- **诚实性**：保留了人物的内在矛盾和盲区（如 PG 的 Delve 事件、Karpathy 的 vibe coding vs 构建式理解的张力）

### 2. 传播策略分析

- **数据表现**：原帖 68 likes、22 条回复，引用帖（女娲介绍）93 likes、57 回复、10 转发
- **传播逻辑**：用「女娲造人」的比喻降低理解门槛，用具体人物（PG/Karpathy/张一鸣）作为锚点吸引不同圈层
- **社区效应**：女娲.skill 本身 26.7k stars，已形成社区生态（COMMUNITY.md 收录社区贡献的 Skill）

### 3. 技术趋势

Agent Skills 正在成为一个开放标准（agentskills.io），支持 50+ runtime。女娲.skill 是这个生态中「思维蒸馏」方向的标杆项目。将人物思维框架化为可加载的 Skill，代表了 AI agent 从「工具」到「思维伙伴」的进化方向。

---

## 延伸阅读

- 女娲.skill 社区索引：[COMMUNITY.md](https://github.com/alchaincyf/nuwa-skill/blob/main/COMMUNITY.md)
- Agent Skills 标准：[agentskills.io](https://agentskills.io)
- Paul Graham 博客：[paulgraham.com](https://paulgraham.com)
- Karpathy 博客：[karpathy.github.io](https://karpathy.github.io)

---

*来自hueshadow*
