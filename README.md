# Editorial Poster Skill

A Codex skill for creating editorial poster-style images with a stable visual system: photorealistic subjects, monumental background typography, restrained palettes, clean foregrounds, and strong magazine-cover composition.

It is designed for repeatable image direction rather than one-off prompt luck. Use it when you want city posters, landmark posters, editorial portraits, social media covers, Instagram / Xiaohongshu vertical visuals, travel editorials, cultural posters, or real-scene poster photographs with a consistent look.

## Example outputs

These are generated sample outputs from the skill. They show the intended range: landmarks, city scenes, portraits, custom palettes, and high-impact editorial color systems.

| Landmark / dusty palette | Landmark / charcoal palette |
|---|---|
| ![Paris Eiffel Tower editorial poster](examples/gallery/paris-eiffel-dusty-blue.jpg) | ![New York Empire State Building editorial poster](examples/gallery/new-york-empire-charcoal.jpg) |

| Landmark / classic city poster | Portrait / warm editorial |
|---|---|
| ![Shanghai Oriental Pearl Tower editorial poster](examples/gallery/shanghai-oriental-pearl.jpg) | ![VISION creative director editorial poster](examples/gallery/vision-creative-director.jpg) |

| Portrait / cool editorial | Portrait / cinematic red |
|---|---|
| ![Female DESIGN editorial poster](examples/gallery/female-design-dusty-blue.jpg) | ![Female RED cinematic editorial poster](examples/gallery/female-red-cinematic.jpg) |

## What it creates

The skill helps an AI agent generate poster-style images with a consistent visual system across different subjects:

- city landmark posters
- real street / interior posters
- environmental portrait posters
- social media, Instagram, and Xiaohongshu-style vertical covers
- editorial travel or culture visuals
- brand or concept posters with one strong hero word

It works best when the image has one dominant subject and one short hero word.

## Visual reference system

The style is based on a restrained editorial poster language:

- one photorealistic hero subject: landmark, building, street scene, interior, object, or person
- one monumental ultra-condensed uppercase hero word behind the subject
- subject overlap that makes the typography feel integrated, not pasted on
- warm paper, brick red, terracotta, charcoal, stone, sage, dusty blue, or other restrained palettes
- matte print texture and subtle ink-density variation
- simple foregrounds and clear subject hierarchy
- magazine-cover scale, not tourist-ad clutter

The skill does not copy a specific reference image, designer, place label, logo, or layout. It extracts the reusable design grammar: large type, photographic subject, safe margins, controlled color, and editorial restraint.

## What is inside

The skill includes rules for:

- hero word safe margins
- subject scale
- long-word typography handling
- simple foreground control
- person-vs-place composition
- text reliability and deterministic overlay fallback
- QA rejection criteria
- multilingual prompting
- optional user-specified background colors and restrained palette pairing

## Repository structure

```text
editorial-poster-skill-github/
  README.md
  LICENSE
  examples/
    gallery/
    prompts.md
  editorial-poster/
    SKILL.md
    agents/
      openai.yaml
    references/
      style-system.md
      prompt-templates.md
```

## Installation

Copy the `editorial-poster/` folder into your Codex skills directory.

```bash
cp -R editorial-poster ~/.codex/skills/
```

Then invoke it naturally:

```text
Use editorial-poster to make a 3:4 Paris landmark poster.
Hero word: PARIS.
```

## Recommended usage

For stable results, provide:

- mode: `place` or `person`
- subject / location
- exact hero word
- aspect ratio
- lighting / mood
- background color or palette, if relevant
- prompt language, if relevant
- whether text must be production-perfect

## Prompt examples

### Landmark poster

```text
Use editorial-poster to create a vertical 3:4 poster of the Eiffel Tower in Paris.
Hero word: PARIS.
Sunny natural daylight, keep the original tower and city colors, no vintage grey filter.
Simple foreground, one dominant landmark, safe margins for the hero word.
```

### Custom palette

```text
Use editorial-poster to create a vertical 3:4 poster of the Empire State Building in New York.
Hero word: NEW YORK.
Palette: charcoal background, warm ivory typography, muted red accent.
Keep the building's natural limestone color, simple foreground, no neon or glossy gradient.
```

### Environmental portrait

```text
Use editorial-poster to create a vertical 3:4 editorial portrait of a creative director in a quiet studio.
Hero word: VISION.
Dusty blue-grey background, muted terracotta typography, warm ivory shirt, charcoal jacket.
The person overlaps the hero word; face unobstructed; no extra readable text.
```

### Chinese invocation

```text
用 editorial-poster 做一张 3:4 巴黎埃菲尔铁塔海报。
主词：PARIS。
晴天自然光，保留铁塔和城市原本颜色，不要做旧发灰。
前景简单，一个主体，大字左右留安全距离。
```

## Palette presets

You can use the default warm paper + brick red palette, or specify a custom palette.

Useful open presets:

- `museum-ivory`: warm ivory background, muted brick red hero word, charcoal details
- `cinematic-red`: saturated scarlet background, bone-white hero word, amber rim light, deep charcoal shadows
- `dusty-blue`: dusty blue-grey background, muted terracotta hero word, warm ivory and charcoal neutrals
- `sage-editorial`: grey-green sage background, charcoal hero word, warm ivory highlights, restrained red accent
- `sandstone`: sand / beige background, oxblood or brick-red hero word, natural stone / wood subject colors
- `charcoal-premium`: charcoal background, warm ivory hero word, muted red accent, warm photographic highlights
- `terracotta-sun`: warm terracotta background, pale cream hero word, charcoal shadows, natural subject colors

Color rule: use one dominant background color, one hero-word color, and one neutral/detail color family. Preserve the subject's natural colors unless the user explicitly asks for stylized recoloring.

## Text reliability note

Image models can misspell or distort text, especially in non-Latin scripts or long copy. This skill asks for exact hero words and provides QA rules, but for final publishable typography the most reliable workflow is:

1. Generate the image with clean space and subject overlap.
2. Add the final word deterministically in a layout tool.
3. Validate margins, spelling, and thumbnail readability.

For production-perfect typography, especially detailed Chinese, Japanese, Korean, Arabic, Devanagari, accented Latin, or multi-line copy, generate the visual base first and overlay final text in a layout tool.

## Good outputs should pass this QA

- The subject is recognizable and photorealistic.
- The hero word is legible in one second.
- The hero word is not cropped or stuck to the edge.
- There is one dominant visual anchor.
- The foreground is simple and does not compete with the subject.
- The palette is restrained and print-like.
- There are no invented dates, coordinates, logos, filler text, malformed letters, or distorted anatomy.

## License

MIT. See `LICENSE`.
