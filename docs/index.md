# Editorial Monument Photo

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
cp -R editorial-monument-photo ~/.codex/skills/
```

## Quick prompts

```text
Use editorial-monument-photo to create a 3:4 Shanghai landmark poster.
Hero word: SHANGHAI.
Sunny natural daylight, original building colors, simple foreground.
```

```text
用 editorial-monument-photo 做一张 3:4 北京天坛海报。
主词：BEIJING。
晴天自然光，保留建筑本身颜色，前景简单。
```

## Production note

For exact typography, generate a clean base image first, then overlay text deterministically.
