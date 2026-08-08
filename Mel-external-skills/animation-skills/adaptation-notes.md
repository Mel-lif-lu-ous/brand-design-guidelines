---
title: Animation Design Skills — Adaptation Notes
---

# Source

Pulled from: [freshtechbro/claudedesignskills on GitHub](https://github.com/freshtechbro/claudedesignskills)

Date pulled: 2026-08-05

# What was pulled

Only the `SKILL.md` instructional content for each of the 22 animation-related skills, fetched directly from the repo's raw GitHub content (`.claude/skills/<skill-name>/SKILL.md`). Slash commands, agent definitions, helper scripts, and asset/template files were intentionally excluded — those are Claude-Code-specific tooling (meant to be invoked as a Claude Code skill) and aren't usable or needed as plain reference material outside Claude Code. What's kept here is the descriptive/instructional documentation: concepts, code patterns, API usage notes, and best practices for each library.

All 22 skills were accessible with no rate-limit or access issues. Every file below has real, complete content.

# Files pulled (22 of 22)

| File | Source skill | Library |
|---|---|---|
| `threejs.md` | threejs-webgl | Three.js |
| `gsap.md` | gsap-scrolltrigger | GSAP + ScrollTrigger |
| `react-three-fiber.md` | react-three-fiber | React Three Fiber |
| `framer-motion.md` | motion-framer | Framer Motion |
| `babylonjs.md` | babylonjs-engine | Babylon.js |
| `a-frame.md` | aframe-webxr | A-Frame / WebXR |
| `vanta.md` | lightweight-3d-effects | Vanta |
| `playcanvas.md` | playcanvas-engine | PlayCanvas |
| `pixijs.md` | pixijs-2d | PixiJS |
| `locomotive-scroll.md` | locomotive-scroll | Locomotive Scroll |
| `barba-js.md` | barba-js | Barba.js |
| `react-spring.md` | react-spring-physics | React Spring |
| `magic-ui.md` | animated-component-libraries | Magic UI (and related component libraries) |
| `aos.md` | scroll-reveal-libraries | AOS (Animate On Scroll) |
| `anime-js.md` | animejs | Anime.js |
| `lottie.md` | lottie-animations | Lottie |
| `blender.md` | blender-web-pipeline | Blender (web pipeline) |
| `spline.md` | spline-interactive | Spline |
| `rive.md` | rive-interactive | Rive |
| `substance-3d.md` | substance-3d-texturing | Substance 3D texturing |
| `web3d-integration.md` | web3d-integration-patterns | Web3D integration patterns (meta-skill) |
| `modern-web-design.md` | modern-web-design | Modern web design (meta-skill) |

Nothing was skipped or inaccessible. Note: the repo's own README groups "Magic UI" and "AOS" under broader skill names (`animated-component-libraries` covers component libraries generally, `scroll-reveal-libraries` covers AOS specifically) — the file names above map to the library, not necessarily a 1:1 skill-name match.

# Most directly usable for LKI's stack (plain PHP + vanilla JS, no framework)

Per the task priority, these are the ones to reach for first since LKI's site has no React/build step:

- `gsap.md` (GSAP + ScrollTrigger) — the most robust option for scroll-driven and timeline animation on a vanilla site.
- `locomotive-scroll.md` — smooth-scroll/parallax library, framework-agnostic.
- `aos.md` — simplest option, pure attribute-driven scroll reveals, zero JS authoring needed.
- `anime-js.md` — lightweight vanilla JS animation engine, good for one-off DOM/SVG animations.
- `lottie.md` — After Effects export playback via lottie-web, framework-agnostic.

`react-three-fiber.md` and `react-spring.md` are React-specific and won't apply directly to the PHP site — kept as reference only in case a future project uses React, but not a priority for the current build.

# IMPORTANT — reconcile with LKI's own motion rules

Every one of these library skills documents that library's own defaults and idioms, which will often diverge from LKI's documented motion standards (in Design Guidelines). Regardless of what a given library's SKILL.md recommends by default (many GSAP/Anime.js/React Spring examples lean on bounce, elastic, or spring easings, larger scale transforms, or rotation for flair), any animation actually implemented on an LKI site must still follow:

- **Easing:** `cubic-bezier(0.32, 0.72, 0.24, 1)` — calm and confident, never bouncy or springy. Do not use a library's "elastic," "bounce," or "spring" easing presets as-is.
- **Durations:** the 140ms / 220ms / 400ms scale — not whatever duration a library's example code defaults to.
- **Transforms:** fades plus small translate (4–12px) only. No scale-ups above 1.02. No rotations.
- **No shimmer loaders.**

When adapting a code pattern from any of these files, treat the library's own example values (easing curves, durations, scale/rotation amounts) as things to override, not copy. The library choice is just the mechanism — the motion language stays LKI's.
