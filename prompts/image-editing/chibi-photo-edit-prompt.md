# GPT Image 2 — Chibi 风格照片编辑 Prompt

> 来源：X/Twitter @Ciri_ai [原文](https://x.com/Ciri_ai/status/2050094437821513896)
> 提取时间：2026-05-12
> 数据：20.5 万查看 | 3.6K 喜欢 | 2.4K 书签
> 来自hueshadow

---

## Prompt（完整原文）

```
Edit the image while keeping the original photo completely unchanged — 
including the person, face, body, pose, lighting, and gym background.

Add multiple small, cute chibi-style "mini versions" of her around the image. 
Each mini character should have a big head, expressive facial features, 
and match her hairstyle and outfit.

Depict each mini version doing different gym-related activities:

- one cheering with arms raised
- one running in running shoes
- one drinking from a shaker bottle
- one wearing sporty running glasses
- one climbing near her leg

Enhance the image with playful, hand-drawn doodles and handwritten notes 
in white and pink ink, in a scrapbook style. Include elements like arrows, 
stars, hearts, sparkles, and sketchy lines.

Add cute, handwritten gym-themed motivational phrases:

"lift strong"
"stronger every rep"
"no pain no gain"
"sweat now, shine later"
"progress over perfection"
"train hard, stay soft"

The overall vibe should feel fun, energetic, and feminine.
```

---

## 结构拆解

| 层次 | 内容 | 作用 |
|------|------|------|
| **约束层** | 原图完全不变（人物/脸/身体/姿势/光线/背景） | 防止 AI 篡改原图，编辑模式下最关键的一句 |
| **主体层** | 5 个 chibi 迷你版人物，每人不同动作 | 定义要添加的核心元素，逐个描述避免重复 |
| **风格层** | 手绘涂鸦 + 粉白墨水手写字 + 剪贴簿风 | 定调整体视觉风格 |
| **装饰层** | 箭头/星星/爱心/火花/素描线 | 丰富画面细节，用列举法不给 AI 自由发挥空间 |
| **文案层** | 6 句健身励志语（英文手写体） | 用引号包裹确保原样输出 |
| **定调层** | fun, energetic, feminine | 三个词收束全局风格 |

---

## 通用化模板

把上面的 Prompt 中的具体元素替换为你的场景：

```
Edit the image while keeping the original photo completely unchanged — 
including the person, face, body, pose, lighting, and background.

Add multiple small, cute chibi-style "mini versions" of [主体] around the image. 
Each mini character should have a big head, expressive facial features, 
and match [主体]'s hairstyle and outfit.

Depict each mini version doing different [场景相关] activities:

- [活动 1]
- [活动 2]
- [活动 3]
- [活动 4]
- [活动 5]

Enhance the image with playful, hand-drawn doodles and handwritten notes 
in [颜色 1] and [颜色 2] ink, in a scrapbook style. Include elements like 
arrows, stars, hearts, sparkles, and sketchy lines.

Add cute, handwritten [主题] motivational phrases:

"[短语 1]"
"[短语 2]"
"[短语 3]"
"[短语 4]"
"[短语 5]"
"[短语 6]"

The overall vibe should feel [氛围词 1], [氛围词 2], and [氛围词 3].
```

---

## 技巧要点

1. **「原图完全不变」放在第一句** — GPT Image 2 编辑模式的关键约束，不放前面 AI 容易连带原图一起改动
2. **每个 mini 角色独立描述动作** — 不写「加几个小人」这种笼统描述，逐个定义，避免 AI 产出重复或混乱
3. **装饰元素用列举法** — 写出「arrows, stars, hearts, sparkles, sketchy lines」，不给 AI 自行发挥的余地
4. **文案用引号包裹** — 确保文字原样输出，AI 不会自行改写
5. **定调词收尾** — 2-3 个氛围形容词放在最后，收束全局风格
