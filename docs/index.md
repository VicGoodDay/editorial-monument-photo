# Editorial Poster

Stable image-direction skill for editorial monument posters.

## Core idea

Turn a real place, landmark, street scene, interior, or person into a disciplined editorial poster:

- photorealistic subject
- one monumental hero word
- warm ivory paper
- muted brick-red typography
- subject-over-type depth
- restrained museum / art-book composition

## Install

Copy the skill folder into your Codex skills directory:

```bash
cp -R editorial-poster ~/.codex/skills/
```

## Quick prompts

```text
Use editorial-poster to create a 3:4 Paris landmark poster.
Hero word: PARIS.
Sunny natural daylight, original building colors, simple foreground.
```

```text
用 editorial-poster 做一张 3:4 巴黎埃菲尔铁塔海报。
主词：PARIS。
晴天自然光，保留铁塔和城市本身颜色，前景简单。
```

## Production note

For exact typography, generate a clean base image first, then overlay text deterministically.

## Color

The default palette is warm ivory background plus brick-red hero typography. You can specify a background color or brand palette; keep the result restrained, with one background color, one hero-word color, and natural subject colors.
