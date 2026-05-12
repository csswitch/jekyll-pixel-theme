---
layout: post
title: "Welcome to Pixel Theme — 8-Bit Jekyll"
date: 2024-01-15
tags: [design, retro, getting-started]
description: "An 8-bit pixel art Jekyll theme with CRT scanlines, boot sequence, HP progress bar, and Press Start 2P font."
---

Welcome to **Pixel Theme** — a Jekyll blog that looks like it was compiled in 1993.

## What You're Looking At

- The font is [Press Start 2P](https://fonts.google.com/specimen/Press+Start+2P) — a pixel-perfect bitmap-style Google Font
- Those horizontal lines across the page are CSS scanlines (a `repeating-linear-gradient` overlay)
- The boot sequence you saw on first load? Pure CSS `@keyframes` — no JavaScript until the sequence ends
- The ❤️ in the top bar tracks your reading progress

## The Palette System

Change your entire color scheme with one config value:

```yaml
pixel:
  palette: "gameboy"   # try: nes | cga | amber | synthwave
```

**gameboy** → classic green-on-black Game Boy LCD  
**nes** → warm cream/blue NES palette  
**cga** → hardcore cyan/magenta CGA monitor  
**amber** → orange amber CRT terminal  
**synthwave** → purple/pink retrowave

## Writing Posts

Create files in `_posts/` with the format `YYYY-MM-DD-title.md`:

```markdown
---
layout: post
title: "My Pixel Post"
date: 2024-01-15
tags: [javascript, tutorial]
description: "Short excerpt shown on the post card."
---

Content here...
```

## Easter Egg 🕹️

There's a hidden easter egg in the theme. Try typing `A`, `B`, `↑`, `↑`, `↓`, `A`, `B` using your keyboard...

*(hint: it's related to the color of everything)*
