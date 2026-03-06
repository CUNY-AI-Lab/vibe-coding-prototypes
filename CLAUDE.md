# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

A static slide deck for **CAIL Spotlight Workshop #2: Vibe-Coding Prototypes**. No build tools, no bundler, no framework — just vanilla HTML, CSS, and JS served as static files. Deployed via GitHub Pages from the `main` branch at `cuny-ai-lab.github.io/vibe-coding-prototypes`.

## Architecture

- **`index.html`** — Single-file slide deck. All slides are `<section class="slide">` elements inside `<main>`. All CSS is inlined in `<style>`. No external stylesheets.
- **`src/slides.js`** — Slide engine: keyboard/touch/scrubber navigation, progressive fragment reveal (`.frag` class), overview mode (Escape key), hash-based routing.
- **`src/chladni.html`** — Standalone canvas animation embedded as an iframe in the title slide.
- **`SLIDES.md`** — Plain-text mirror of slide content. Must stay in sync with `index.html` whenever slide text changes. Includes slide count in the last line.
- **`img/`** — Logo assets referenced by the title slide.

## Slide System Conventions

- Slides are counted dynamically from `document.querySelectorAll('section.slide')`. The JS auto-sets the scrubber `max` and counter text at runtime.
- The hardcoded `max` attribute on `#slide-scrubber` and the `#slider-counter` text in the HTML should match the actual slide count to prevent a flash of wrong values before JS initializes.
- Progressive reveal: add class `frag` to any element inside a `.stage`. Fragments start hidden and appear one at a time on advance (Space/Arrow Right).
- Slide types: regular (content + stage side-by-side), `slide-break` (full-width section dividers), `data-slide="title"` (title layout with iframe stage).
- Stage inner layouts: `.step-grid` (numbered steps), `.stageCenter` (centered text block), `.agenda-table`, `.res-wrap` (resource links).

## Editing Slides

When adding, removing, or reordering slides:
1. Update both `index.html` and `SLIDES.md` together
2. Update the HTML comment numbers (e.g., `<!-- 12 · PUSH TO GITHUB -->`)
3. Update agenda links in slide 2 (`href="#N"` values)
4. Update `max` on `#slide-scrubber` and `#slider-counter` initial text
5. Update the slide count in the `_Last synced` line of `SLIDES.md`

## Development

No install or build step. Open `index.html` in a browser. Use any local server (e.g., `python3 -m http.server`) if the iframe in the title slide needs to load.

## Commit Style

Short, lowercase messages with no sign-off. Examples from this repo:
```
scaffold vibe-coding prototypes deck — spotlight workshop #2
split deploy slide into push + github pages navigation
```
