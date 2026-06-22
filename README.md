# Nora — Your AI Right Hand (MLDI)

Marketing deck for **Nora**, a personal AI agent for small- and medium-business
owners. Nora lives in the owner's phone 24/7, learns their business deeply, and
takes over the invisible admin work — client memory, correspondence, reminders,
money, and noise filtering — so the owner gets their **time** back.

Single-file HTML presentation. `index.html` is the live deck — no build step,
no dependencies. The whole thing (markup, design system, icons, logo, and
navigation logic) lives in one file.

## Quick start

```bash
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

## The deck (22 slides)

1. Cover — *Get back the hours your business quietly takes from you.*
2. The admin runs you (the invisible work, 10–20 hrs/week)
3. It's not your craft, but it never stops
4. What if it just got handled? — *That's Nora.*
5. What Nora is — a personal AI agent in your phone
6. Yours, not theirs — a private agent for you, not a client chatbot
7. Works inside the tools you already use
8. Meet **Nora**
9. Morning briefing
10. Client memory — remembers your people
11. What Nora keeps on every client
12. Draft replies — in your voice, you send
13. Reminders — who, when, why
14. Memory for money
15. Noise filter
16. Voice or text, anywhere
17. One assistant, your entire operation
18. How we set up your Nora (5 steps)
19. Privacy & control
20. Investment & timeline
21. Why now
22. Close — *Let's set up your Nora.*

## Design system

Dark theme, fluid `clamp()` typography, and an aurora glow gradient define the
look. Key tokens live in `:root` at the top of `index.html`:

- `--bg: #0d0c0b` · `--text: #f5f2ef` · `--soft: #d8d4cf` · `--muted: #9a9691`
- Aurora glow (`.aurora-top` / `.aurora-bottom`), halftone fades, and the
  layered radial gradients are pure CSS.
- Nora's face, the MLDI monogram, and all utility glyphs (briefing, memory,
  reminders, money, filter, voice, Telegram, etc.) are inline SVG `<symbol>`s
  referenced via `<use>`, several with built-in SMIL animations.

## Editing

Everything is in `index.html`:

- **Content** — each slide is a `<section class="slide" data-slide>` inside
  `<main class="deck">`.
- **Styling** — the `<style>` block in `<head>`.
- **Icons / avatar** — the `<svg>` symbol library near the top of `<body>`.
- **Navigation** — the `<script>` block at the bottom.

`replica.html` is kept as a pristine reference copy of the original imported
source deck (the Digital Employees version this was repurposed from).
