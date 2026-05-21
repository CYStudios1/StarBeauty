# Star Beauty Supply -- Design System Contract

Each concept section below is the binding spec. Every hex code, every font weight, every radius value must be followed exactly during build.

---

## Concept 01: Editorial Premium

### Typography

**PRIMARY FONT:** DM Sans
- Weights: 400 (body), 500 (emphasis), 700 (bold UI elements)
- Usage: Body copy, navigation, form labels, product details, buttons
- Letter-spacing: `0.01em` at body sizes, `0` at headlines

**SECONDARY FONT:** Fraunces
- Weights: 300 (display light), 400 (display regular), 700 (display bold)
- Usage: Headlines, section titles, hero text, pull quotes
- Letter-spacing: `-0.02em` at display sizes
- Optical sizing: ON (use `font-variation-settings: 'opsz' 72` for display)

**DISPLAY FONT:** Instrument Serif
- Weight: 400 (regular)
- Usage: Accent text, editorial callouts, special labels (e.g., "Est. 1995")
- Letter-spacing: `0.05em` for uppercase labels

### Type Scale

| Token | Size | Line Height | Font | Weight |
|-------|------|-------------|------|--------|
| display | 72px | 76px | Fraunces | 300 |
| h1 | 56px | 60px | Fraunces | 300 |
| h2 | 40px | 44px | Fraunces | 400 |
| h3 | 28px | 34px | Fraunces | 400 |
| body | 18px | 28px | DM Sans | 400 |
| small | 14px | 20px | DM Sans | 400 |
| label | 12px | 16px | DM Sans | 500 |
| overline | 11px | 16px | Instrument Serif | 400 |

### Color Tokens

| Token | Hex | Usage |
|-------|-----|-------|
| `--bg-primary` | `#FFFDF8` | Main page background -- warm off-white, NOT pure white |
| `--bg-secondary` | `#F3EDE4` | Section alternation, card backgrounds |
| `--fg-primary` | `#1A1612` | Primary text -- warm near-black |
| `--fg-secondary` | `#5C5347` | Secondary text, captions |
| `--fg-muted` | `#9C9183` | Muted text, timestamps, metadata |
| `--accent-primary` | `#C8A97E` | Primary accent -- warm gold. Buttons, links, highlights |
| `--accent-secondary` | `#8B6914` | Secondary accent -- deep gold for hover states |
| `--surface` | `#FFFFFF` | Cards, modals, elevated surfaces |
| `--border` | `#E4DDD3` | Borders, dividers |
| `--border-strong` | `#C8BFB1` | Strong borders, active states |

### Spacing Scale (8pt grid)

`4, 8, 16, 24, 32, 48, 64, 96, 128, 160`

Spacing rules:
- Section padding: `96px` vertical on desktop, `64px` on mobile
- Between major elements: `48px`
- Between related elements: `24px`
- Component internal padding: `16px`--`32px`
- Micro-spacing (icon gaps, label margins): `4px`--`8px`

### Border Radius

**SHARP corners only.** Max `2px`.
- Cards: `0px`
- Buttons: `2px`
- Inputs: `2px`
- Images: `0px`
- Modals: `0px`

### Shadow Language

**No box-shadows.** This concept uses borders and background color shifts for depth.
- Elevation level 1: `1px solid var(--border)`
- Elevation level 2: `1px solid var(--border-strong)` + `background: var(--surface)`
- Hover: border color transitions to `var(--accent-primary)`
- No `shadow-lg`, no `shadow-xl`, no drop shadows anywhere

### Button System

**Primary:**
- Background: `var(--accent-primary)` (`#C8A97E`)
- Text: `var(--fg-primary)` (`#1A1612`)
- Font: DM Sans 500, 14px, letter-spacing `0.08em`, uppercase
- Padding: `14px 32px`
- Border: none
- Radius: `2px`
- Hover: background shifts to `var(--accent-secondary)` (`#8B6914`), text shifts to `#FFFDF8`
- Transition: `400ms ease-out`

**Secondary:**
- Background: transparent
- Text: `var(--fg-primary)`
- Border: `1px solid var(--border-strong)`
- Padding: `14px 32px`
- Hover: border color shifts to `var(--accent-primary)`, text color shifts to `var(--accent-primary)`

**Ghost / Text Link:**
- No background, no border
- Text: `var(--accent-primary)`
- Underline: `1px solid` (persistent, not on hover)
- Hover: text shifts to `var(--accent-secondary)`
- Styled as inline text, not as a box

### Motion Language

| Property | Duration | Easing | Usage |
|----------|----------|--------|-------|
| Default | 400ms | `ease-out` | All transitions |
| Entrance | 600ms | `cubic-bezier(0.22, 1, 0.36, 1)` | Fade-in, slide-up on scroll |
| Exit | 300ms | `ease-in` | Modal close, element removal |

Notes:
- All motion is SLOW and deliberate. Nothing bounces, nothing springs.
- Scroll-triggered reveals use staggered delays: first element 0ms, +100ms per subsequent element
- Hover transitions are immediate-feeling but smooth (400ms)
- No transform scale on hover. Only color/border/opacity changes.

---

## Concept 02: Vibrant Modern

### Typography

**PRIMARY FONT:** Sora
- Weights: 400 (body), 600 (emphasis), 800 (headlines, hero)
- Usage: Headlines, hero text, section titles, buttons
- Letter-spacing: `-0.03em` at display sizes, `0` at body

**SECONDARY FONT:** Outfit
- Weights: 300 (light captions), 400 (body), 600 (emphasis)
- Usage: Body copy, navigation, form labels, product details
- Letter-spacing: `0.01em`

**DISPLAY FONT:** Anybody
- Weights: 400 (regular), 900 (black)
- Width: Variable -- use `font-stretch: 75%` for condensed display moments
- Usage: Large numbers, data callouts, accent display type
- Letter-spacing: `-0.05em` at condensed widths

### Type Scale

| Token | Size | Line Height | Font | Weight |
|-------|------|-------------|------|--------|
| display | 80px | 80px | Sora | 800 |
| h1 | 56px | 56px | Sora | 800 |
| h2 | 36px | 40px | Sora | 600 |
| h3 | 24px | 30px | Sora | 600 |
| body | 17px | 28px | Outfit | 400 |
| small | 14px | 22px | Outfit | 400 |
| label | 12px | 16px | Outfit | 600 |
| data | 96px | 96px | Anybody | 900 |

Note: display and h1 line-heights are TIGHT (1:1 ratio). Headings in this concept are punchy, stacked, compressed.

### Color Tokens

| Token | Hex | Usage |
|-------|-----|-------|
| `--bg-primary` | `#0C0A09` | Main background -- rich warm black |
| `--bg-secondary` | `#1C1917` | Section alternation, card interiors |
| `--fg-primary` | `#FAFAF9` | Primary text -- warm near-white |
| `--fg-secondary` | `#D6D3D1` | Secondary text |
| `--fg-muted` | `#78716C` | Muted text, metadata |
| `--accent-primary` | `#F97316` | Primary accent -- bold orange. CTAs, highlights |
| `--accent-secondary` | `#FB923C` | Secondary accent -- lighter orange for hovers |
| `--accent-hot` | `#EF4444` | Hot accent -- sale badges, urgent elements |
| `--accent-gold` | `#FBBF24` | Gold accent -- star ratings, premium labels |
| `--surface` | `#292524` | Cards, elevated surfaces |
| `--border` | `#44403C` | Borders, dividers |

### Spacing Scale (8pt grid)

`4, 8, 12, 16, 24, 32, 48, 64, 96, 128`

Spacing rules:
- Section padding: `64px` vertical on desktop, `48px` on mobile
- Between major elements: `32px`--`48px`
- Between related elements: `16px`--`24px`
- This concept is DENSER than Editorial. Tighter spacing = more energy.

### Border Radius

**Mixed -- intentional contrast.**
- Cards: `8px`
- Buttons: `999px` (full pill)
- Inputs: `8px`
- Images: `4px` (just barely softened)
- Badges/chips: `999px` (full pill)
- Modals: `16px`

### Shadow Language

**Colored shadows with ambient glow.**
- Card hover: `0 8px 32px rgba(249, 115, 22, 0.15)` (orange-tinted glow)
- Modal: `0 24px 48px rgba(0, 0, 0, 0.4)`
- Button hover: `0 4px 16px rgba(249, 115, 22, 0.3)` (orange underglow)
- No gray/neutral shadows. Every shadow carries brand color.

### Button System

**Primary:**
- Background: `var(--accent-primary)` (`#F97316`)
- Text: `#0C0A09` (black on orange)
- Font: Outfit 600, 15px, letter-spacing `0.02em`
- Padding: `16px 36px`
- Border: none
- Radius: `999px` (pill)
- Hover: background `var(--accent-secondary)`, `box-shadow: 0 4px 16px rgba(249, 115, 22, 0.3)`, scale `1.02`
- Transition: `250ms cubic-bezier(0.34, 1.56, 0.64, 1)` (slight bounce)

**Secondary:**
- Background: transparent
- Text: `var(--fg-primary)`
- Border: `2px solid var(--border)`
- Radius: `999px`
- Hover: border color `var(--accent-primary)`, text color `var(--accent-primary)`, `box-shadow: 0 0 0 1px var(--accent-primary)`

**Ghost:**
- No background, no border
- Text: `var(--accent-primary)`
- Hover: underline slides in from left (animated), text brightens to `var(--accent-secondary)`

### Motion Language

| Property | Duration | Easing | Usage |
|----------|----------|--------|-------|
| Default | 250ms | `cubic-bezier(0.34, 1.56, 0.64, 1)` | Micro-interactions (slight overshoot/bounce) |
| Entrance | 500ms | `cubic-bezier(0.22, 1, 0.36, 1)` | Fade-in, slide-up, stagger reveals |
| Hover | 200ms | `ease-out` | Color shifts, scale, shadow |
| Data counter | 1200ms | `cubic-bezier(0.16, 1, 0.3, 1)` | Number count-up animations |

Notes:
- Motion is FAST and energetic. Slight overshoot on interactions gives tactile feel.
- Hover states are aggressive: scale, color shift, AND shadow all at once.
- Numbers animate via count-up when scrolled into view (use Intersection Observer).
- Stagger delay: 60ms between elements (faster than Editorial -- more energy).

---

## Concept 03: Neighborhood Trusted

### Typography

**PRIMARY FONT:** Source Serif 4
- Weights: 300 (light display), 400 (body serif), 700 (bold headlines)
- Usage: Headlines, section titles, pull quotes, editorial moments
- Letter-spacing: `0` (default tracking -- natural, not forced)

**SECONDARY FONT:** Nunito Sans
- Weights: 400 (body), 600 (emphasis), 700 (bold)
- Usage: Body copy, navigation, form labels, product details, buttons
- Letter-spacing: `0.01em`

**DISPLAY FONT:** Lora
- Weights: 400 (regular), 400 Italic, 700 (bold)
- Usage: Pull quotes, testimonials, accent text, "since 1995" type moments
- The italic is the star -- use it for warmth

### Type Scale

| Token | Size | Line Height | Font | Weight |
|-------|------|-------------|------|--------|
| display | 64px | 72px | Source Serif 4 | 300 |
| h1 | 48px | 56px | Source Serif 4 | 400 |
| h2 | 36px | 44px | Source Serif 4 | 400 |
| h3 | 24px | 32px | Source Serif 4 | 700 |
| body | 18px | 30px | Nunito Sans | 400 |
| small | 14px | 22px | Nunito Sans | 400 |
| label | 13px | 18px | Nunito Sans | 600 |
| quote | 22px | 34px | Lora Italic | 400 |

Note: Body line-height is GENEROUS (30px on 18px = 1.67 ratio). This concept breathes. Comfortable reading pace.

### Color Tokens

| Token | Hex | Usage |
|-------|-----|-------|
| `--bg-primary` | `#FDF8F3` | Main background -- warm cream, like aged paper |
| `--bg-secondary` | `#F0E6D8` | Section alternation, warm sand |
| `--bg-accent` | `#FFF1E6` | Highlight sections, sale callouts -- peachy warmth |
| `--fg-primary` | `#2C1810` | Primary text -- deep warm brown, NOT black |
| `--fg-secondary` | `#5E4B3B` | Secondary text, descriptions |
| `--fg-muted` | `#9B8A7A` | Muted text, metadata, timestamps |
| `--accent-primary` | `#B85C38` | Primary accent -- terra cotta. Warm, earthy, inviting |
| `--accent-secondary` | `#D4763A` | Secondary accent -- lighter terra cotta for hovers |
| `--accent-green` | `#5B7C5A` | Trust signals, "in stock," confirmation states |
| `--surface` | `#FFFFFF` | Cards, modals |
| `--border` | `#E0D5C7` | Borders, dividers |
| `--border-warm` | `#D4C4B0` | Stronger borders, active states |

### Spacing Scale (8pt grid)

`4, 8, 16, 24, 32, 48, 64, 96, 128`

Spacing rules:
- Section padding: `80px` vertical on desktop, `56px` on mobile
- Between major elements: `48px`
- Between related elements: `24px`
- This concept is COMFORTABLE. Not as airy as Editorial, not as dense as Vibrant.

### Border Radius

**Soft and warm.** Max `12px`.
- Cards: `12px`
- Buttons: `8px`
- Inputs: `8px`
- Images: `8px`
- Badges/chips: `999px` (full pill for small elements)
- Modals: `16px`

### Shadow Language

**Warm, soft shadows.**
- Card rest: `0 2px 8px rgba(44, 24, 16, 0.06)` (barely-there warmth)
- Card hover: `0 8px 24px rgba(44, 24, 16, 0.1)` (soft lift)
- Modal: `0 16px 48px rgba(44, 24, 16, 0.15)`
- No colored shadows. No harsh edges. Everything is warm and diffused.

### Button System

**Primary:**
- Background: `var(--accent-primary)` (`#B85C38`)
- Text: `#FFFFFF`
- Font: Nunito Sans 700, 16px
- Padding: `14px 28px`
- Border: none
- Radius: `8px`
- Hover: background darkens to `#A04E2E`, shadow `0 4px 12px rgba(184, 92, 56, 0.25)`
- Transition: `350ms ease-in-out`

**Secondary:**
- Background: `var(--bg-primary)`
- Text: `var(--accent-primary)`
- Border: `1.5px solid var(--accent-primary)`
- Radius: `8px`
- Hover: background fills to `var(--accent-primary)`, text flips to white

**Ghost:**
- No background, no border
- Text: `var(--accent-primary)`
- Underline: none at rest
- Hover: underline appears (`1px solid`), slight color shift to `var(--accent-secondary)`

### Motion Language

| Property | Duration | Easing | Usage |
|----------|----------|--------|-------|
| Default | 350ms | `ease-in-out` | All standard transitions |
| Entrance | 500ms | `cubic-bezier(0.25, 0.46, 0.45, 0.94)` | Fade-in, slide-up |
| Hover | 250ms | `ease-in-out` | Background fills, shadow lifts |
| Pulse | 2000ms | `ease-in-out` | Chat button pulse, gentle attention |

Notes:
- Motion is GENTLE and predictable. No bounce, no overshoot. Ease-in-out everywhere.
- Entrance animations are subtle -- small `translateY(12px)` slides, gentle fades.
- No aggressive parallax or scroll-jacking. This concept respects the user's scroll.
- Stagger delay: 80ms between elements (moderate, comfortable rhythm).

---

## Global Rules (All Concepts)

### Image Treatment
- All hero images: `object-fit: cover`, minimum 50vh on desktop
- Product images: consistent aspect ratios within each concept
- No generic stock overlay gradients. If text needs contrast over an image, use a solid-color panel adjacent to the image, not a gradient over it.

### Responsive Breakpoints
- Mobile: 0--639px
- Tablet: 640px--1023px
- Desktop: 1024px+
- Max content width: `1200px` (Editorial), `1280px` (Vibrant), `1120px` (Neighborhood)

### Accessibility Minimums
- All color combinations must pass WCAG AA (4.5:1 for body text, 3:1 for large text)
- Focus states: visible outline using `var(--accent-primary)` per concept
- All interactive elements: minimum 44px touch target
- Reduced-motion: respect `prefers-reduced-motion: reduce` -- disable scroll animations, simplify hover states

### Typography Global
- Real typographic punctuation: curly quotes (" "), em dashes (--), apostrophes (')
- No straight typewriter quotes ever
- Body text minimum: 16px (we use 17--18px across all concepts)
- No orphans in headlines: use `text-wrap: balance` where supported
