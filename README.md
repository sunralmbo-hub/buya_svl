# Buya Illustrations

> 把中文文章里的判断、流程、状态和隐喻，转成“不鸭不咋样”式白底、粗黑分镜、橙嘴白鸭、小漫画正文配图。
>
> 16:9 横版 | 不鸭不咋样 IP | 小漫画 | 手写对白框 | 生活梗 | Codex Skill

---

## 这个仓库是什么

Buya Illustrations 是一个 Codex Skill，用来指导 AI Agent 为中文文章、帖子、博客、Notion 文档和方法论内容生成“不鸭不咋样”风格小漫画正文配图。

它的核心目标是：先理解文章里的认知锚点和情绪锚点，再把其中一个判断、状态、流程或隐喻，变成一个 16:9 不鸭小漫画。

默认视觉 IP 是“不鸭不咋样”：白色长脖子鸭子，橙色扁嘴，黑色小点眼睛，粗黑线轮廓，圆头鼓脸。常见画面可以是一只鸭、两只鸭互动、几格小过程，也可以是鸭群、浅绿色背景块和特殊鸭。

---

## 视觉风格

- 纯白页面背景，分镜内部可用浅绿色色块
- 粗黑色手绘漫画分镜框，边框略微不规则
- 白色长脖子鸭，橙色扁嘴，黑色小点眼睛，圆头鼓脸
- 中文放在白色手写文本框里，像漫画旁白或对白
- 一张图只表达一个核心情绪场景、生活梗或隐喻动作
- 可选：鸭群、特殊鸭、粉色标记、浅绿背景、黄色闪光

---

## 参考图策略

参考图只用于校准不鸭的小漫画语法：粗黑分镜、白鸭比例、橙嘴、小点眼、手写对白框、生活情绪。鸭群只是可选方向。

如需长期保留参考图，请放入 `buya-illustrations/assets/references/`。参考图只用于风格校准，不作为构图模板。

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
Use $buya-illustrations 为这篇中文文章设计并生成 5 张不鸭不咋样小漫画正文配图。
```

---

## 怎么用

```text
Use $buya-illustrations 先不要生图。
请分析下面这篇文章哪里值得配图，输出 5 张左右的 shot list。
每张图写清楚：放在哪段后、主题、核心意思、情绪关键词、小漫画分镜格式、构图类型、建议中文旁白。

<粘贴文章>
```

```text
Use $buya-illustrations 把下面这篇文章生成 4 张不鸭不咋样小漫画正文配图。
要求：16:9 横版、粗黑漫画分镜、白色长脖子鸭、橙色扁嘴、小点眼、手写对白框。鸭群和浅绿背景只在适合时使用。

<粘贴文章>
```

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
