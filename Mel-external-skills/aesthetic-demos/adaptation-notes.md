# Adaptation Notes — Frontend Design Pro Demo (Reference Material)

**Source repo:** [claudekit/frontend-design-pro-demo](https://github.com/claudekit/frontend-design-pro-demo)
**Date pulled:** August 5, 2026
**Files pulled from:** `demos-v02/` (index.html, the 11 aesthetic HTML files, and the master-prompt
callouts inside them) and `skills/frontend-design-pro/SKILL.md` (keyword/palette/signature-effect table)

## What this is

This folder contains 11 self-contained HTML/CSS demo files, each committing fully to one distinct
visual aesthetic (Minimalism & Swiss Style, Neumorphism, Glassmorphism, Brutalism, Claymorphism,
Aurora/Mesh Gradient, Retro-Futurism/Cyberpunk, 3D Hyperrealism, Vibrant Block/Maximalist, Dark OLED
Luxury, Organic/Biomorphic) plus `master-prompts.md`, which lists the key characteristics and
signature techniques for each one.

## What this is NOT

**None of these 11 aesthetics is LKI's actual brand, and none of them should be adopted wholesale.**
LKI's real visual identity is documented in `Design Guidelines/colors_and_type.css` and
`Design Guidelines/LKI-design-guidelines.html` — a warm-cool palette, Inter + Instrument Serif
typography, and a restraint-oriented editorial sensibility. That is the brand. This folder is
reference material sitting alongside it, not a menu to pick a look from.

## Why it's here

Two specific uses, both indirect:

1. **Studying commitment as a discipline.** Each of these 11 demos picks one point of view and
   pushes it all the way through — typography, color, motion, structure — instead of defaulting to
   something generic or splitting the difference between three ideas. That is a useful thing to look
   at closely even when the aesthetic itself is wrong for LKI, because the failure mode LKI wants to
   avoid isn't "wrong style," it's "no committed style."

2. **Shared vocabulary for borrowing a single technique.** Having these named and coded means a
   request like "use the shadow-depth technique from the neumorphism demo for this one card" is
   possible without pulling in the rest of that aesthetic — a way to reference a specific move
   (a shadow treatment, a hover behavior, a grid idea) by name without going fully neumorphic,
   fully brutalist, etc.

## The one exception worth flagging

**Minimalism & Swiss Style** (`swiss-minimalism.html`) is the closest structural cousin to LKI's own
restraint-oriented taste — grid discipline, generous whitespace, typography-first hierarchy. Even so,
it is here for reference and discipline (studying how far a grid-and-whitespace system can be pushed),
not for copying. Its specific color/type choices (monochrome + single accent, grotesque sans) are not
LKI's palette or typefaces and shouldn't be pulled in directly.

## Verification

All 11 HTML files were downloaded from `raw.githubusercontent.com` and their byte sizes were checked
against the GitHub API's reported file sizes for `demos-v02/` — all matched exactly, confirming
complete, unmodified downloads. Files are saved as-is (no trimming or editing), per the source
repo's intent that they be self-contained visual references.
