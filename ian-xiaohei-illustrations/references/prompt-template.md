# 生图提示词模板

每张图单独生成。根据正文内容替换变量，不要把多张图拼在一起。

```text
Generate one standalone 16:9 horizontal Chinese article illustration.

Visual DNA:
Pure white background. Thick rounded black hand-drawn line art. Large empty white space. Simple sticker-like Chinese internet meme feeling. Minimal colors: white duck body, orange beak and feet, tiny black dot eyes, sparse pink/green/blue accents only when needed. No gradients, no shadows, no paper texture, no complex background, no commercial vector style, no PPT infographic look, no realistic UI, no 3D, no plush toy, no realistic animal.

Recurring IP character required:
“不鸭不咋样”, a minimalist Chinese sticker-style white duck character. It has a long simple neck, rounded head, puffy cheek, thick black outline, flat orange beak, tiny black dot eyes, simplified white body, and goofy deadpan expression. The duck should feel silly, cute, meme-like, slightly absurd, and emotionally expressive, but still clean and minimal. It should not become a realistic duck, plush toy, 3D mascot, detailed animal, or polished commercial vector illustration.

Theme:
{正文配图主题}

Emotion / meme point:
{这张图对应的情绪或梗点：无语 / 得意 / 委屈 / 嘴硬 / 卡住 / 装懂 / 拖延 / 被迫营业 / 过载 / 假装没事}

Core idea:
{这张图要表达的核心意思}

Buya-style scene type:
{情绪替身 / 生活梗 / 道具隐喻 / 表情包短句 / 小漫画分镜}

Composition:
{具体画面：不鸭不咋样在哪里、姿势是什么、正在做什么、主道具是什么、情绪如何表达}

Suggested props:
{道具1} / {道具2} / {道具3，可选}

Chinese handwritten phrase:
{一句 2-6 个字的中文短句；可为空；不要长段文字}

Expression rule:
Use body posture, flat orange beak shape, tiny dot eyes, blush, sweat drops, motion marks, small hearts, sparks, or one short handwritten Chinese phrase to express mood. The duck should behave like an internet sticker reacting to the concept, not like a serious diagram operator.

Color use:
Black for thick outlines, dot eyes, short phrase, and main object outlines. White for the duck body. Orange for beak, feet, and at most a few action marks. Pink for blush or tiny hearts. Light green or light blue only for simple clothes, books, blocks, or small props. Keep colors sparse and flat.

Constraints:
One image explains only one emotional scene or meme-like metaphor. Keep the main subject around 35%-55% of the canvas. Preserve at least 40% blank white space. Use at most one short Chinese phrase, ideally 2-6 Chinese characters. Do not write a title in the top-left corner. Do not write the structure type on the image. Do not make it a formal diagram, course slide, dense explainer, system architecture, or PPT infographic. Do not copy any reference image, original text, date, watermark, platform ID, outfit, prop, or exact composition. It should feel like a clean, funny, minimal Chinese sticker-style duck illustration inserted into an article.
```

## 图像编辑提示

去掉左上角标题：

```text
Edit the provided image. Remove only the handwritten title "{要删除的文字}" and its underline from the top-left corner. Fill that area with the same clean white background, matching the surrounding blank paper. Preserve everything else exactly: character, labels, paths, line style, composition, aspect ratio, and image quality. Do not add any new text or objects.
```

增强不鸭感：

```text
Regenerate this illustration with the same core meaning, but make it much closer to the “不鸭不咋样” sticker style: a white long-neck duck with thick black outline, flat orange beak, tiny black dot eyes, rounded head and puffy cheek, simple goofy emotional posture, large white space, and one very short Chinese phrase. Do not make it a serious diagram or polished mascot.
```
