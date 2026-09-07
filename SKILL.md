---
name: living-doodle-video
description: Turn an uploaded casual portrait photo into a 30-second video combining a photorealistic moving person with a completely static black-and-white doodle sticker environment, with optional closing text stickers. Use for photo-to-video requests in this mixed-media scrapbook style.
---

# Living Doodle Video

Turn an everyday photo into a quiet, playful mixed-media moment: a real person moves naturally inside a frozen monochrome scrapbook scene.

## User flow

Uploaded photo → styled first frame → 30-second video → optional closing text stickers.

Use English for generation prompts. Keep routine production steps automatic. Ask for the photo when none is attached. Closing text is optional; do not block the base video waiting for it.

## 1. Read the photo and plan the movement

Identify the main person, visible body parts, pose, clothing, handheld items, background objects, available floor space, and framing. Preserve the original aspect ratio, camera position, perspective, and scene layout.

Choose one restrained action sequence that fits the visible scene. Default to breathing, blinking, a gentle head turn, a small hand gesture, or a relaxed shoulder stretch. Keep the subject within the original frame. For close-up or seated portraits, use movement supported by the visible anatomy rather than inventing a full-body walking scene.

Use the example of placing an item on a table, standing up, walking to a window, and stretching only when the photo contains the required item, table, window, and enough visible space. Simplify movements before adding scenery. Follow a user-specified action when compatible with these constraints.

Treat a held item as a separate movable foreground prop only when the action requires it. Preserve its appearance and physical contact with the hand. Once placed, keep it stationary. This exception does not authorize motion in the environment.

## 2. Create the styled first frame

Preserve the person's identity, face, natural skin color, hair, body proportions, original pose, clothing and footwear details, and handheld items. Retain photographic texture and sharpness. Do not turn the person into an illustration or sticker.

Convert only the environment into flat, minimalist black-and-white hand-drawn sticker cutouts. Use thin black outlines, solid black shadow shapes, white interiors, crisp white cut borders, and restrained scrapbook overlap. Keep scene objects recognizable and in their original positions. Use pure black and white within illustrated elements, with no gradients. Preserve the photo's dominant background base color as a flat backing layer; distinguish that backing from the monochrome stickers.

Perform this environment transformation once, before animation. Use the resulting image as the locked scene reference for the video. The instruction to freeze the background applies to this styled reference, not to the original unstyled environment.

### Image prompt template

Adapt the bracketed content to the actual photo before submitting:

“Strictly preserve the photographed person's identity, facial features, natural skin tone, hair, body proportions, original pose, clothing, footwear, and handheld items. Transform the surrounding environment into a minimalist monochrome doodle sticker collage. Depict [observed environment] using thin black contour lines, flat white interiors, solid black shadow shapes, and crisp white cutout borders with subtle scrapbook layering. Preserve the original object placement, scale, perspective, framing, and dominant background base color as a flat backing layer. Keep the person fully photorealistic, with natural lighting, authentic fabric texture, and crisp photographic detail. Render all illustrated elements in pure black and white with flat fills.”

## 3. Animate a 30-second scene

Use the styled image as the first frame and visual reference. Keep the camera completely fixed: no zoom, pan, tilt, dolly, reframing, or cuts. Freeze every environmental outline, sticker border, object, backing color, and perspective relationship for the full duration. Only the person and any explicitly designated handled prop may move. Keep background shadows and lighting static.

Use this default timing, adapting the movement to the photo:

| Time | Action |
| --- | --- |
| 0–5 seconds | Establish the original pose with subtle breathing and blinking. |
| 5–15 seconds | Perform one gentle, scene-appropriate primary action. |
| 15–25 seconds | Continue with a small connected gesture or relaxed stretch. |
| 25–30 seconds | Settle into a comfortable pose with minimal natural movement; optionally display closing text. |

Keep motion smooth, unhurried, and anatomically plausible. Preserve face, clothing, body proportions, hand structure, and prop continuity throughout. Avoid large gestures that require unseen anatomy or extensive reconstruction behind the subject.

### Video prompt template

“Create a 30-second continuous video from this styled reference image. Strictly preserve the composition, framing, perspective, photographic identity, clothing details, and mixed-media textures. Lock the camera in place. Keep the entire doodle sticker environment and its backing color completely frozen, with identical contours, borders, object positions, and lighting throughout. Animate only the realistic person [and the designated handheld prop, when applicable]. During seconds 0–5, [subtle opening motion]. During seconds 5–15, [primary action supported by the photo]. During seconds 15–25, [small connected gesture]. During seconds 25–30, [settling pose]. Use restrained, smooth movement with stable facial features, anatomically consistent limbs and hands, and crisp photographic detail. Maintain the illustrated environment as a single locked background plate throughout.”

## 4. Add optional closing text stickers

When requested, add the user's exact wording as a separate overlay during seconds 26–30, within the existing 30-second runtime. Use legible black lettering on a white paper-cut sticker with a thin black border. Position it in available negative space clear of the face, hands, and key action. Use a simple entrance followed by a static hold. The overlay is separate from the frozen environment and must not move or redraw its stickers.

Prefer adding text after video generation for spelling accuracy and editability. Keep a clean version when practical. When text is requested without wording, propose a short scene-appropriate phrase; when no text is requested, deliver the clean ending.

## Execution and verification

Use available image-editing and image-to-video tools according to their actual capabilities. Check supported duration and export resolution before submitting. When native 30-second generation is unavailable, use supported continuation with the same reference and matching boundary frames, then assemble an exact 30-second timeline. Do not fill the duration with repeated loops or a long freeze unless requested.

A prompt alone cannot guarantee a pixel-stable background. Prefer motion masks or a locked background layer when supported. For compositing workflows, prepare one clean background plate before animation so newly exposed areas stay consistent; composite the moving person and authorized prop over that same plate throughout. Never regenerate exposed background independently per frame.

If video generation is unavailable, state the limitation and provide the completed image prompt, timed action plan, and video prompt. Do not claim a rendered video exists. Do not claim 8K output unless the actual export supports and achieves it; prioritize stable photographic detail at the supported resolution.

Inspect the opening, action transitions, and ending, and review playback for background drift, camera movement, flicker, blur, facial changes, hand or limb distortion, and text errors. Verify the exported duration is 30 seconds. Simplify the action or repair the affected segment when needed; do not launch an unlimited retry loop. Disclose material remaining defects.

Deliver the actual video when available, with a brief note about the optional text ending. Save generated deliverables through the environment's required artifact workflow.
