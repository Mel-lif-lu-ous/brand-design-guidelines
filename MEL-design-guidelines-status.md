# MEL-design-guidelines-status.md — Mel·lif·lu·ous
# mel-lif-lu-ous.com
# Last updated: August 8, 2026

Living tracker for the design system: tokens, sync status, and open design tasks. The brand
definition itself lives in `MEL-design-guidelines.html`, with tokens mirrored into
`colors_and_type.css`.

---

## Source of Truth

**`MEL-design-guidelines.html` is authoritative.** If `colors_and_type.css`, the theme, or
any other implementation conflicts with it, align to the HTML.

Renamed from `index.html` on August 7, 2026 via `git mv`, so history is preserved. The
rename follows the workspace naming rule and matches LKI's `LKI-design-guidelines.html`.

⚠️ **The old `README.md` and `SKILL.md` are archived.** Both were moved into
`_Archives (DO NOT READ)` during the August 7, 2026 reorg. They carried the "index.html is
the source of truth" enforcement rules, which have been moved into
`../MEL-folder-structure-and-rules.md` → Brand Rules. Do not restore them; the root rules
file owns those rules now.

`SKILL.md` was a Claude Code project skill (`mel-design-guidelines`). It is no longer
loadable. If a skill is wanted again, recreate it pointing at the new filename.

---

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

⚠️ **Mel's easing is `ease`, not LKI's `cubic-bezier(0.32, 0.72, 0.24, 1)`.** The
`Mel-external-skills/animation-skills/adaptation-notes.md` file documents LKI's easing,
because it was copied over from LKI's workspace. Those notes are reference only;
`colors_and_type.css` wins. Worth correcting in that file, or at least reading it with this
in mind.

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

`MEL-design-guidelines.html`, 535 lines, single file, light/dark toggle.

Sections: Mood Board · Icons · Typography · Type Scale · Color · Shadow · Spacing · Radius ·
Elevation · Buttons · Cards · Badges · Forms

**Changes made August 7, 2026:**
- Removed the Principles / Philosophy section (four numbered cards) and its nine orphaned
  CSS rules
- Stripped the numeric prefixes from all 13 section eyebrows. Numbering had gaps at 07 and
  13 and added nothing

---

## External Skills

`Mel-external-skills/` holds 40 third-party reference documents pulled August 5, 2026:

- **`animation-skills/`** — 24 library guides (GSAP, Three.js, Framer Motion, Rive, Lottie,
  Spline, Blender, and others)
- **`aesthetic-demos/`** — 11 self-contained HTML demos, each committing to one aesthetic
- **`ui-ux-pro-max/`** — UX guidelines and UI reasoning rules

**These are reference, never authoritative.** Each folder's own `adaptation-notes.md` is
explicit that none of the 11 aesthetics is the brand and none should be adopted wholesale.
Colour and typography always come from this folder's tokens, never from a skill, including
the "Color Mood" and "Typography Mood" descriptors inside `reasoning-rules.md`.

Library defaults matter here: many GSAP and Anime.js examples lean on bounce, elastic or
spring easings, larger scale transforms, and rotation. Treat those example values as things
to override, not copy. The library is just the mechanism; the motion language stays Mel's.

`swiss-minimalism.html` is the closest structural cousin to Mel's restraint. Useful for
studying how far grid and whitespace can be pushed, not for borrowing its palette or type.

---

## Open Tasks

- [ ] ⚠️ **Favicon points at LKI's GitHub.** `MEL-design-guidelines.html` loads its favicon
      from `raw.githubusercontent.com/Lara-Kroeker-Interactive/global-assets`. Wrong brand.
      Needs a Mel favicon set
- [x] 🤖 **`--sz-principle-min` removed (August 8, 2026).** `.shadow-card` now points at the
      existing `--sz-card-min` (180px, was 200px), shared with `.card`. The orphaned token
      is gone from `colors_and_type.css` in both this folder and the theme copy, plus the
      live server copy. Verified byte-identical across all three (md5 `2dbd9e9f...`)
- [ ] ⚠️ **`@import` for Google Fonts** at the top of `colors_and_type.css` blocks
      rendering. Fonts should be enqueued in the head instead. Fixing it breaks
      byte-identical parity with the theme copy, so it needs a deliberate decision
- [ ] **Logo is type for now** (decided August 7, 2026). The nav wordmark is live text in
      Newsreader using the `.nav__logo-text` pattern from `lki.css`. No vector exists, and
      this is the right answer for a typographic name regardless. Replaceable later without
      touching layout. The lead for a real mark is
      `../Content Docs/Projects/Wildroot & Amber/Logo/Logo Mellifluous.psd`. Note the `.ai`
      files elsewhere in that folder are laser-cut layouts for the installation, not logos
- [ ] **Empty folders:** `ui_kits/website/` and `uploads/` hold only `.gitkeep`. Populate or
      remove
- [ ] 👤 **Repo visibility.** `brand-design-guidelines` is Public; the workspace rule says
      Design Guidelines should be Private
- [ ] **Uncommitted work in this repo.** The `git mv` is staged but not committed, and the
      working tree carries a large batch of pre-existing deletions from the reorg (the
      `preview/` folder, `README.md`, `SKILL.md`, `assets/`). Needs one deliberate commit
