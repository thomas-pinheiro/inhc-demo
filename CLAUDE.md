# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

Academic presentation for a Human-Computer Interaction course (Bacharelado em Sistemas de Informação, IFAL Maceió, 4º período). The topic is **Reserva de Salas & Manutenção** — a Design Thinking case study proposing a room-booking and maintenance-reporting system for IFAL Campus Maceió.

## Running the presentation

The engine loads slides via `fetch()`, so a static server is required (no `file://`):

```
npx serve .
```

Then open `http://localhost:3000` (or whichever port `serve` picks).

**Keyboard shortcuts:**
- `← →` / `Space` / `PageUp PageDown` — navigate slides
- `T` — toggle table of contents
- `N` — toggle presenter notes
- `F` — toggle fullscreen
- `Home` / `End` — jump to first/last slide
- Touch swipe (50 px threshold) also works

## Architecture

Everything lives in `index.html` — a zero-dependency, self-contained presentation engine.

**Slide loading:** `SLIDE_FILES` (array in `index.html`) lists paths in order. The engine fetches them all via `Promise.all`, parses each with `tmp.firstElementChild`, and appends to `#slides-host` inside `#scaler`. **To add a slide:** create the file and add its path to `SLIDE_FILES`. **To remove a slide:** remove from `SLIDE_FILES` (file can stay on disk).

**Critical parsing rule:** The engine uses `tmp.firstElementChild`, so the `<section>` must be the **first element** in each slide file. Never put a `<style>` or any other tag before it. Inline `<style>` blocks must go **inside** the `<section>`.

**Viewport scaling:** Fixed 1280×720 canvas (`#scaler`) CSS-scaled to fill any screen via `Math.min(innerWidth/1280, innerHeight/720)`. Edit all styles at 1280×720 coordinates. Usable content area per slide: ~1152×520 px (after chrome 62 px top + CTA 78 px bottom + 64 px side padding).

**Slide anatomy:**
```html
<section class="slide [blk-*]" data-title="TOC label" data-cta="Button text"
  data-notes="Presenter notes shown with N key.">
  <!-- optional: <style>...</style> for slide-local CSS -->
  <div class="stage top"> <!-- or .stage for vertical centering -->
    <span class="eyebrow"><span class="dot"></span> Label</span>
    <h2 class="title">Heading</h2>
    <!-- content -->
  </div>
</section>
```

**Block color themes** (set on `<section>`):
- *(none)* — indigo (default)
- `.blk-game` — cyan; also tints `.casebox` border and `.kicker`
- `.blk-ia` — violet; same casebox tinting
- `.blk-end` — green

**CSS design system** (all in `index.html` `<style>`):

| Class | Purpose |
|---|---|
| `.grid.c2/.c3/.c4` | CSS grid layouts |
| `.card` | Bordered card with `.ico`, `h3`, `p` |
| `.cols` + `.col` / `.col.good` / `.col.warn` | 2-col compare (green / red variants) |
| `.casebox` | Highlighted callout box with `.kicker`, `h3`, `p`, `.meta` |
| `.topics` | Icon-bullet list; each `li` is `display:flex` — always wrap text in `<span>` |
| `.crit` | 2-col criteria grid with violet left border |
| `.stat.a/.b/.c` | Colored stat cards (indigo-violet / cyan / dark) |
| `.tl` | Timeline: `.row`, `.when`, `.what` |
| `.pill` / `.pill.hot` | Inline badge (neutral / amber) |
| `.note` + `.b` | Small footnote row with label badge |
| `.path` + `.p` + `.arr` | Breadcrumb-style progress indicator |
| `.tip[data-tip="…"]` | Hover/click tooltip |

**`.topics li` flex rule (critical):** `.topics li` and `.note` are `display:flex`. Any `.tip` or bare text node directly inside them becomes a flex item and breaks spacing. Always wrap surrounding text in a `<span>`:
```html
<!-- correct -->
<li><span class="mk">📌</span><span>Text with <span class="tip" data-tip="…">term</span>.</span></li>
```

**Image lightbox:** Use `.img-gallery` > `.img-thumb` > `img.img-trigger` with `data-src`, `data-alt`, `data-caption`. Galleries with >1 image get arrows automatically; >3 images get dot indicators.

**Step reveals:** Add `.step` to any element inside a slide to hide it initially. Each forward navigation within the slide reveals the next `.step` element (`.show` class toggled by the engine).

## Current slide sequence

| File | Content |
|---|---|
| `01-capa.html` | Cover — team + project hook |
| `02-agenda.html` | Agenda — 4-card overview + path |
| `03-triangulo-intro.html` | Triângulo de Ouro intro (UX / DEV / PM stat cards) |
| `04-triangulo-ux.html` | Desejabilidade — 3×3 positivos/riscos/soluções table |
| `05-triangulo-dev.html` | Capacidade Técnica — same layout |
| `06-triangulo-pm.html` | Viabilidade — same layout; row 2 sol cell is red (org risk) |
| `07-personas-overview.html` | 4 persona mini-cards |
| `08–11-persona-*.html` | Individual personas: profile + pain points + user story |
| `12-user-stories.html` | 6 prioritized user stories in `.crit` grid |
| `13-funcionalidades.html` | MVP features in 3 grouped cards (`.blk-ia`) |
| `14-demo.html` | Demo landing (`.blk-end`) — "Agora começa a Demo" |

The tri-table layout used in slides 04–06 is defined with inline `<style>` classes (`.tri`, `.tri-row`, `.tc`, `.tc.pos`, `.tc.neg`, `.tc.sol`). Since all slides live in the DOM simultaneously, these classes are global — identical definitions across slides cause no conflict.
