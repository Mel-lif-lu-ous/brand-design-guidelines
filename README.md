# Quantum Partners — Design System

A design system for **Quantum Partners**, a professional services firm that helps organizations build with precision, long-view thinking, and strategic clarity. The brand sits at the intersection of technical rigor and human partnership — grounded in forest greens, anchored by Newsreader's editorial weight, and brought alive by a retro-futurist technical depth.

> **Positioning:**
> *"Where rigorous thinking meets long-term partnership."*
>
> We help organizations navigate complexity with clear-eyed strategy, precise execution, and the kind of sustained collaboration that compounds over time.

The visual system is composed, technical, and quiet — built on a bounded grid, a green-forward palette, and Newsreader's editorial confidence paired with Inter's functional clarity.

---

## Index

```
README.md                     ← you are here
SKILL.md                      ← Agent-Skills compatible entry point
colors_and_type.css           ← CSS variables + semantic type classes

assets/
  qp-logo.svg                 ← primary wordmark (add when available)

preview/                      ← Design System tab cards
  logo.html
  colors-primary.html         colors-surface.html
  colors-accent.html
  type-display.html           type-body.html
  type-scale.html
  spacing.html  radii.html  elevation.html
  buttons.html  cards.html  forms.html

ui_kits/
  website/                    ← public marketing website kit
```

---

## CONTENT FUNDAMENTALS

Quantum Partners copy is composed, precise, and authoritative without being cold. It reads like a senior partner in conversation — measured, confident, and oriented toward outcomes that compound.

### Voice

- **Precise but human.** Never "disrupt," "unlock," "supercharge," or "reimagine." Instead: *build with clarity*, *execute with rigor*, *sustain over time*.
- **Peer-to-peer.** The reader is a thoughtful executive, founder, or operator. Treat them as someone who already knows the problem space.
- **Long-view oriented.** The brand values patience, compounding results, and structural soundness over speed-for-its-own-sake.
- **Technical without jargon.** When the work is complex, name it directly. Never dress up vagueness in abstraction.

### Tone

- Composed. Direct. Quietly authoritative.
- No exclamation marks in body copy. No emoji. No urgency theater.
- Newsreader italic is the ONLY typographic flourish — used once, in the single most important phrase on a page.

### Grammar & casing

- **Sentence case** for all headings, buttons, nav items, and UI labels.
  - ✅ "Start a conversation" · ✅ "What we do" · ✅ "Case studies"
  - ❌ "Start A Conversation" · ❌ "START A CONVERSATION"
- **UPPERCASE + tracked letter-spacing (0.16em)** is reserved for eyebrow / micro-labels only: `01 · COLOR`, `PARTNERS`, `CAPABILITIES`.
- **Oxford commas** on.
- **Em-dashes (—): max one per page.** Use it in the single most important sentence. Replace all others with commas, colons, or parentheses.

### Pronouns

- **"You"** for the reader, **"we"** for Quantum Partners, **"your organization"** or **"your team"** when speaking about clients' internal context.
- Avoid third-person about the firm ("Quantum Partners delivers…") — it reads like a brochure.

### Examples

- Tagline: *"Where rigorous thinking meets long-term partnership."*
- Body: *"We help organizations navigate complexity with clear-eyed strategy, precise execution, and the kind of sustained collaboration that compounds over time."*
- Button: `Start a conversation`
- Micro-label: `01 · CAPABILITIES`
- Section header: `How we work`

---

## VISUAL FOUNDATIONS

### Palette

See `colors_and_type.css` for the full set. The mental model is three tiers:

1. **Foundation trio** — Ink `#171717`, White `#FFFFFF`, Mist `#F2F7F4`. These carry 80% of any layout.
2. **Green family** — Forest `#437652` is the primary accent and CTA color. Sage `#8DA696` supports. Teal `#418282` provides tertiary contrast. Forest Dark `#2E5238` is hover/press. Forest Light `#E8F0EB` is a tinted wash for subtle fills.
3. **Grey scale** — `#737373` (secondary text), `#A3B5A8` (muted/dividers), `#DCE5DF` (hairline).

The palette is cool-warm: forest green provides warmth and life; teal and grey maintain precision. Avoid saturated reds, blues, or purples. The greens are the only vivid family.

### Typography

- **Newsreader** for all display and major editorial headings (H1, H2). Weight 400 (regular). Italic is the sole typographic flourish.
- **Inter** for all functional text: H3–H5, body, UI copy, labels, buttons. Weights 400 / 500 / 600 / 700.
- No monospace typeface in the core stack. Use `ui-monospace` system fallback for code snippets only.
- **Display spec (from design source):** 48px / 52.8px line-height / -0.03em letter-spacing.
- **Body spec (from design source):** 13px / 21px line-height.
- Large oversized Newsreader letterforms ("Aa" at 200px+) work as decoration on type-specimen pages only.

### Backgrounds

- Default page = `#F2F7F4` (Mist). Default surface = `#FFFFFF`.
- Feature sections use a **solid `#437652` forest slab** with Mist-colored text on top.
- Dark/inverse sections use `#171717` Ink background.
- **No noise overlays, no gradient meshes, no repeating tile patterns.**

### The Gradient Border Shell

The signature elevation treatment. Wrap a surface in an outer shell with:
- `padding: 1–2px`
- `background: linear-gradient(135deg, rgba(67,118,82,0.30), rgba(141,166,150,0.15), rgba(65,130,130,0.20))`
- `border-radius` matching the inner card

The inner surface sits inside with its own radius, so the gradient shell reads as a hairline premium frame. Do not use a solid green border in its place — the shell is the technique.

### WebGL Accent

The brand carries a retro-futurist 3D WebGL accent: a perspective grid field (green lines on dark), animating with a slow breathing pulse. Pointer drift is allowed but subtle. Build with Three.js (`alpha: true`, `antialias: true`, DPR clamp to 2). Fallback is a static dark panel. This accent is used in feature-card wells and hero insets — never as full-page background.

**Stack:** Three.js — `PerspectiveCamera` (50deg FOV), grid line geometry with depth fade, `PointsMaterial`, ambient + key lighting, slow `sin(time)` breathing on Z position.

### Animation

- **Minimal and interface-led.** Never kinetic for its own sake.
- Default easing: `ease`. Durations: 140ms / 220ms / 400ms.
- Fades + small translate (4–8px). No scale-ups. No rotations.
- The WebGL breathing pulse is the only ambient motion allowed.

### Hover & press

- **Buttons:** hover darkens (Forest `#437652` → Forest Dark `#2E5238`). No scale change.
- **Cards:** hover lifts with `--shadow-lift` + `translateY(-2px)`.
- **Links:** hover underlines (1px, offset 3px). No color change.
- **Disabled:** `opacity: 0.5` + `cursor: not-allowed`.

### Borders

- Hairline `#DCE5DF` (1px) is the universal divider and card stroke.
- `#A3B5A8` is reserved for input borders at rest.
- No double borders.

### Shadows

Elevation is **surface-first** — surfaces elevate via the gradient shell, not stacked shadows. Two tokens: `--shadow-lift` (soft, 15px spread) and `--shadow-deep` (stronger, feature panels). `--shadow-xs` is for micro-lifts.

### Layout rules

- **Max container width: 1280px** with 8px-rhythm side padding (64px desktop, 24px mobile).
- **8px grid** throughout. Scale: 4 / 8 / 16 / 24 / 32 / 40 / 48 / 64 / 80 / 96 / 128.
- **Fixed top nav**, transparent over hero, solid Mist once scrolled.
- **Footer** is always Ink (`#171717`) with Mist text.

### Corner radii

- Cards: `12px` (default) / `16px` (feature / large).
- Inputs: `8px`.
- Buttons: `8px` (standard UI button); `999px` pill only for tags and status chips.
- Containers with editorial content: `16px`.
- The gradient border shell outer wrapper: `0px` (flush) or `16px` (when curved).

### Cards

- Default card: `#FFFFFF` background, `1px solid #DCE5DF` border, `12px` radius, no shadow at rest. On hover: `--shadow-lift`.
- Feature card: `#437652` (forest) background, Mist text, gradient border shell at rest, `16px` radius.
- Dark/inverse card: `#171717` background, `#F2F7F4` text.
- Never a colored left-border accent bar.

---

## ICONOGRAPHY

Use a clean, geometric line icon style — 1.5px stroke, rounded joins, no fills. Forest or Sage on light backgrounds; Mist on dark/forest backgrounds. Icon grid: 20×20px with 2px padding inset.

---

## DO'S AND DON'TS

### Do
- Use Forest `#437652` as the single CTA and primary accent.
- Keep spacing aligned to the 8px rhythm.
- Use the gradient border shell consistently for elevated surfaces.
- Use Newsreader italic once, for the most important editorial phrase.

### Don't
- Don't introduce colors outside the defined palette.
- Don't use the WebGL grid as a full-page wallpaper — it's an accent, not a background.
- Don't mix shadow recipes. The lift and deep tokens are the only options.
- Don't use pill (999px) for action buttons — that shape is reserved for tags and chips.
- Don't add a second em-dash to any page. One per page, maximum.
