---
layout: post
title: "CSS Pixel Art Techniques — No Images Required"
date: 2024-01-22
tags: [css, tutorial, pixel-art, design]
description: "How to build pixel art UI components using only CSS box-shadows, repeating gradients, and image-rendering: pixelated."
---

Real pixel art — in CSS, without a single image file. Here's how Pixel Theme achieves the look.

## The Core Trick: `image-rendering: pixelated`

This CSS property tells the browser to scale images (and the element) without anti-aliasing:

```css
img {
  image-rendering: pixelated;
  image-rendering: crisp-edges; /* Firefox */
}
```

Pair this with small SVGs or emoji and you get crisp scaled sprites.

## Tiled Background Grid

The pixel grid background is a pure CSS double repeating-gradient:

```css
.pixel-bg {
  background-image:
    repeating-linear-gradient(
      0deg,
      transparent,
      transparent 7px,
      rgba(48,98,48, 0.3) 7px,
      rgba(48,98,48, 0.3) 8px
    ),
    repeating-linear-gradient(
      90deg,
      transparent,
      transparent 7px,
      rgba(48,98,48, 0.3) 7px,
      rgba(48,98,48, 0.3) 8px
    );
}
```

Two perpendicular `repeating-linear-gradient` layers create a 8×8 grid. The grid line is 1px wide, the cell is 7px wide.

## Pixel Button with Depth

The "inset pixel shadow" effect:

```css
.btn-pixel {
  box-shadow: 4px 4px 0 rgba(0,0,0,0.8);
  transition: box-shadow 0.08s, transform 0.08s;
}

.btn-pixel:hover {
  box-shadow: 2px 2px 0 rgba(0,0,0,0.8);
  transform: translate(2px, 2px);
}

.btn-pixel:active {
  box-shadow: 0 0 0 rgba(0,0,0,0.8);
  transform: translate(4px, 4px);
}
```

The button *moves* toward the shadow as you click — it feels physically pressed.

## CRT Scanlines

```css
.scanlines {
  position: fixed;
  inset: 0;
  pointer-events: none; /* critical — don't block clicks */
  background: repeating-linear-gradient(
    0deg,
    transparent,
    transparent 3px,
    rgba(0,0,0,0.08) 3px,
    rgba(0,0,0,0.08) 4px
  );
  animation: flicker 8s infinite;
}

@keyframes flicker {
  0%, 95%, 100% { opacity: 1; }
  96%, 98%      { opacity: 0.97; }
  97%           { opacity: 0.92; }
}
```

The `flicker` keyframe is subtle — a barely-perceptible opacity dip every 8 seconds. Your eye catches it peripherally, adding analog authenticity without being distracting.

## Pixel Card Inset Shadow

```css
.post-card {
  box-shadow:
    inset -2px -2px 0 rgba(0,0,0,0.5),   /* bottom-right darkens */
    inset  2px  2px 0 rgba(255,255,255,0.1); /* top-left highlights */
}
```

Two inset shadows on opposite corners simulate a beveled 3D edge without any border-image tricks.

## Floating Sprite Animation

```css
@keyframes float {
  0%, 100% { transform: translateY(0); }
  50%      { transform: translateY(-8px); }
}
```

The key is using exactly `8px` — matching the pixel grid. Floating on a non-pixel boundary feels wrong; 8px feels intentional.
