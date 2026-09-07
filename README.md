# Living Doodle Video

Turn an everyday portrait photo into a 30-second mixed-media video: the real person moves naturally while the surrounding environment becomes a completely static black-and-white doodle sticker collage.

## 中文介绍

**Living Doodle Video** 是一个面向日常人物照片的通用视频生成 Skill。用户只需上传一张随手拍照片，它会在严格保留真人五官、肤色、身材比例、服装、动作与手持物品的基础上，将周围环境转化为扁平、极简的黑白手绘贴纸场景，并生成一段 30 秒的动态视频。

视频全程采用固定镜头，背景贴纸、物体位置、透视关系、光影和底色保持静止，仅让真实人物完成与原图场景相符的自然动作。Skill 会根据照片中实际可见的姿势、空间和物品自动调整动作幅度，减少人物变形、肢体崩坏、背景重绘和画面闪烁。视频最后还可以加入文字贴纸，用于生活记录、社交媒体内容、创意短片和混合媒介视觉表达。

**使用流程：** 上传随手拍照片 → 生成黑白涂鸦贴纸风格首帧 → 生成人物自然运动的 30 秒视频 → 添加可选的结尾文字贴纸。

## What it does

Living Doodle Video guides an image-to-video workflow that keeps the photographed subject realistic and recognizable while transforming the environment into a flat scrapbook-style scene.

- Preserves the subject's identity, face, skin tone, body proportions, pose, clothing, footwear, and handheld objects
- Converts only the environment into minimalist black-and-white hand-drawn sticker cutouts
- Locks the camera, composition, perspective, background, lighting, and sticker outlines
- Animates only the real person and an explicitly designated handheld prop
- Adapts movement to the anatomy, objects, and space visible in the uploaded photo
- Produces an exact 30-second timeline
- Supports an optional closing text sticker during the final four seconds

## Workflow

```text
Upload a casual photo
        ↓
Create the styled first frame
        ↓
Generate a 30-second character animation
        ↓
Add an optional closing text sticker
```

### 1. Upload a photo

Use a casual portrait or full-body photo with one clear main subject. Photos with visible surroundings and enough room for small natural movements work best.

### 2. Create the styled first frame

The subject remains photorealistic. The surrounding environment is converted into monochrome doodle stickers with thin black contours, white interiors, solid black shadow shapes, crisp white cut borders, and subtle scrapbook layering.

### 3. Generate the video

The Skill builds a restrained action sequence based on the uploaded image. It uses blinking, breathing, a gentle head turn, a small hand gesture, or a relaxed stretch when larger actions are unsupported by the frame.

| Time | Default behavior |
| --- | --- |
| 0–5 seconds | Hold the original pose with subtle breathing and blinking |
| 5–15 seconds | Perform one gentle primary action supported by the photo |
| 15–25 seconds | Continue with a small connected gesture or relaxed stretch |
| 25–30 seconds | Settle into a comfortable ending pose |

A sequence such as placing an item on a table, standing up, walking to a window, and stretching is used only when the original photo contains the required item, table, window, visible anatomy, and sufficient space.

### 4. Add closing text

Closing text is optional. When requested, it appears during seconds 26–30 as black lettering on a white paper-cut sticker with a thin black border. Post-production text overlays are preferred for spelling accuracy and editability.

## Use the Skill

Upload a photo and invoke the Skill with a request such as:

```text
Use $living-doodle-video to turn this photo into a 30-second video.
Keep the person photorealistic, freeze the monochrome doodle background,
and end with the text sticker “A Quiet Little Moment.”
```

You can also specify a motion:

```text
Use $living-doodle-video to create a 30-second video from this photo.
Have the person place the cup on the table, stand up slowly, walk toward
the window, and finish with a relaxed stretch.
```

The Skill will simplify or adapt the requested movement when the source image does not visually support the full sequence.

## Visual rules

The output follows four core constraints:

1. **Photographic subject**  
   The person retains realistic facial features, skin texture, clothing detail, and natural proportions.

2. **Frozen illustrated environment**  
   Background stickers, object positions, contours, borders, backing color, lighting, and perspective remain fixed for the full video.

3. **Fixed camera**  
   The shot contains no zoom, pan, tilt, dolly, reframing, or cuts.

4. **Restrained motion**  
   Movement remains smooth, natural, anatomically plausible, and compatible with the visible scene.

## Quality checks

Before delivery, the workflow checks:

- Exact 30-second duration
- Stable facial identity and body proportions
- Consistent hands, limbs, clothing, and handheld props
- No background drift, sticker redrawing, camera motion, flicker, or unexpected blur
- Correct spelling and placement of optional closing text

For the strongest background stability, use a video tool that supports motion masks, locked background layers, or foreground compositing. Prompting alone may not produce a pixel-identical background across every frame.

## Repository structure

```text
Living-Doodle-Video-Skill/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── assets/
    └── icon.svg
```

- **SKILL.md** contains the complete workflow, prompt templates, timing rules, and verification guidance.
- **agents/openai.yaml** defines the Skill's display metadata and invocation behavior.
- **assets/icon.svg** provides the Skill icon.

## Output requirements

The rendered result depends on the capabilities and limits of the available image and video generation tools. If a tool cannot generate 30 seconds natively, the workflow uses matched continuation segments and assembles them into one 30-second timeline. Resolution claims are based on the actual export rather than prompt wording.
