# 通用人像 Prompt 公式 & 负面约束库

> 来源：X/Twitter @zhongying14（麻酱AI实验室）[原文](https://x.com/zhongying14/status/2050973647548866765)
> 提取时间：2026-05-12
> 来自hueshadow

---

## 一、人像 Prompt 公式

### 英文版

```
[用途] + [主体/气质] + [镜头语言] + [构图/机位] + [景深] + [光线设计] + [色调锚点] + [真实感细节] + [限制项]
```

### 中文理解

先说这张图是什么 → 再说拍谁 → 再说怎么拍 → 再说光线和色调 → 最后说真实感和不要什么。

### 示例

```
portrait shot 85mm lens, close 3/4 framing, slight telephoto compression
```

---

## 二、九模块速查

### 模块 1 · 图像用途
头像 / 职业写真 / 生活方式图 / 杂志风格图 / 纪实 / 美妆 / 电影感人像

### 模块 2 · 主体和气质
人脸特征保留：脸型、五官比例、眉眼结构、鼻子、嘴唇、肤色、发型、年龄感、整体气质

### 模块 3 · 镜头语言
| 焦段 | 画面感 |
|------|--------|
| 24mm–35mm | 环境人像、空间感强 |
| 50mm | 自然视角、平实记录感 |
| 85mm | 经典人像、适度压缩、主体突出 |
| 135mm+ | 远距离抓拍、强压缩感 |

### 模块 4 · 构图和机位
- 平视（最稳）/ 略高机位（柔化）/ 略低机位（力量感）
- 正面直视 / 45度侧面 / 抓拍感偏移

### 模块 5 · 景深
明确光圈（f/1.4, f/2.8, f/4）+ 背景虚化程度 + 背景信息保留量

### 模块 6 · 光线设计
```
soft natural window light from the left, gentle shadow on the right side of face, subtle catchlight in eyes
```

### 模块 7 · 色调锚点
| 锚点 | 方向 |
|------|------|
| Portra 400 | 柔和肤色、温暖色调 |
| Kodachrome | 高饱和、强对比、复古感 |
| Fuji Pro 400H | 清淡、青绿调、日系感 |
| Hasselblad | 极致细节、中画幅质感 |

### 模块 8 · 真实感细节
皮肤纹理、眼神光（catchlight）、背景虚化渐变、布料质地、高光方向

### 模块 9 · 限制项

---

## 三、通用负面提示词（Negative Prompts）

### 通用
```
no plastic skin, no airbrushed look, no unnatural poses,
no over-saturated colors, no artificial bokeh
```

### 夜景额外加
```
restrained neon glow, no excessive halation
```

### 商业写真额外加
```
natural expression, not stiff, not overly posed
```

---

## 四、8 种风格预设速查

| 风格 | 推荐参数 |
|------|---------|
| 职业写真 | 85mm, f/2.8, 平视, 柔光箱正面光, 简洁背景 |
| 胶片生活方式 | 35mm, f/2, 抓拍感, 自然光, Portra 400 色调 |
| 黑白纪实 | 50mm, f/4, 平视, 硬侧光, 高对比度 |
| 都市风 | 24mm, f/5.6, 略低机位, 环境光混合, 冷色调 |
| 夜景电影感 | 50mm, f/1.4, 45度侧, 霓虹光+环境光, 电影色调 |

---

## 五、三步实操

1. **确定用途** — 头像/写真/生活方式/纪实/电影感
2. **从 9 模块各选 1–2 项** — 不要堆太满
3. **拼成拍摄 brief** — 像摄影执行单一样写 prompt

---

*来自hueshadow*
