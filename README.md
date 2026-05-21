# Star Beauty Supply -- Website Pitch

**Client:** Star Beauty Supply (7 locations, Chicago, IL)
**Agency:** CY Studios
**Deliverable:** Three distinct website concepts -- static HTML, no backend, no build step

## Concepts

1. **Editorial Premium** -- Magazine-worthy sophistication with warm gold accents and sharp editorial typography. Aesop meets the South Side.
2. **Vibrant Modern** -- Bold, dark-theme, orange-accented energy. TikTok-era beauty supply with real personality and motion.
3. **Neighborhood Trusted** -- Warm, cream-toned, community-first. The website equivalent of walking into a store where they know your name.

## Structure

```
/
├── README.md
├── research/
│   ├── findings.md          # 8-site competitive analysis
│   └── visual-references.md # Photo, font, and style anchors per concept
├── design-system.md         # Binding design specs per concept
├── shared-content.md        # Copy, locations, products, component specs
├── concepts/
│   ├── 01-editorial-premium/
│   ├── 02-vibrant-modern/
│   └── 03-neighborhood-trusted/
└── pitch/
    └── presenter-notes.md
```

## How to View

Each concept folder contains a standalone `index.html` and `join.html`. Open in any modern browser. No server required.

## Tech

- Static HTML + inline CSS + vanilla JavaScript
- Google Fonts (loaded via `<link>`)
- Unsplash images (via direct URL)
- No frameworks, no build tools, no dependencies
