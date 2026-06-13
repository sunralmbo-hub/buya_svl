# Buya Illustrations

> 把中文文章里的判断、流程、状态和隐喻，转成一张张“不鸭不咋样”式白底、粗黑线、橙嘴白鸭、生活情绪梗正文配图。
>
> 16:9 横版 | 不鸭不咋样 IP | 表情包感 | 生活梗 | 短中文 | Codex Skill

---

## 这个仓库是什么

Buya Illustrations 是一个 Codex Skill，用来指导 AI Agent 为中文文章、帖子、博客、Notion 文档和方法论内容生成“不鸭不咋样”风格正文配图。

它不是通用插画 prompt，也不是 PPT 信息图模板。它的核心目标是：先理解文章里的认知锚点和情绪锚点，再把其中一个判断、状态、流程或隐喻，变成一个有记忆点的 16:9 不鸭生活梗场景。

默认视觉 IP 是“不鸭不咋样”：一只白色长脖子鸭子，橙色扁嘴，黑色小点眼睛，粗黑线轮廓，圆头鼓脸，表情呆傻、无语、可爱、略欠但很有情绪。它不是严肃系统操作员，而是把抽象观点变成生活梗、表情包反应和情绪替身的角色。

一句话：**让 AI 不只是“配一张图”，而是把文章里的一个关键状态画成“不鸭式生活梗”。**

---

## 适合谁用

特别适合：

- 写中文文章，需要正文配图和文章插图的人
- 做知识型内容、方法论内容、AI 工作流内容的人
- 想把抽象判断画成轻巧生活梗的人
- 想要一种比 PPT 信息图更轻、更傻、更有个人识别度的配图风格的人
- 用 Codex 做内容生产，希望稳定复用一套视觉语言的人

不适合：

- 想要商业插画、品牌 KV 或精致扁平插画的人
- 想要传统 PPT 信息图、复杂架构图或流程图的人
- 想把大量正文、长段解释或完整课程页塞进一张图里的人
- 需要严格可编辑矢量源文件的人
- 需要直接复刻未授权原图的人

---

## 它会产出什么

默认输出：

- 16:9 横版正文配图
- 一篇文章的 4-8 张 shot list
- 每张图的主题、核心意思、情绪关键词、不鸭式场景、不鸭动作和中文短句建议
- 最终 PNG 图片，保存到 workspace 的 `assets/<article-slug>-illustrations/`

默认不输出：

- PPTX / PDF / Keynote
- SVG / HTML / Canvas 可编辑图
- 商业海报或封面 KV
- 大段文字型信息图
- 对参考图、原图、日期、水印或具体构图的复制品

---

## 视觉风格

这个 skill 默认使用“不鸭不咋样生活梗正文配图”风格：

- 纯白背景，不要纸纹、米色、阴影、渐变
- 粗黑色手绘轮廓，线条圆润稳定
- 白色长脖子鸭，橙色扁嘴，黑色小点眼睛，圆头鼓脸
- 大量留白，主体只占画面约 35%-55%
- 中文最多一句，优先 2-6 个字
- 一张图只表达一个核心情绪场景、生活梗或隐喻动作
- 不鸭不咋样必须承载情绪或梗点，不能只是装饰
- 呆傻、可爱、无厘头、清爽，但不要精致商业 mascot 感

---

## 参考图策略

参考图只用于校准不鸭的角色识别度：白鸭长脖子、圆头鼓脸、橙色扁嘴、小点眼、粗黑线和生活情绪。

本仓库的 `buya-illustrations/assets/references/` 里放的是自制 SVG 校准图，不直接搬运网上原图。不要把未授权网上原图直接提交进仓库，不要复刻原图里的日期、水印、平台 ID、原始台词、具体服装、具体道具或具体构图。

---

## 安装

克隆仓库：

```bash
git clone https://github.com/sunralmbo-hub/buya_svl.git
cd buya_svl
```

复制 skill 到 Codex skills 目录：

```bash
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
cp -R ./buya-illustrations "${CODEX_HOME:-$HOME/.codex}/skills/"
```

安装后，在 Codex 里使用：

```text
Use $buya-illustrations 为这篇中文文章设计并生成 5 张不鸭不咋样生活梗正文配图。
```

---

## 怎么用

### 只做配图规划

```text
Use $buya-illustrations 先不要生图。
请分析下面这篇文章哪里值得配图，输出 5 张左右的 shot list。
每张图写清楚：放在哪段后、主题、核心意思、情绪关键词、不鸭式场景、不鸭在做什么、建议中文短句。

<粘贴文章>
```

### 直接生成正文配图

```text
Use $buya-illustrations 把下面这篇文章生成 4 张不鸭不咋样生活梗正文配图。
要求：16:9 横版、纯白背景、粗黑手绘线稿、白色长脖子鸭、橙色扁嘴、小点眼、短中文。

<粘贴文章>
```

### 为单个概念生成一张图

```text
Use $buya-illustrations 为“信任不是喊出来的，而是一块证据一块证据铺过去”生成一张正文配图。
画面要像不鸭表情包：一只白鸭、一个动作、一句短话、一个生活梗。
```

### 去掉图里的标题或错误文字

```text
Use $buya-illustrations 帮我编辑这张图，去掉左上角的“流程图”标题，其他内容保持不变。
```

---

## 工作流程

这个 skill 的流程是：

1. 读取文章、Markdown、Notion 内容、截图或用户给的主题
2. 提炼核心观点、认知转折、流程结构和适合视觉化的段落
3. 找出每个候选图的情绪锚点和梗点
4. 先输出 shot list：每张图只选一个认知锚点和一个生活情绪
5. 为每张图选择不鸭式构图：情绪替身、生活梗、道具隐喻、表情包短句或小漫画分镜
6. 重新发明一个简单生活场景
7. 让不鸭不咋样承担核心动作和情绪
8. 每张图单独调用图像模型生成
9. 按 QA checklist 检查：不鸭识别度、白底、粗黑线、橙嘴、小点眼、短中文、非 PPT 感、非参考图复刻
10. 保存最终 PNG，并报告用途和路径

---

## 目录结构

```text
.
├── README.md
├── LICENSE
├── NOTICE.md
├── assets/
├── examples/
└── buya-illustrations/
    ├── SKILL.md
    ├── agents/
    │   └── openai.yaml
    ├── assets/
    │   └── references/
    │       ├── 01-buya-neutral.svg
    │       ├── 02-buya-holding-sign.svg
    │       ├── 03-buya-stuck.svg
    │       └── 04-buya-carrying-papers.svg
    └── references/
        ├── style-dna.md
        ├── buya-ip.md
        ├── composition-patterns.md
        ├── prompt-template.md
        ├── qa-checklist.md
        └── reference-policy.md
```

真正需要安装到 Codex 的是子目录：

```text
buya-illustrations/
```

---

## 注意事项

- 图片里的中文文字越短越稳定。
- 每张图只讲一个核心情绪场景，不要把文章做成说明书。
- 不鸭不咋样必须承担情绪或梗点；如果去掉不鸭画面仍然完全成立，说明它太装饰了。
- 参考图只用于校准角色比例、线条、留白、颜色克制和情绪表达，不要复刻构图。
- AI 图像模型可能出现错字、幻觉标签、风格漂移或多余标题，生成后需要检查。
- 如果中文错字严重，优先减少标注词并重生成。

---

## 原作者

本仓库 fork 自 [helloianneo/ian-xiaohei-illustrations](https://github.com/helloianneo/ian-xiaohei-illustrations)，原项目采用 MIT License。
