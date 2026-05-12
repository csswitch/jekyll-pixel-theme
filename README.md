# Pixel Theme — 8-Bit Jekyll Theme

[![License: csswitch Commercial](https://img.shields.io/badge/license-csswitch%20commercial-blue.svg)](./LICENSE)
[![Buy on Gumroad](https://img.shields.io/badge/Buy-%2449-brightgreen.svg)](https://csswitch.gumroad.com/l/csswitch-pixel)
[![Live Demo](https://img.shields.io/badge/demo-live-orange.svg)](https://csswitch.github.io/jekyll-pixel-theme/)

## 📄 License & Pricing

|  | Free | Paid — $49 |
|--|------|------------|
| Personal / non-commercial site | ✅ | ✅ |
| **Footer attribution required** | ✅ must keep | ❌ removed |
| Commercial / client projects | ❌ | ✅ |
| Future theme updates | ❌ | ✅ |
| Private source repo access | ❌ | ✅ |

**Free to use** on personal projects — just keep the small *"Theme by csswitch"* footer link intact.  
**Buy the $49 license** to remove the attribution, use commercially, and receive future updates.

**[Buy on Gumroad — $49 →](https://csswitch.gumroad.com/l/csswitch-pixel)**

See [LICENSE](./LICENSE) for full terms.

---

[![MIT License](https://img.shields.io/badge/license-MIT-9bbc0f.svg)](LICENSE)
[![Jekyll](https://img.shields.io/badge/jekyll-4.3-9bbc0f.svg)](https://jekyllrb.com)
[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-compatible-9bbc0f.svg)](https://pages.github.com)

> An 8-bit pixel art Jekyll theme with CRT scanlines, boot sequence, HP reading progress, and a Press Start 2P pixel font.

**[Live Demo →](https://csswitch.github.io/jekyll-pixel-theme)**

---

## ✨ Features

- 🕹️ **Press Start 2P** — authentic pixel font from Google Fonts
- 📺 **CRT scanline overlay** — `repeating-linear-gradient` with subtle flicker animation
- 🖥️ **Boot sequence** — matrix-style startup animation on first visit (CSS keyframes)
- 🃏 **Pixel cards** — inset bevel shadow + click-depth button press effect
- ❤️ **HP reading progress** — health bar style progress indicator on posts
- 🎨 **5 color palettes** — gameboy, nes, cga, amber, synthwave
- 🎮 **Floating sprite** — CSS `translateY` hero animation on 8px pixel grid
- 📱 **Fully responsive** — 1–3 column post grid
- ⚡ **Zero dependencies** — vanilla JS only (~3KB)
- 🐙 **GitHub Pages compatible**
- 🥚 **Easter egg** — keyboard sequence triggers palette inversion

## 🚀 Quick Start

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_BLOG.git
cd YOUR_BLOG
bundle install
bundle exec jekyll serve --livereload
```

## ⚙️ Configuration

```yaml
pixel:
  palette: "gameboy"      # gameboy | nes | cga | amber | synthwave
  scanlines: true         # CRT scanline overlay
  cursor_blink: true      # blinking cursor in nav logo
  boot_sequence: true     # boot animation on first visit
  tile_bg: true           # pixel grid background
```

## 🎨 Palettes

| Name | Background | Accent | Vibe |
|------|-----------|--------|------|
| `gameboy` | `#0f380f` | `#9bbc0f` | Classic Game Boy LCD |
| `nes` | `#1a1a2e` | `#e94560` | Warm NES UI |
| `cga` | `#000000` | `#00ffff` | CGA cyan/magenta |
| `amber` | `#0a0800` | `#ff8c00` | Amber CRT monitor |
| `synthwave` | `#0d0015` | `#ff00c8` | 80s retrowave |

## 📄 License

MIT © [csswitch](https://github.com/csswitch)

---

Made with 💚 by [csswitch](https://github.com/csswitch) — distinctive Jekyll themes for developers.
