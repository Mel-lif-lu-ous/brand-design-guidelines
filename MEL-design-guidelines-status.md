# MEL-design-guidelines-status.md — Mel·lif·lu·ous
# mel-lif-lu-ous.com
# Last updated: August 16, 2026

Living tracker for the design system: tokens, sync status, and open design tasks. The brand
definition lives in `colors_and_type.css` in this folder, mirrored byte-identically into the
theme and rendered live at `/design-guidelines/`.

---

## Source of Truth

**`colors_and_type.css` in this folder is authoritative.** Every value the brand uses is
defined here, and the live `/design-guidelines/` page renders from it at request time, so the
page cannot state a colour the file does not have.

⚠️ **`MEL-design-guidelines.html` was deleted August 16, 2026.** It was a 535-line standalone
copy of the guidelines, and a second description of the brand is a second thing to keep in
step. The live page replaces it and cannot drift, because it reads the tokens rather than
restating them. Recoverable from git history if a section of its copy is ever wanted back.

⚠️ **`Mel-external-skills/` was deleted the same day**, 39 third-party reference documents on
animation libraries, aesthetic demos and UX heuristics. Reference material, never authoritative,
and LKI's equivalent folder went at the same time. Also in git history.

## Tokens

Prefix is `--qp-` and stays that way. Never hardcode a colour or font value.

### Colour

| Role | Token | Value |
|---|---|---|
| Canvas | `--qp-canvas` | `#f5f5f5` |
| Canvas soft | `--qp-canvas-soft` | `#fafafa` |
| Surface card | `--qp-surface-card` | `#ffffff` |
| Surface strong | `--qp-surface-strong` | `#f0efed` |
| Surface dark | `--qp-surface-dark` | `#0c0a09` |
| Ink | `--qp-ink` | `#313131` |
| Body | `--qp-body` | `#4e4e4e` |
| Muted | `--qp-muted` | `#777169` |
| Muted soft | `--qp-muted-soft` | `#a8a29e` |
| Hairline | `--qp-hairline` | `#e7e5e4` |
| Hairline strong | `--qp-hairline-strong` | `#d6d3d1` |
| Brand forest | `--qp-brand` | `#4d7a5c` |
| Brand light | `--qp-brand-light` | `#89a998` |
| Brand dark | `--qp-brand-dark` | `#3a6148` |
| Success | `--qp-success` | `#16a34a` |
| Error | `--qp-error` | `#dc2626` |

### Typography

- **Newsreader** for display and editorial headings: 400 regular, 300 italic
- **Inter** for UI, body, labels, metadata: 300 / 400 / 500 / 600 / 700
- The 300-italic accent is **forest only, one per page**

Scale: Display 56/61.6 (-0.03em) · H1 40/48 · H2 32/40 · H3 24/32 (Inter 600) ·
Lead 24/36 · Body 16/26 · Small 12/18 · Micro caps 11/16 (0.10em, upper)

### Components and motion

- Button radii **8px**. Pill radii reserved for tags and chips, never buttons
- Hairline borders by default. Shadow and gradient shell only for interactive or
  high-emphasis surfaces
- Motion: easing `ease` (`--ease-std`), durations 140 / 220 / 400ms (`--dur-fast` /
  `--dur-std` / `--dur-slow`), fades plus 4 to 12px translate. No scale above 1.02, no
  rotation, no shimmer loaders

⚠️ **Mel's easing is `ease`, not LKI's `cubic-bezier(0.32, 0.72, 0.24, 1)`.** The notes that
carried LKI's value went with `Mel-external-skills/` on August 16, 2026, so the contradiction is
gone. `colors_and_type.css` is the only place easing is defined now.

### Photography and icons

- **Photography:** documentary style, natural light, real locations, minimal processing. No
  staged stock
- **Icons:** Phosphor light weight only. 1.5px stroke, rounded joins, no fill, 20x20 grid
  with 2px inset

---

## Sync Status

| Copy | Location | State |
|---|---|---|
| Canonical | `colors_and_type.css` (this folder) | Source of truth for tokens |
| Theme copy | `../Website/mel-theme/colors_and_type.css` | Byte-identical, verified via `md5` |

**Rule, settled August 7, 2026:** the theme carries a **byte-identical copy**, enqueued
before `mel.css`. Tokens are not flattened into the main stylesheet.

Why: WordPress cannot read a stylesheet from outside the theme folder, so a copy is
unavoidable. Keeping the filename and contents identical makes syncing a file copy rather
than a hand-merge, so "is it in sync?" is answerable with `diff` and fixable with `cp`.
Flattening the tokens is how KSA's deployed copy drifted.

**Never hand-edit the theme's copy.** Edit this folder's file, re-copy, verify with `diff`.
The check is step 2 of the deploy checklist in `../Website/MEL-website-status.md`.

This deliberately differs from `lki-child`, which keeps tokens inline in `lki.css`. LKI's
cleanup is on Lara's own schedule; the two themes will differ in the interim.

---

## Guidelines Page State

**There are now two, and the live one is authoritative for what the site does.**

**One page now, on the site.** `page-design-guidelines.php`, Page ID 15510, added August 16,
2026. Sections follow the shared order in `../../WORKSPACE-design-guidelines-playbook.md`:
Logo · Photography · Icons · Colour · Type · Layout · Buttons. A searchable icon library sits
alongside it at `/icon-library/`, Page ID 15511, 1,512 Phosphor Light icons.

The live page **cannot state a colour the stylesheet does not have**: swatches fill from
`var(--token)`, the hex beside each is parsed out of `colors_and_type.css` by `mel_tokens()` at
render time, and contrast is computed in the browser from the rendered colour. The static HTML
has no such guarantee, so where the two disagree, the live page is right about the site and the
HTML is right about the intent.

### Four decisions the page is waiting on

Each renders as a "Decision needed" block on the page rather than being hidden. Deleting the
block is how the section gets finished.

1. **Logo.** No vector exists, so there is nothing to offer as a download. Either the wordmark
   is the identity and this section documents the face, weight and tracking, or a mark gets
   commissioned and an `assets-logo/` folder appears. Lead: `Content Docs/Projects/Wildroot &
   Amber/Logo/Logo Mellifluous.psd`
2. **Icons.** Phosphor Light is chosen and nothing ships it, so there is no honest sample.
   Sourcing is one shallow clone, command is on the page. Second question: animated set for
   section moments the way LKI has, or static-only, which suits the restraint here
3. **Two type scales.** The named scale sits alongside a parallel `--type-ui-*` ladder of
   thirteen steps, 9px to 82px, some of it genuinely in use. A system with two scales has no
   scale. Fold it in, or keep it as an explicitly separate interface ladder with a stated reason
4. **Thirteen radius steps.** `none, 2xs, xs, s, sm, m, md, card, lg, feature, shell, xl, pill,
   circle`, with 3, 6, 10, 20 and 22px sitting close enough to their neighbours that swapping one
   changes nothing visible. Seven are shown on the page because those do real work

### Fixed while building

- ⚠️ **The page printed dark-mode hexes on its first render.** `colors_and_type.css` ends with a
  `body.dark` block redefining six tokens, and the parser scanned the whole file and kept the
  last match, so Canvas painted `#F5F5F5` and printed `#0F0E0E`. Five of twenty-one tokens were
  wrong. `mel_tokens()` is now scoped to the `:root` block. **Caught only because the
  browser-measured contrast disagreed with the printed hex** — the argument for computing rather
  than storing that number
- ⚠️ **`--qp-muted-soft` is not a text colour.** Measured 2.52:1 against Canvas, which misses the
  3:1 large-text floor as well as AA. This file previously listed it under Colour without
  qualification. It is a divider and placeholder colour
- ✅ **Hero scrim tokenised.** `.hero__scrim` carried a literal `rgba(49,49,49,…)` triple; it now
  reads `--scrim-hero-strong/-mid/-soft`. Values unchanged, so nothing shifted
- ✅ **`.hero--page` and `.hero__bg--photo` added**, named to match `lki-child` so the two themes
  stay one system. Interior heroes are ready for a photograph: set `$mel_hero_slug` and nothing
  else changes. The dark slab is the design, not a fallback

### Still hardcoded in mel.css, noted not fixed

Three literal colours remain, all outside the hero: the drawer link border and hover tint
(`rgba(49,49,49,.05)` / `.04`) and the blog-card overlay gradient. Same class of problem LKI
cleared on August 16; worth the same sweep here, but each is a small visual decision rather than
a mechanical swap.

---

## Open Tasks

- [ ] ⚠️ **Mel still has no favicon set.** The old standalone HTML pulled one from LKI's
      `global-assets` repo, wrong brand, and that file is now deleted. The site itself needs a
      real one: see the Favicon section of the workspace playbook for the procedure
- [x] 🤖 **`--sz-principle-min` removed (August 8, 2026).** `.shadow-card` now points at the
      existing `--sz-card-min` (180px, was 200px), shared with `.card`. The orphaned token
      is gone from `colors_and_type.css` in both this folder and the theme copy, plus the
      live server copy. Verified byte-identical across all three (md5 `2dbd9e9f...`)
- [ ] ⚠️ **`@import` for Google Fonts** at the top of `colors_and_type.css` blocks rendering.
      Fonts should be enqueued in the head instead. Fixing it breaks byte-identical parity with
      the theme copy, so it needs a deliberate decision. **Still open.**
- [ ] **Logo is type for now** (decided August 7, 2026). The nav wordmark is live text in
      Newsreader using the `.nav__logo-text` pattern from `lki.css`. No vector exists, and
      this is the right answer for a typographic name regardless. Replaceable later without
      touching layout. The lead for a real mark is
      `../Content Docs/Projects/Wildroot & Amber/Logo/Logo Mellifluous.psd`. Note the `.ai`
      files elsewhere in that folder are laser-cut layouts for the installation, not logos
- [x] ✅ **Empty folders removed.**
- [ ] 👤 **Repo visibility.** `brand-design-guidelines` is Public; the workspace rule says
      Design Guidelines should be Private
- [x] ✅ **Resolved.** That reorg was committed some time before August 16, 2026; this entry was
      stale. The tree is clean apart from current work.
