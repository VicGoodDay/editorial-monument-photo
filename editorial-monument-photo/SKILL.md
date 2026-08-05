---
name: editorial-monument-photo
description: Create restrained editorial poster photographs that combine a photorealistic place, landmark, interior, street scene, or person with monumental condensed typography, warm paper, brick-red accents, archival print texture, and museum-catalogue microcopy. Use when the user asks for this reference style, retro editorial travel or portrait imagery, real-scene poster photos, monumental word backgrounds, or a stable prompt system for matching this visual family.
---

# Editorial Monument Photo

Create a photorealistic editorial image first, then turn it into a disciplined poster composition. Preserve the visual system across different subjects; do not copy a reference's proper nouns, exact layout, or incidental text.

## Required inputs

Infer reasonable defaults when omitted. Collect only what materially changes the image:

- mode: `place` or `person`
- subject and location/context
- hero word: one short word, ideally 4-10 Latin letters; Chinese may use 2-4 characters
- aspect ratio and platform
- prompt language / output language, if the user has a preference
- exact readable text, if any
- mood/time/wardrobe, when relevant

Use `4:5` for Xiaohongshu by default, `3:4` for vertical social covers when requested, and `2:3` for an editorial poster. The user may prompt in any language. Preserve the user's requested hero word exactly, including casing, accents, spaces, or non-Latin characters.

If the user needs reliable non-Latin text, detailed copy, or production-perfect typography in any language, generate the visual base with only the hero word or no text, then add exact text in a deterministic layout tool.

## Workflow

1. Read [references/style-system.md](references/style-system.md).
2. Choose `place` or `person`, then read the corresponding template in [references/prompt-templates.md](references/prompt-templates.md).
3. Write one complete generation prompt. State subject facts before styling.
4. Use the built-in image generation tool. Treat user images as visual references, not edit targets, unless they explicitly ask for an edit.
5. Inspect the full-size output. Reject if it fails any non-negotiable below.
6. Make at most two materially different retries. Change composition or typography integration, not merely color.
7. Save the final prompt with the selected image when the image belongs to a project.

## Non-negotiable visual grammar

- One unmistakable photorealistic hero subject.
- One monumental ultra-condensed uppercase word forming the background architecture.
- Subject overlaps or interrupts the word; the word does not float like a sticker.
- Hero type keeps a safe margin: target 5-8% from left and right canvas edges, never under 4%, and never visually cropped.
- Landmark scale stays balanced: target 52-62% of canvas height for city landmarks, with 45-65% allowed only when the specific landmark shape requires it.
- Do not solve edge safety by making the subject too small. If negative space exceeds about 30%, increase landmark scale or lower the hero word instead of adding foreground clutter.
- Warm ivory paper ground plus muted brick/cinnabar red, charcoal, stone, and at most one subdued secondary hue.
- Mostly frontal or axial composition, controlled symmetry, generous negative space.
- Fine archival print grain and subtle ink/paper variation; no heavy distress filter.
- Small museum-catalogue annotations stay subordinate and sparse.
- Calm, cultured, precise mood; editorial rather than commercial.

## Place mode

Keep the landmark geographically and architecturally recognizable. Use a believable camera position, natural daylight, restrained atmospheric depth, and documentary detail. The landmark must be the single dominant visual anchor, not one detail inside a busy cityscape. Let the lower 52-62% carry the main building or landmark mass while the hero word dominates the upper field or extends behind the subject. Use 45-65% only as a tolerance band, not the default target.

For city landmark images, keep the picture structure simple. Use only the minimum foreground and context needed to identify place: one clean river/water strip, one quiet street edge, a few trees, or a low secondary skyline. Avoid complex foregrounds, dense trees, crowds, many boats, many vehicles, busy bridges, cluttered street furniture, and competing buildings that pull attention away from the landmark. Prefer closer architectural portraits when the landmark is the user's stated subject.

Composition safety rule: long city names need tighter type, not edge-cropping. Keep the full hero word inside the safe zone, then balance by setting the landmark to a medium-close scale. Reject outputs where the word touches the edge, the landmark feels oversized, or the image feels empty after scaling down the landmark.

## Person mode

Use a real, specific adult with natural anatomy, skin texture, hands, and expression. Favor a three-quarter or full-body environmental portrait, eye-level camera, quiet confidence, and clothing with tactile natural materials. Keep the face unobstructed. The person must feel photographed in a real place, not composited onto a fashion template.

## Text policy

- Render only the exact hero word unless the user explicitly supplies other copy.
- Never invent dates, coordinates, history, quotations, seals, logos, or pseudo-language.
- Do not ask the image model to typeset paragraphs.
- For final publishable typography in Chinese, Japanese, Korean, Arabic, Devanagari, accented Latin, or any detailed multi-word copy, generate a clean visual base and overlay verified text afterward.
- For multilingual use, write the generation prompt in the user's language when useful, but keep core visual grammar unambiguous: `monumental ultra-condensed uppercase lettering`, `safe margins`, `behind the subject`, and `exact readable text only`.

## Negative constraints

Always include the applicable avoid list from [references/style-system.md](references/style-system.md). Explicitly exclude generic tourism ads, glossy luxury campaigns, cyberpunk, orange-teal grading, red-yellow shock posters, sticker collages, fake film borders, excessive scratches, illegible filler text, duplicate architecture, warped faces/hands, and pasted-on typography.

## QA gate

Pass only when all are true:

- The subject is recognizable and photorealistic.
- The hero word is legible in one second and belongs to the composition.
- The hero word respects safe margins and is not cropped or edge-stuck.
- There is one dominant message and one visual anchor.
- The landmark fills the frame enough to avoid a hollow poster, but not so much that it crowds the type.
- City landmark foreground is simple and does not compete with the landmark.
- Palette, grain, and contrast feel printed and restrained.
- No extra readable words, invented facts, malformed letters, or anatomy defects.
- The result remains distinctive at thumbnail size.

If the model cannot render the exact word cleanly, keep the photograph and typography space, remove generated text, and add the word deterministically. Do not call a typoed render final.
