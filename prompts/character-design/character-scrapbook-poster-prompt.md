# GPT Image 2 · 角色手账拼贴板 Prompt（Character Scrapbook Poster）

> 来源：X/Twitter @Fujimoto_hina（Aegon）[原文](https://x.com/fujimoto_hina/status/2054104921344245823)
> 工具：ChatGPT + GPT Image 2（原帖标注 GPT 2 on ChatGPT）
> 提取时间：2026-05-13
> 来自hueshadow

---

## 完整 Prompt（JSON 结构化，可直接复制使用）

```
{ "title": "Meet [角色名]!", "style": "Ultra-detailed cozy aesthetic scrapbook poster, Pinterest-inspired anime realism, warm beige neutral palette, cinematic soft lighting, dreamy lifestyle collage, highly detailed digital illustration, soft matte textures", "subject": { "description": "A handsome young man named [角色名] with curly dark brown hair, warm brown eyes, trimmed beard, black glasses, friendly smile, wearing a cream knit sweater layered with a black puffer vest, blue jeans, silver necklace, wristwatch, and holding an iced coffee cup", "pose": "Standing casually with one hand in pocket and coffee in the other, relaxed confident posture", "expression": "Warm, approachable, calm, thoughtful, slightly playful" }, "scene": { "background": "Soft pastel beige scrapbook-style background with handwritten doodles, tiny stars, hearts, paper textures, polaroids, aesthetic lifestyle cards, tapes, and cozy decorative elements", "lighting": "Warm ambient sunlight with soft cinematic glow and dreamy highlights", "mood": "Comforting, stylish, cozy masculine aesthetic" }, "layout": { "design": "Pinterest-style character introduction board with multiple aesthetic sections arranged around the central character portrait", "elements": [ "rounded aesthetic cards", "handwritten typography", "mini lifestyle photo grids", "polaroid pictures", "sticky tape decorations", "cute doodles and icons" ] }, "sections": { "the_vibe": [ "Soft heart, strong mind", "Quiet but thoughtful", "Loyal to the people I love", "Ambitious & disciplined", "Protective energy" ], "what_i_love": [ "coffee", "night drives", "music", "travel", "sunsets", "gaming" ], "goals_and_dreams": [ "Build a peaceful life", "Travel the world", "Become successful", "Create meaningful memories", "Inspire others" ], "currently": [ "Working on my goals", "Listening to music", "Planning my next trip", "Building discipline" ], "daily_essentials": [ "coffee", "watch", "headphones", "skincare", "sunglasses", "phone" ], "this_or_that": [ "Sunrise or Sunset", "Beach or Mountains", "Books or Movies", "City or Nature", "Sweet or Salty" ], "fun_facts": [ "Overthinks everything", "Listens to music at night", "Acts tough but cares deeply", "Loves late-night conversations", "Always has a playlist ready" ], "reminder_to_self": [ "You are enough.", "You are so capable.", "Keep going, [角色名].", "Proud of you, always." ] }, "extra_details": [ "Coffee cup with heart doodle", "Minimal masculine accessories", "Soft paper scrapbook textures", "Cute heart and sparkle doodles", "Vintage polaroid aesthetic", "Warm cozy lifestyle vibe", "Neutral earthy tones", "Soft shadows and cinematic depth" ], "quality": { "resolution": "8K", "rendering": "Ultra detailed", "texture": "Soft matte illustration with subtle paper grain", "detail_level": "Highly intricate lifestyle collage composition" } }
```

---

## 模板化版本（替换 [ ] 内内容即可）

```json
{
  "title": "Meet [角色名]!",
  "style": "Ultra-detailed cozy aesthetic scrapbook poster, Pinterest-inspired anime realism, warm beige neutral palette, cinematic soft lighting, dreamy lifestyle collage, highly detailed digital illustration, soft matte textures",
  "subject": {
    "description": "[角色外观描述：发型、眼睛、服装、配饰、手持物]",
    "pose": "[姿势描述]",
    "expression": "[表情描述]"
  },
  "scene": {
    "background": "Soft pastel beige scrapbook-style background with handwritten doodles, tiny stars, hearts, paper textures, polaroids, aesthetic lifestyle cards, tapes, and cozy decorative elements",
    "lighting": "Warm ambient sunlight with soft cinematic glow and dreamy highlights",
    "mood": "[整体氛围]"
  },
  "layout": {
    "design": "Pinterest-style character introduction board with multiple aesthetic sections arranged around the central character portrait",
    "elements": ["rounded aesthetic cards", "handwritten typography", "mini lifestyle photo grids", "polaroid pictures", "sticky tape decorations", "cute doodles and icons"]
  },
  "sections": {
    "the_vibe": ["[性格标签]", "..."],
    "what_i_love": ["[爱好]", "..."],
    "goals_and_dreams": ["[目标]", "..."],
    "currently": ["[当前状态]", "..."],
    "daily_essentials": ["[日常必备]", "..."],
    "this_or_that": ["[二选一]", "..."],
    "fun_facts": ["[趣事]", "..."],
    "reminder_to_self": ["[自我提醒]", "..."]
  },
  "extra_details": ["[额外细节]", "..."],
  "quality": {
    "resolution": "8K",
    "rendering": "Ultra detailed",
    "texture": "Soft matte illustration with subtle paper grain",
    "detail_level": "Highly intricate lifestyle collage composition"
  }
}
```

---

## 使用说明

### 适用工具
- GPT Image 2（原始创作工具，原帖标注 "GPT 2 on ChatGPT"）
- 也适用于其他 JSON-prompt 兼容的文生图工具

### 适用场景
- Pinterest 风格角色介绍板：适合展示角色个性、生活方式、审美品味
- 角色人设可视化：将抽象的性格标签转化为视觉拼贴
- 社交媒体角色展示卡：适合作为头像/封面/角色设定图
- 温暖手账风：适合温馨、治愈、生活化的人物呈现

### 与「角色身份板」的区别

| 维度 | 角色手账板（本提示词） | 角色身份板（@aimikoda） |
|------|----------------------|------------------------|
| 风格 | 温暖手账拼贴、Pinterest 审美 | 电影级动画工作室、画册排版 |
| 目的 | 展示角色个性与生活方式 | 生成 AI 可读的身份参考图 |
| 内容 | 性格标签、爱好、目标、日常 | 多角度全身、剪影、表情研究 |
| 色调 | 暖米色、柔和电影光 | 纯白/米白背景、干净克制 |
| 排版 | 圆角卡片、手写字体、宝丽来 | 不对称优雅、艺术书籍布局 |

### 关键技巧
1. **JSON 结构化**：将 Prompt 写成 JSON 格式，ChatGPT/GPT Image 2 能更准确理解层次关系
2. **分区设计**：通过 `sections` 把角色信息分为 vibe/爱好/目标/当前/日常/趣事/自我提醒等模块
3. **手账元素**：纸纹理、拍立得、胶带装饰、手绘涂鸦、圆角卡片 —— 这些是营造 "scrapbook" 感的关键
4. **暖色调**：暖米色 + 柔光 + 电影级高光，避免冷色调
5. **可替换性**：将 [角色名] 和 sections 内容替换即可适配任意角色

---

## 快捷名

`角色手账板` — 引用此提示词时可直接用此名称
