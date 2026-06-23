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

## The deck (15 slides)

A direct, founder-to-founder story, built to be felt:

1. Cover — **Nora**, your personal AI assistant
2. You didn't start your business to become its back office
3. You know the feeling (the invoice, the forgotten name, the cold lead)
4. From the founder — *"I built Nora because I needed her."*
5. Meet Nora — what she is
6. She lives in the tools you already use
7. Every morning — the briefing
8. Before every call — she remembers everyone
9. All day long — drafts in your voice, you send
10. In the background — she catches what you'd have dropped
11. Getting started (set up for you, live in 30 days)
12. Security & compliance (SOC 2, GDPR, HIPAA, ISO, EU AI Act)
13. What it costs
14. Why now
15. Close — *"Let's give you your time back."*

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
