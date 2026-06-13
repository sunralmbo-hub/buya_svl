# 生图提示词模板

每张图单独生成。根据正文内容替换变量。默认生成“小漫画式正文配图”，不是正式信息图。

```text
Generate one standalone 16:9 horizontal Chinese article mini-comic illustration.

Identity lock comes first:
Before drawing the comic scene, lock the recurring character identity. The character is “不鸭不咋样”, a minimalist Chinese sticker-style white long-neck duck. It should have: a large rounded head, puffy cheek, long simple white neck, simplified white body, thick black hand-drawn outline, tiny black dot eyes with no highlights, flat horizontal orange beak with black outline, goofy blank deadpan expression, and almost no realistic feather/wing/foot detail. Prefer side profile or 3/4 side profile. Do not make it a yellow duck, realistic duck, goose, swan, plush toy, 3D toy, generic mascot, big-eyed cute animal, or realistic bird.

Visual DNA:
Pure white page background. Thick black hand-drawn comic panel borders, slightly uneven. White long-neck duck characters with flat orange beaks, tiny black dot eyes, rounded heads and puffy cheeks. Handwritten Chinese captions inside white rectangular text boxes with thick black outlines. Optional visual motifs: a single duck, two ducks interacting, a small sequence of panels, a duck crowd texture, pale green background blocks, one special duck with a pink crest/blush/mark, small yellow sparkles. No gradients, no shadows, no paper texture, no complex background, no commercial vector style, no PPT infographic look, no realistic UI, no 3D, no plush toy, no realistic animal.

Recurring IP character required:
“不鸭不咋样”, a minimalist Chinese sticker-style white duck character. It has a long simple neck, rounded head, puffy cheek, thick black outline, flat orange beak, tiny black dot eyes, simplified white body, and goofy deadpan expression. The duck should feel silly, cute, meme-like, slightly absurd, and emotionally expressive, but still clean and minimal.

Mini-comic format:
{分镜格式：single panel / two stacked panels / four panels / two-duck interaction / crowd panel plus close-up panel}

Theme:
{正文配图主题}

Emotion / meme point:
{这张图对应的情绪或梗点：普通 / 特别 / 被看见 / 被淹没 / 嘴硬 / 孤独 / 闪光 / 被找到 / 尴尬 / 温柔 / 拥抱 / 犯困 / 假装没事}

Core idea:
{这张图要表达的核心意思}

Composition:
{具体画面：几格漫画、是一只鸭/两只鸭/鸭群/远近切换、文本框放在哪里、情绪如何落点}

Optional duck crowd rule:
Use a duck crowd only when the theme needs “many”, “ordinary”, “crowd”, or “being submerged”. If using a crowd scene, draw many similar white ducks with orange beaks, cropped at panel edges, creating a dense repeated pattern. One special duck may have a pink crest, pink mark, different pose, or extra white space around it.

Chinese handwritten captions:
{每格 0-1 个白色手写文本框；每个文本框一句自然中文；不要长篇说明；不要复制参考图原句}

Color use:
Black for panel borders, duck outlines, dot eyes, text-box outlines, and handwritten text. White for duck bodies and page background. Orange for beaks and tiny feet. Pale green can be used for panel background blocks, especially in crowd scenes. Pink can mark a special duck or tiny emotional marks. Yellow only for small sparkles.

Constraints:
One image explains only one emotional scene or meme-like metaphor. It should look like a hand-drawn Chinese sticker mini-comic, not a diagram. Do not force a duck crowd if the scene works better with one duck, two ducks, or a quiet single panel. Do not write structure labels. Do not make it a formal diagram, course slide, dense explainer, system architecture, or PPT infographic. Do not copy any reference image, original text, date, watermark, platform ID, outfit, prop, or exact composition. Do not include visible watermarks or social media IDs. Keep it simple, funny, gentle, and emotionally clear.
```

## 图像编辑提示

去掉左上角标题：

```text
Edit the provided image. Remove only the handwritten title "{要删除的文字}" and its underline from the top-left corner. Fill that area with the same clean white background, matching the surrounding blank paper. Preserve everything else exactly: character, labels, paths, line style, composition, aspect ratio, and image quality. Do not add any new text or objects.
```

增强不鸭身份相似度：

```text
Regenerate this image with the same composition, but make the duck character much closer to the “不鸭不咋样” identity: white long neck, large round head, puffy cheek, thick black outline, flat horizontal orange beak, tiny black dot eyes, blank goofy expression, simplified white body, no realistic feathers, no big cute eyes, no yellow duck, no 3D toy, no generic mascot. Keep the mini-comic panel style and handwritten Chinese caption boxes.
```

增强不鸭小漫画感：

```text
Regenerate this illustration with the same core meaning, but make it much closer to the “不鸭不咋样” mini-comic style: thick black hand-drawn panel borders, white long-neck duck characters with flat orange beaks and tiny dot eyes, white handwritten Chinese caption boxes, and a gentle meme-like emotional punchline. Use duck crowds, pale green backgrounds, or a special pink-marked duck only when they support the concept. Do not make it a serious diagram or polished mascot.
```
