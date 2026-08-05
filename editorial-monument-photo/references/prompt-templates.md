# Prompt templates

Replace every bracketed field. Remove unused options rather than leaving alternatives in the final prompt.

These templates can be used in any prompt language. Preserve the user's exact hero word and casing. If the target text uses non-Latin scripts or must be production-perfect, prefer the text-free base workflow and deterministic typography overlay.

## Place / landmark

```text
Create a vertical [2:3 / 4:5] editorial poster built around a photorealistic documentary photograph of [SUBJECT] in [LOCATION], seen from [CAMERA POSITION] under [LIGHT / WEATHER]. Preserve its recognizable architecture, materials, proportions, and real-world context. The landmark is the single dominant visual anchor, not a detail inside a busy cityscape. Prefer a closer architectural portrait when a specific landmark is named. The subject occupies the lower [52-62]% of the frame with a clean, believable horizon and restrained surrounding detail. Avoid both oversized landmark crowding and hollow empty-paper compositions.

Keep foreground and context simple: use only [ONE SIMPLE FOREGROUND: water strip / steps / quiet pavement / low planting] plus minimal secondary skyline or trees. Avoid complex foregrounds, dense trees, crowds, many boats, busy bridges, heavy traffic, cluttered street furniture, and competing buildings.

Behind and partially obscured by the subject, set the single exact word “[HERO WORD]” in monumental ultra-condensed grotesk uppercase lettering: very tall proportions, tight tracking, flat muted brick-red ink, spanning nearly the full width and [50-70]% of the canvas height. Keep a clear side safe zone: target 5-8% margin on both left and right, hard minimum 4%, no cropped or edge-stuck first/last letters. For long city names, use tighter ultra-condensed type before shrinking the landmark too much. Rooflines, towers, trees, or foreground edges naturally interrupt the letters so typography and photograph share real depth. Keep the word legible in one second.

Art direction: warm ivory matte paper, brick/cinnabar red, charcoal and stone neutrals, low saturation, controlled contrast, soft highlight roll-off, subtle offset-lithograph grain and slight ink-density variation, cultured museum-catalogue restraint, axial composition, generous negative space. Add no secondary readable text unless explicitly supplied.

Avoid: [PASTE ALWAYS AVOID LIST]. Do not invent dates, coordinates, logos, seals, history, or extra words. Exact readable text: “[HERO WORD]” only.
```

## Real scene / interior / street

```text
Create a vertical [RATIO] art-book editorial image of a real [SCENE TYPE] in [LOCATION / CONTEXT], photographed at eye level with [LIGHT], true materials, natural depth, and quiet lived-in details. Choose one strong visual anchor: [ANCHOR]. Keep the scene simple and visually quiet so the anchor dominates. Use only minimal foreground context and avoid complex foregrounds, dense trees, crowds, many boats, busy bridges, heavy traffic, cluttered street furniture, and competing buildings. Keep the image documentary and plausible, not staged advertising.

Build the composition around the exact word “[HERO WORD]” in huge ultra-condensed uppercase brick-red lettering placed behind the main scene. Let [DOORWAY / PERSON / FURNITURE / TREE / OBJECT] overlap selected letter edges, creating convincing foreground-background depth. Warm paper field, charcoal and stone, muted red, fine art-book print grain, low saturation, restrained symmetry, sparse museum editorial rhythm. No extra readable copy.

Avoid: [PASTE ALWAYS AVOID LIST]. Exact readable text: “[HERO WORD]” only.
```

## Environmental portrait

```text
Create a vertical [2:3 / 4:5] environmental editorial portrait of a real [AGE RANGE] [PERSON / ROLE] in [LOCATION / SETTING]. [POSE AND ACTION]. Eye-level [THREE-QUARTER / FULL-BODY] camera, [LENS FEEL], natural [LIGHT], realistic skin pores, hair, hands, fabric, and body proportions. Expression: [QUIET CONFIDENCE / THOUGHTFUL / COMPOSED]. Wardrobe: [MATTE NATURAL-MATERIAL CLOTHING]. The setting remains clearly recognizable and supports the person’s story.

Behind the person, set the single exact word “[HERO WORD]” in monumental ultra-condensed grotesk uppercase lettering, flat muted brick-red, filling [50-70]% of the frame. The body and environmental foreground naturally cover parts of the letters while the face remains fully clear; typography feels built into the composition, never pasted on.

Art direction: warm ivory paper, brick red, charcoal, stone, optionally muted sage; low saturation; controlled editorial contrast; subtle offset-lithograph grain; soft highlight roll-off; cultured independent magazine and museum-catalogue restraint; generous negative space; no glamour retouching and no advertising smile. Add no secondary readable text.

Avoid: [PASTE ALWAYS AVOID LIST], beauty filter, plastic skin, fashion-runway pose, exaggerated expression, text crossing eyes or mouth. Exact readable text: “[HERO WORD]” only.
```

## Text-free base for deterministic overlay

Append this instruction when exact typography will be added later:

```text
Do not render any letters or words. Reserve a clean, high-contrast background typography zone occupying [AREA], and preserve natural overlap masks around [SUBJECT EDGES] for later typesetting.
```

## Compact invocation examples

- `用 $editorial-monument-photo 做一张上海街景，主词 SHANGHAI，4:5，阴天纪实。`
- `用 $editorial-monument-photo 做一张女性创始人的环境人物图，主词 BUILDER，暖纸砖红，办公室实景。`
- `用 $editorial-monument-photo 把这座建筑做成复古编辑海报，只保留主词 SUZHOU。`
- `Use $editorial-monument-photo to create a 3:4 portrait poster of a museum curator, hero word MAKER, warm paper and brick-red typography.`
- `Usa $editorial-monument-photo para crear un póster vertical 3:4 de Madrid, palabra principal MADRID, luz natural y tipografía roja detrás del edificio.`
- `Utilise $editorial-monument-photo pour créer une affiche éditoriale 3:4 de Paris, mot principal PARIS, lumière naturelle et sujet photoréaliste.`
