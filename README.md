# Digital Employees — MLDI

The MLDI internal master deck (**v122**) — a self-contained, single-file HTML
presentation. This is the live, canonical version of the deck and the base we
continue building from.

## Quick start

Open `index.html` in any modern browser. No build step, no dependencies — the
whole deck (markup, design system, icons, logo, and navigation logic) lives in
one file.

```bash
# from the repo root
open index.html        # macOS
xdg-open index.html    # Linux
```

## Navigation

| Action            | Control                                            |
| ----------------- | -------------------------------------------------- |
| Next slide        | `→` · `Space` · `PageDown` · click the right edge  |
| Previous slide    | `←` · `PageUp` · click the left edge               |
| First / last      | `Home` / `End`                                     |
| Fullscreen        | `F`                                                |
| Direct link       | URL hash, e.g. `index.html#9` jumps to slide 9     |
| Touch             | Swipe left / right                                 |

## The deck (24 slides)

1. Cover — *Free your team from the repetitive work they're stuck on.*
2. The problem — your team burns hours on it, you burn money on it
3. What if it just got handled?
4. What a Digital Employee is
5. Works with your tools
6. So what does one actually look like?
7. Meet **Maya** — Content Writer
8. Maya · a little story
9. Maya · already running
10. Maya · the numbers
11. Meet **Tom** — Sales Representative
12. Tom · a little story
13. Tom · already running
14. Tom · the numbers
15. Meet **Dana** — Contract Renewal Specialist
16. Dana · a little story
17. Dana · how she works
18. Dana · the numbers
19. Every Digital Employee runs the same way
20. How we build it (5 steps)
21. Compliance & Deployment
22. Investment & timeline
23. Why now
24. Close — *Let's build your first one.*

## Design system

Dark theme, fluid `clamp()` typography, and an aurora glow gradient define the
look. Key tokens live in `:root` at the top of `index.html`:

- `--bg: #0d0c0b` · `--text: #f5f2ef` · `--soft: #d8d4cf` · `--muted: #9a9691`
- Aurora glow (`.aurora-top` / `.aurora-bottom`), halftone fades, and the
  layered radial gradients are pure CSS.
- The three Digital Employees (Maya, Tom, Dana), the generic bot, the MLDI
  monogram, and all utility glyphs are inline SVG `<symbol>`s referenced via
  `<use>`, several with built-in SMIL animations.

## Editing

Everything is in `index.html`:

- **Content** — each slide is a `<section class="slide" data-slide>` inside
  `<main class="deck">`.
- **Styling** — the `<style>` block in `<head>`.
- **Icons / avatars** — the `<svg>` symbol library near the top of `<body>`.
- **Navigation** — the `<script>` block at the bottom.

`replica.html` is kept as a pristine reference copy of the imported source.
