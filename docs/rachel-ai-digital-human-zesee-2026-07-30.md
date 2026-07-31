# Rachel 的 AI 分身上线｜数字人口播实战（MiniMax × HeyGen × Codex）- 完整整理

> 来源：X/Twitter [@Zesee](https://x.com/Zesee/status/2082848456985497901)  
> 主帖：https://x.com/Zesee/status/2082848456985497901  
> 引用长文：https://x.com/Zesee/status/2077723280534851786（X Article《99% 的人没看出来的数字人口播实战攻略》）  
> 整理时间：2026-07-31  
> 来自hueshadow

---

## 简介

@Zesee（Rachel🥥）发布「**Rachel 的 AI 分身上线**」竖/横屏演示，并说明后续会给分身新开抖音号，向观众征询形象状态反馈。该帖**引用**了她此前的 X Article 长文，把数字人口播完整链路沉淀为可复用的 **Codex Skill**。

核心分工一句话：

> **MiniMax 管声音克隆与 TTS · HeyGen 管画面口型表情 · Codex Skill 管检查、样片门禁、状态与风控**

本文合并整理：

1. 2026-07-30 分身上线 showcase 帖 + 本地归档视频  
2. 2026-07-16 数字人口播实战攻略（Article 全文结构）  
3. 公开 GitHub Skill 仓库与可执行 checklist  

---

## 一、主帖概要（AI 分身上线）

| 项 | 内容 |
|----|------|
| 作者 | Rachel🥥（@Zesee） |
| 简介 | 00 年｜上交 × 帝国理工｜AI Spark 创始人｜前微软 & 亚马逊 PM｜AI 使用干货与商业化｜抖音/小红书：Rachel的AI使用日记 |
| 地区 | Hong Kong |
| 粉丝（抓取时） | 约 15,064 |
| 发布时间 | 2026-07-30 15:19 UTC |
| 形式 | 单帖 + 视频 + Quote 自己的 X Article |
| 语言 | 中文 |

### 原帖全文

```
Rachel的AI分身上线
后续会给她新开一个抖音号
大家觉得形象状态怎么样🤓
```

### 传播数据（抓取时）

| 指标 | 主帖（分身上线） | 引用 Article 帖 |
|------|------------------|-----------------|
| Views | ~27,941 | ~511,476 |
| Likes | 218 | 1,149 |
| Bookmarks | 265 | 2,409 |
| Reposts | 33 | 199 |
| Replies | 25 | 53 |
| Quotes | 4 | 16 |

读法：

- 主帖 **书签 > 赞**（265 vs 218），更像「存起来看做法 / 关注后续账号」  
- 引用长文帖书签极高（2409），说明 **可复用流程** 才是真正被收藏的资产  
- 主帖是产品/IP 亮相；长文是方法论沉淀

### 演示视频规格

| 项 | 值 |
|----|-----|
| 时长 | 约 69.7 秒 |
| 原片最高清 | 3836 × 2160（约 4K 级横屏） |
| 本地归档 | 1278 × 720 MP4（约 5.7MB，便于仓库推送） |
| 媒体 ID | 2082847742951317504 |

本地路径：

- 视频：`assets/videos/rachel-ai-digital-human-zesee-2026-07-30.mp4`
- 封面：`assets/videos/rachel-ai-digital-human-zesee-2026-07-30-thumb.jpg`

原帖 CDN 多码率（需重下更高清时用）：

| 分辨率 | 约码率 |
|--------|--------|
| 478×270 | 256 kbps |
| 638×360 | 832 kbps |
| 1278×720 | 2.2 Mbps（已归档） |
| 1918×1080 | 10.4 Mbps（可选，体积较大） |
| 3836×2160 | 25.1 Mbps（原帖最高清，体积大，未入库） |

### Showcase 解读（差异化价值）

这条不是纯教程钩子，而是 **IP 数字化上线公告**：

1. **人物 IP 固化**：名字直接叫「Rachel 的 AI 分身」——数字人不是一次性 demo，是账号资产  
2. **渠道预告**：明确「后续新开抖音号」——完成「模型能力 → 内容账号」闭环  
3. **社交确认**：问「形象状态怎么样」——用评论做形象 QA / 调性校准  
4. **方法论背书**：Quote 自己两周前的 Article + Skill，证明分身背后有工程化流水线，不是偶然一条假脸视频  

若你要抄作业：先有可复用生产 Skill，再发「分身上线」——收藏与信任会叠在方法论文档上，而不是单条炫技。

---

## 二、引用长文：99% 的人没看出来的数字人口播实战攻略

> Article 标题：99% 的人没看出来的数字人口播实战攻略  
> Article 帖：https://x.com/Zesee/status/2077723280534851786  
> 发布时间：2026-07-16  
> GitHub：https://github.com/Jingyi-Wu-Richael/rachel-digital-human-production  

### 开场动机

作者发过一条数字人讲 FDE 的口播视频，很多人第一反应不是问工具，而是**不相信这是数字人**。于是把整条流程做成可复用 Codex Skill 并开源。

### 最终工作流（总览）

```
素材检查
  → MiniMax 生成配音
  → HeyGen 15 秒样片
  → 人工确认
  → HeyGen 完整版
  → 下载验片
  → 状态归档
```

**适用场景**：知识口播、短视频批量生产、课程讲解、产品介绍、多语言内容、固定 IP 数字人账号。

---

### 1. 链路怎么分工

核心：**声音和画面拆开**。

| 组件 | 职责 |
|------|------|
| MiniMax | 声音克隆 + TTS |
| HeyGen | 人像驱动、口型、表情、动作 |
| Codex | 检查素材、调用流程、记录状态、控制风险 |

完整步骤：

1. 准备真人录音，用 MiniMax 海外版克隆声音  
2. 文案 → MiniMax TTS → 克隆音色 MP3  
3. 准备一张清晰正面人像  
4. 人像 + MiniMax MP3 上传 HeyGen  
5. **先生成 15 秒样片**，确认后再生成完整视频  

#### 最容易犯的错（作者强调）

声音已经由 MiniMax 克隆完成，却又让 HeyGen **重新配音**。

若目标是保留 MiniMax 克隆音色：

- 应把 MiniMax 生成的音频上传到 HeyGen，用该音频驱动画面  
- **不要**切回 HeyGen 的 `script + voice_id` 方案  
- 否则声音相似度会被覆盖  

---

### 2. HeyGen 与 MiniMax 模式怎么选

#### HeyGen

第一次建议直接用 **Image-to-Video**（API Key），约 **2 分钟视频 ~$2**。

优点：轻——不必一开始就训练 Avatar；上传人像 + 音频即可快速看口型、表情、脸部稳定性、构图。

建议：

| 阶段 | 选择 |
|------|------|
| 单条测试 | Image-to-Video |
| 固定账号长期生产 | 再做 Photo Avatar |
| 未验证前 | 不要急着训练 Avatar，测试越轻越好 |

#### MiniMax

| 目标 | 建议 |
|------|------|
| 第一次测试 | 海外版 Voice Clone → TTS 出 MP3 |
| 追求质量 | 优先 `speech-2.8-hd` |
| 追求速度 / 批量预览 | `speech-2.8-turbo` 先跑测试 |

---

### 3. 素材准备：不用复杂，但必须干净

#### 声音样本（MiniMax 要求摘要）

| 项 | 要求 |
|----|------|
| 格式 | MP3 / M4A / WAV |
| 时长 | 至少 10 秒，最多 5 分钟 |
| 大小 | ≤ 20 MB |
| 可选提示音频 | < 8 秒，且提供与音频完全对应的文字 |

实操建议录 **30–90 秒**：

- 单人  
- 无 BGM  
- 无明显混响 / 电流声  
- 音量稳定  
- 语速接近日常口播  
- 不要过度降噪、变速或严重压缩的二手音频  

#### 人像

- 正脸看镜头，五官无遮挡  
- 露出头、肩和上半身，人物约占画面 50%–70%  
- 嘴部清晰，不被头发 / 手 / 滤镜挡  
- 竖屏优先 9:16 或接近 9:16  
- HeyGen Assets：PNG / JPEG；普通素材单文件上限约 32 MB  

原则：**嘴部越清晰，口型越稳；声音越干净，克隆越像。**

---

### 4. 怎么放进 Codex 执行

推荐目录结构：

```markdown
project/
├── inputs/
│   ├── portrait.jpg
│   ├── voice-source.mp3
│   └── script.md
├── work/
│   ├── voiceover-full.mp3
│   ├── preview-15s.mp3
│   └── job-state.json
└── outputs/
    ├── preview-15s.mp4
    └── final-1080p.mp4
```

对 Codex 的示例指令：

```text
请用 MiniMax 海外版声音克隆和 HeyGen API 制作数字人口播。
输入：
- 文案：inputs/script.md
- 人像：inputs/portrait.jpg
- 声音样本：inputs/voice-source.mp3
- MiniMax 密钥来自环境变量 MINIMAX_API_KEY
- HeyGen 密钥来自环境变量 HEYGEN_API_KEY
流程：
1. 先检查素材。
2. 先生成 15 秒样片。
3. 样片确认后再生成完整版。
4. 所有任务 ID 写入 work/job-state.json。
5. 不要在日志、脚本或文档中显示完整密钥。
```

重点是**标准化**：不必每次靠记忆，把正确流程写进 Skill，让代理每次按流程跑。

---

### 5. Skill 固定了什么

仓库：https://github.com/Jingyi-Wu-Richael/rachel-digital-human-production  

调用示例：

```text
用 $rachel-digital-human-production 做这条视频，先只做 15 秒样片。
```

Skill 固定项：

- 固定目录结构  
- 先检查文案、人像、声音样本  
- MiniMax 负责声音，HeyGen 负责画面  
- **永远先生成 15 秒样片**  
- 样片未明确确认，不生成完整版  
- 每步记录 `voice_id`、`asset_id`、`video_id` 与状态  
- 失败不盲目重试，避免重复扣费  
- 最终 MP4 必须完整检查  
- 不把 API Key、授权 header、临时下载链接写进日志或状态文件  

---

### 6. 小 tips：成片不自然时查什么

常见问题：

- 声音不像本人  
- 中文口型跟不上  
- 脸部轻微变形  
- 嘴角 / 下巴运动奇怪  
- 眨眼和肩部动作不自然  
- 构图不适合短视频平台  

所以 **15 秒样片是强制门禁**：先确认声音、口型、画面、构图，再跑完整片。

---

### 相关官方链接（作者文中列出）

| 资源 | URL |
|------|-----|
| GitHub Skill | https://github.com/Jingyi-Wu-Richael/rachel-digital-human-production |
| MiniMax Voice Clone 文档 | https://platform.minimax.io/docs/guides/speech-voice-clone |
| HeyGen Image to Video | https://developers.heygen.com/image-to-video |
| HeyGen Assets | https://developers.heygen.com/assets |

> 注：整理时对 GitHub raw/API 的额外抓取未获执行许可，仓库细节以作者 Article 公开内容与上述链接为准；克隆仓库可本地再核 README / Skill 文件。

---

## 三、可复用检查清单（照做）

### A. 上线一条数字人口播前

- [ ] `inputs/script.md` 定稿  
- [ ] `inputs/portrait.jpg`：正脸、嘴清、构图够竖屏  
- [ ] `inputs/voice-source.mp3`：30–90s 干净单人样本  
- [ ] 环境变量：`MINIMAX_API_KEY`、`HEYGEN_API_KEY`（勿入库）  
- [ ] MiniMax：clone → TTS（质量优先 `speech-2.8-hd`）  
- [ ] HeyGen：用 **MiniMax MP3 驱动**，禁止再用 HeyGen 自带 voice 盖音  
- [ ] 只出 **15s 样片** → 人审  
- [ ] 通过后再 full render → 下载验片 → 写 `job-state.json`  

### B. 从「能做」到「分身账号」

- [ ] 形象统一（服装/背景/镜头距离）  
- [ ] 音色稳定（同一 voice_id，不轻易重 clone）  
- [ ] 平台适配（抖音竖屏 9:16；本演示片为横屏高清 demo）  
- [ ] 内容栏目固定（知识口播 / 产品介绍等）  
- [ ] 公开问反馈（主帖式「形象状态怎么样」）收集调性  
- [ ] 方法论文档/Skill 开源或内部分享，降低协作成本  

---

## 四、架构示意（文字）

```
[真人声样] --clone--> [MiniMax Voice]
[文案 script.md] --TTS--> [voiceover.mp3] ----\
                                               +--> [HeyGen I2V / Avatar] --> [preview 15s]
[正面人像 portrait] ---------------------------/            |
                                                      人工确认
                                                            |
                                                      [full MP4]
                                                            |
                                                      验片 + job-state 归档
```

风控要点：样片门禁、状态落盘、失败不盲重试、密钥永不进日志。

---

## 五、传播与产品启示

| 观察 | 含义 |
|------|------|
| Article 帖 51 万+ views、2409 bookmarks | 「不相信是数字人」级别的成片 + 可复制流程，收藏动机极强 |
| 分身帖 bookmarks > likes | 观众在等账号/形象落地，不只是点赞娱乐 |
| Skill 化（Codex） | 把 PM/创作者的流程记忆变成可执行资产 |
| 声音/画面拆分 | 各用最强专项工具，避免「一个工具通吃却双输」 |
| 15 秒强制样片 | 用小额成本买质量确认，控 API 账单与翻车率 |

对做 AI 内容/数字人业务的直接启发：

1. **先工程化，再人格化上线**（Skill → 分身账号）  
2. **门禁步骤写进系统**，不要写在脑内  
3. **展示层问反馈，资产层放 GitHub**——两条内容分工明确  

---

## 六、资源汇总

### 原帖与媒体

| 名称 | 链接 / 路径 |
|------|-------------|
| 分身上线主帖 | https://x.com/Zesee/status/2082848456985497901 |
| 实战攻略 Article 帖 | https://x.com/Zesee/status/2077723280534851786 |
| 作者 | https://x.com/Zesee |
| 本地视频（720p） | `assets/videos/rachel-ai-digital-human-zesee-2026-07-30.mp4` |
| 本地封面 | `assets/videos/rachel-ai-digital-human-zesee-2026-07-30-thumb.jpg` |

### 工具与代码

| 名称 | 说明 |
|------|------|
| rachel-digital-human-production | Codex Skill 仓库 |
| MiniMax | 声音克隆 + TTS |
| HeyGen | Image-to-Video / Photo Avatar |
| Codex | 流程编排与状态管理 |

### Article 配图（CDN，未全部本地下载）

作者长文中含多张说明图，例如：

- 封面：`https://pbs.twimg.com/media/HNWMh9eXQAAFCKW.jpg`
- 其他：`HNWLRYhWoAABTgS.jpg`、`HNWLRYiWkAAilel.jpg`、`HNWLh8PXkAAXR9u.jpg`、`HNWLh8FW0AA8YAj.jpg`、`HNWNKgfXUAAiMth.jpg`、`HNWNWrfXwAAyrJX.jpg`、`HNWOFu1XAAA_tKR.jpg` 等  

---

## 七、限制说明

- 主帖评论区未做深度抓取（登录墙常见限制）。  
- GitHub 仓库目录/README 本次未二次抓取（执行未获许可）；流程以 X Article 公开正文为准。  
- 本地仅归档 **720p** 演示片；1080p/4K 原片 URL 见上文，可按需另下。  
- 价格（如 ~$2 / 2min）与模型名（`speech-2.8-hd` 等）随厂商变更，落地前请核对官方文档。  

---

## 一句话收束

> **分身要像真人，先把声音和画面拆开；想规模化，先把 15 秒样片写进 Skill。**

---

*来自hueshadow*
