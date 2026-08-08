# Adaptation Notes

**Source repo:** UI/UX Pro Max skill, https://github.com/nextlevelbuilder/ui-ux-pro-max-skill
**Date pulled:** 2026-08-05

Only two files were extracted from this repo: `ux-guidelines.md` (from `.claude/skills/ui-ux-pro-max/data/ux-guidelines.csv`) and `reasoning-rules.md` (from `.claude/skills/ui-ux-pro-max/data/ui-reasoning.csv`).

**Explicitly excluded, on purpose:** the skill's 84 UI styles, 192 color palettes, 74 font pairings, and its CLI/Python search-engine tooling (`scripts/search.py`, `scripts/design_system.py`, `scripts/core.py`, the `cli/` installer). None of that was pulled in, so it cannot compete with or drift against LKI's own fixed brand system.

**Reminder:** color and typography for LKI always come from `Design Guidelines/colors_and_type.css` — never from this skill, including the "Color Mood" / "Typography Mood" descriptors that appear inside `reasoning-rules.md`.
