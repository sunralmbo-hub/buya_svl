# Buya Illustrations

> 把中文文章里的判断、流程、状态和隐喻，转成一张张“不鸭不咋样”式白底、粗黑线、橙嘴白鸭、生活情绪梗正文配图。
>
> 16:9 横版 | 不鸭不咋样 IP | 表情包感 | 生活梗 | 短中文 | Codex Skill

---

## 这个仓库是什么

Buya Illustrations 是一个 Codex Skill，用来指导 AI Agent 为中文文章、帖子、博客、Notion 文档和方法论内容生成“不鸭不咋样”风格正文配图。

它的核心目标是：先理解文章里的认知锚点和情绪锚点，再把其中一个判断、状态、流程或隐喻，变成一个有记忆点的 16:9 不鸭生活梗场景。

默认视觉 IP 是“不鸭不咋样”：一只白色长脖子鸭子，橙色扁嘴，黑色小点眼睛，粗黑线轮廓，圆头鼓脸，表情呆傻、无语、可爱、略欠但很有情绪。它不是严肃系统操作员，而是把抽象观点变成生活梗、表情包反应和情绪替身的角色。

---

## 视觉风格

- 纯白背景，不要纸纹、米色、阴影、渐变
- 粗黑色手绘轮廓，线条圆润稳定
- 白色长脖子鸭，橙色扁嘴，黑色小点眼睛，圆头鼓脸
- 大量留白，主体只占画面约 35%-55%
- 中文最多一句，优先 2-6 个字
- 一张图只表达一个核心情绪场景、生活梗或隐喻动作
- 不鸭不咋样必须承载情绪或梗点，不能只是装饰

---

## 参考图策略

参考图只用于校准不鸭的角色识别度：白鸭长脖子、圆头鼓脸、橙色扁嘴、小点眼、粗黑线和生活情绪。

如果需要长期保留参考图，请把可用图片放入 `buya-illustrations/assets/references/`。参考图只用于形象校准，不作为构图模板。

---

## 安装

```bash
git clone https://github.com/sunralmbo-hub/buya_svl.git
cd buya_svl
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

---

## 工作流程

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

## 原作者

本仓库 fork 自 [helloianneo/ian-xiaohei-illustrations](https://github.com/helloianneo/ian-xiaohei-illustrations)，原项目采用 MIT License。
