# Mad Rooms — Generative Art

> A seed-based generative system for layered-grid compositions.  
> A reproducible catalogue of computational room studies.

---

## What is this?

**Mad Rooms** is a generative design system that builds a grid — between three and forty columns, three and forty rows — and fills each cell with a stack of layered rectangles. Every rectangle is drawn with a seeded offset from its neighbours, traced with a glowing stroke, and tinted from a shared foreground palette. The result is a field of *rooms within rooms*: frames that repeat without ever aligning.

Every artwork in this catalogue is defined by a single numeric seed. The same seed always produces the identical composition — making each piece **traceable, reproducible, and licensable** across textile, print, and apparel applications.

Named for the sense of depth and enclosure that emerges from stacked, offset frames, **Mad Rooms** reframes the grid as architecture.

---

## Live

🌐 **[View the catalogue →](https://reyrove.github.io/Mad-Rooms/)**

---

## The System

The generator combines two layers:

| Layer | Description |
|-------|-------------|
| **Grid** | A seeded columns × rows lattice, from 3×3 up to 40×40 cells. |
| **Stacks** | Each cell contains 1 to 9 nested rectangles, each drawn with its own offset, colour, and glow. |

Both layers are driven by the same seed, ensuring deterministic output.

### Parameters

- **Grid dimensions** — 3 to 40 columns × 3 to 40 rows
- **Rooms** — one per cell (up to 1,600)
- **Rectangles per room** — 1 to 9
- **Offset range** — up to half the cell's smaller dimension
- **Stroke glow** — `cellWidth / 10` shadow blur
- **Background** — drawn from 27 curated dark tones
- **Foreground palette** — drawn from 44 curated colour sets (2–8 colours each)

---

## Structure

```
Mad-Rooms/
├── index.html              ← Full catalogue (single-file)
├── images/
│   ├── fav.svg
│   ├── madrooms-tote.png
│   ├── madrooms-cushion.png
│   └── ...
├── Mad-Rooms.jpg           ← Apparel mockup
└── README.md
```

The entire project is contained in a single `index.html` — no build step, no dependencies, no framework. Open it in any modern browser.

---

## Features

- **Seed-based generation** — every composition is deterministic and reproducible
- **Live catalogue** — cover, statement, plate, surfaces, process, archive, commission sections
- **Multiple surfaces** — print, scarf, textile, wallpaper — all rendered from the same seed
- **Archive of 8 seeds** — click any plate to load it into the main view
- **PNG export** — download any composition directly from the browser
- **Keyboard shortcuts** — `R` for new seed, `S` to save
- **Legal modal** — licensing, terms, and credits built in
- **Responsive** — works on desktop, tablet, and mobile
- **Mobile-first navbar** — horizontally scrollable with fade hint

---

## Usage

### Generate a new composition

Click **New Seed** or press `R`.

### Download the current composition

Click **Download** or press `S`.

### Load a seed from the archive

Click any plate in the **Archive** section.

---

## Color System

Every composition is drawn from two curated palettes:

- **Background** — one of 27 dark tones (blacks, deep blues, teals, muted reds, charcoals) chosen per seed
- **Foreground** — one of 44 curated sets, each containing 2 to 8 harmonious or contrasting colours

Each rectangle within a cell picks its stroke colour at random from the foreground set. Because the offsets and colours are both seeded, no two compositions share the same rhythm of line and hue.

---

## Technical Notes

- Pure vanilla JavaScript — no libraries
- Canvas 2D rendering
- Custom xorshift random generator for deterministic seeds
- Device-pixel-ratio aware rendering
- Fully static rendering — one seed produces one composition, no animation loops
- Single `renderStatic()` function drives the cover, plate, framed print, all four surfaces, and all eight archive thumbnails
- Glow via `shadowColor` + `shadowBlur` per rectangle stroke
- `prefers-reduced-motion` respected

---

## About

**Mad Rooms** is a project by [Reyhaneh Daneshdoost](https://reyrove.github.io/) — an Iranian-born artist working at the intersection of classical textile logic and generative systems.

The work begins with a simple observation: the woven surface — repetitive, mathematically structured, infinitely variable — has always been a form of computation, long before computers.

**Mad Rooms** is an attempt to render that logic visible.

> *A room is a frame — and a frame drawn inside itself never quite stays in place.*

---

## Licensing

All compositions are seed-documented and available for licensing across textile, surface, and apparel applications.

For commercial use, custom editions, or exclusive rights:

📧 **reyhanehdaneshdoost@gmail.com**

See the **Licensing** section in the live catalogue for details.

---

## Links

- 🌐 [Website](https://reyrove.github.io/)
- 📷 [Instagram](https://www.instagram.com/rey._.rove/)
- 💼 [LinkedIn](https://www.linkedin.com/in/reyhaneh-daneshdoost-730481160/)
- 🐦 [X](https://x.com/reyrove)

---

## Credits

**Design & Generative System**  
Reyhaneh Daneshdoost

**Typefaces**  
Cormorant Garamond · DM Mono

**Edition**  
Mad Rooms — Autumn 2026

---

<p align="center">
  <em>Generative Layered Grid</em><br />
  <sub>© Reyrove Studio · All compositions reproducible by seed</sub>
</p>