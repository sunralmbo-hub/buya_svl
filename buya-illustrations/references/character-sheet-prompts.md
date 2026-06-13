# Character Sheet Prompts

这些 prompt 用于先生成 identity-only character sheet，再用最像的一版作为后续小漫画的视觉参考。

不要一开始就生成文章配图。先锁角色，再做分镜。

## 1. 不鸭 identity-only character sheet

```text
Generate a clean identity-only character sheet for “不鸭不咋样”, a minimalist Chinese sticker-style white long-neck duck character.

Canvas:
16:9 horizontal, pure white background, no story scene, no long text, no watermark, no date, no social media UI.

Layout:
Six small hand-drawn panels, arranged in 2 rows x 3 columns. Each panel has a thick black hand-drawn border.

Character identity:
White long-neck duck, large rounded head, puffy cheek, simplified white body, flat horizontal orange beak with thick black outline, tiny black dot eyes with no highlights, goofy blank deadpan expression, thick black marker-like hand-drawn outline. Prefer side profile or 3/4 side profile. The head, long neck, and body should feel like one continuous simple white shape.

Panel poses:
1. side profile neutral standing pose
2. 3/4 profile neutral pose
3. side profile speaking / slightly speechless
4. holding a small blank sign
5. awkward, pretending to be fine
6. special version with a tiny pink crest or pink cheek mark

Style:
minimal Chinese sticker mini-comic character, thick black outlines, flat colors only, white body, orange beak, optional tiny pink mark, no shadows, no gradients, no feather texture, no complex clothes.

Negative constraints:
not a yellow duck, not a realistic duck, not a goose, not a swan, not a 3D toy, not a plush toy, not a generic mascot, no big cute eyes, no eye highlights, no realistic beak, no detailed feet, no detailed wings, no feathers.
```

## 2. 啵鸡 identity-only character sheet

Current reference folders do not explicitly define “啵鸡”, so this prompt treats 啵鸡 as the small companion bird/chick character in the same 不鸭 mini-comic universe. Adjust after the first visual test if the role is wrong.

```text
Generate a clean identity-only character sheet for “啵鸡”, a small companion bird/chick character in the same minimalist Chinese sticker mini-comic style as 不鸭不咋样.

Canvas:
16:9 horizontal, pure white background, no story scene, no long text, no watermark, no date, no social media UI.

Layout:
Six small hand-drawn panels, arranged in 2 rows x 3 columns. Each panel has a thick black hand-drawn border.

Character identity:
Small white or very pale cream bird/chick body, shorter and rounder than 不鸭, large rounded head, small rounded body, tiny black dot eyes with no highlights, flat small orange beak with thick black outline, simple pink crest / pink comb / pink tuft on top of the head, thick black marker-like hand-drawn outline, goofy gentle blank expression. Keep it simple, cute, slightly silly, and emotionally expressive.

Panel poses:
1. front neutral standing pose
2. 3/4 profile neutral pose
3. looking up with blank expression
4. holding a tiny blank sign
5. shy / awkward pose with tiny pink blush
6. beside a blank white space for scale comparison with 不鸭, but do not draw 不鸭 in this panel

Style:
minimal Chinese sticker mini-comic character, thick black outlines, flat colors only, pale body, orange beak, pink crest, no shadows, no gradients, no feather texture, no complex clothes.

Negative constraints:
not a yellow chick, not a realistic chicken, not a rooster, not Angry Birds style, not a 3D toy, not a plush toy, not a generic mascot, no big cute eyes, no eye highlights, no realistic beak, no detailed feet, no detailed feathers.
```

## 3. Combined identity comparison sheet

Use this after generating separate sheets. It helps stabilize the two-character relationship.

```text
Generate a clean two-character identity comparison sheet for “不鸭不咋样” and “啵鸡”.

Canvas:
16:9 horizontal, pure white background, no story scene, no long text, no watermark, no date, no social media UI.

Layout:
Two rows. Top row: 不鸭 only, three poses. Bottom row: 啵鸡 only, three poses. Add only tiny handwritten labels: “不鸭” and “啵鸡”.

不鸭 identity:
White long-neck duck, large rounded head, puffy cheek, simplified white body, flat horizontal orange beak, tiny black dot eyes, thick black outline, goofy blank expression.

啵鸡 identity:
Small pale bird/chick companion, shorter and rounder than 不鸭, tiny black dot eyes, small flat orange beak, pink crest / pink comb / pink tuft, thick black outline, goofy gentle expression.

Relationship rule:
不鸭 should look taller, longer-necked, more duck-like and deadpan. 啵鸡 should look smaller, rounder, more chick-like, with a clear pink crest. They must belong to the same thick black hand-drawn mini-comic universe but remain visually distinct.

Negative constraints:
no realistic animals, no yellow chick, no 3D toy, no plush toy, no big cute eyes, no eye highlights, no detailed feathers, no complex clothes, no background scene.
```

## Testing order

1. Generate 不鸭 sheet alone.
2. Generate 啵鸡 sheet alone.
3. Pick the best version of each.
4. Generate the combined comparison sheet.
5. Use the combined sheet as the visual reference for future comics.

If either character identity is weak, do not proceed to article comics yet.
