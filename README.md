# Lumiscale-Superskill · 提示词库

> AI 图像/视频生成 Prompt 收藏库。分类整理，快捷名索引，开箱即用。
> 来自 hueshadow

---

## 快速索引（按快捷名）

| 快捷名 | 分类 | 说明 |
|--------|------|------|
| `角色身份板` | 角色设计 | 电影级动画工作室角色研究 + 画册排版（@aimikoda） |
| `角色手账板` | 角色设计 | Pinterest 温暖手账风 · 生活方式角色介绍卡（@Fujimoto_hina） |
| `芭蕾Xin手账板` | 角色设计 | 角色手账板定制 · 芭蕾舞者 Xin（芭蕾鑫工作室） |
| `人像公式` | 摄影 | 通用人像 Prompt 公式 + 九模块框架 + 8 种风格预设（@zhongying14） |
| `油画写真` | 摄影 | 法式复古油画少女轻私房 · 2×2 四宫格（@zhongying14） |
| `破屏穿越` | 摄影 | 破屏穿越 · 3D 人物从手机屏幕冲出（@you1873118） |
| `时尚编辑` | 摄影 | 时尚杂志双页广告 · Vogue/GQ 级排版（@Ankit_patel211） |
| `Chibi编辑` | 图像编辑 | Chibi Q版小人风格照片编辑（@Ciri_ai） |
| `实写手绘VFX` | 视频 | 实写×手绘动画 VFX：ChatGPT 指示文 + Seedance 终稿（@genel_ai） |
| `发型变装` | 视频 | 9 套发型卡点变装：Turn+Hair Whip + 影棚竖屏 10s（@johnAGI168） |

---

## 目录结构

```
Lumiscale-Superskill/
├── README.md                    ← 本文件
├── prompts/
│   ├── character-design/        ← 角色设计类
│   ├── photography/             ← 摄影/人像类
│   ├── image-editing/           ← 图像编辑类
│   ├── illustration/            ← 插画类
│   └── video/                   ← 视频生成类
│       ├── README.md
│       └── live-action-handdrawn-vfx-chatgpt-seedance.md
└── docs/                        ← 分析与长文
```

---

## 分类详情

### 🎭 角色设计（character-design）

| 快捷名 | 文件 | 内容 | 来源 |
|--------|------|------|------|
| `角色身份板` | character-identity-board-prompt.md | 动画工作室级角色研究 + 艺术画册排版 | @aimikoda |
| `角色手账板` | character-scrapbook-poster-prompt.md | Pinterest 温暖手账风 · 生活方式角色介绍卡 | @Fujimoto_hina |
| `芭蕾Xin手账板` | character-scrapbook-ballet-xin.md | 角色手账板定制 · 芭蕾舞者 Xin | 参考照片定制 |

> 详见 [prompts/character-design/README.md](prompts/character-design/README.md)

### 📷 摄影（photography）

| 快捷名 | 文件 | 内容 | 来源 |
|--------|------|------|------|
| `人像公式` | portrait-prompt-formulas.md | 通用人像 Prompt 公式 + 九模块框架 + 负面约束库 + 8 种风格预设 | @zhongying14 |
| `油画写真` | french-vintage-oil-painting-portrait-2x2.md | 法式复古油画少女轻私房摄影 · 2×2 四宫格完整 Prompt | @zhongying14 |
| `破屏穿越` | screen-burst-luxury-ad-prompt.md | 破屏穿越风格 · 豪华商业广告海报（3D 人物从手机屏幕冲出） | @you1873118 |
| `时尚编辑` | fashion-editorial-system-prompt.md | 时尚杂志双页广告 System Prompt · Vogue/GQ 级奢侈广告排版 | @Ankit_patel211 |

> 详见 [prompts/photography/README.md](prompts/photography/README.md)

### ✂️ 图像编辑（image-editing）

| 快捷名 | 文件 | 内容 | 来源 |
|--------|------|------|------|
| `Chibi编辑` | chibi-photo-edit-prompt.md | Chibi Q版小人风格照片编辑 · 保持原图不变 + 添加 mini 角色装饰 | @Ciri_ai |

### 🎬 视频（video）

| 快捷名 | 文件 | 内容 | 来源 |
|--------|------|------|------|
| `实写手绘VFX` | live-action-handdrawn-vfx-chatgpt-seedance.md | 实写×手绘发光动画 VFX：ChatGPT 指示文 + Seedance 2.0 终稿 + 五铁律 | @genel_ai |
| `发型变装` | hairstyle-transformation-seedance.md | 9 套发型卡点变装：Turn+Hair Whip 转场 + 影棚竖屏 10s | @johnAGI168 |

> 详见 [prompts/video/README.md](prompts/video/README.md)  
> 分析长文：`docs/live-action-handdrawn-vfx-chatgpt-seedance-genel-2026-07-28.md` · `docs/hairstyle-transformation-seedance-johnagi168-2026-07-28.md`

---

## 使用方式

1. 在对话中说对应快捷名即可引用，如 `用角色手账板` 或 `用实写手绘VFX`
2. 每个提示词文件包含：完整 Prompt、模板化版本、使用说明、技巧要点、来源链接
3. 需要参考照片才能出图的 prompt（如油画写真、Chibi编辑），需在 ChatGPT 原生界面使用，API 不支持上传参考图
4. 视频类 prompt 默认面向 Seedance 2.0 文本→视频；BGM 建议 SUNO 后贴

---

## 统计

- **总提示词数**：10+
- **分类数**：4+（角色设计 / 摄影 / 图像编辑 / 视频）
- **最新更新**：2026-07-28（+发型变装）
- **来源平台**：X/Twitter · note

---

*来自 hueshadow*
