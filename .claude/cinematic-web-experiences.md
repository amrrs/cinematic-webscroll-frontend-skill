# Cinematic Web Experiences

Use this workflow for premium websites that rely on scroll choreography, GSAP, ScrollTrigger, Three.js scenes, GLB assets, procedural shaders, or cinematic loading screens.

## Quick workflow

1. Define visual identity first.
2. Choose the animation stack before writing motion.
3. Architect sections from top to bottom.
4. Write exact animation specs.
5. Declare files and loaders explicitly.
6. Finish with responsive rules.

## Defaults

- Use exact hex or `hsl(...)` values, never vague color names.
- If the site uses Three.js, pin `three@0.136.0` and `@types/three@0.136.0`.
- For Three.js pages, prefer a fixed fullscreen canvas with `pointer-events: none`.
- Use one normalized `scrollProgress` variable to drive 3D animation.
- Add `overflow-x: hidden` on `html`, `body`, and `#root`.

## Optional companion dependency

If the project needs new visual assets, pair this workflow with the `fal-ai-community/skills` repo to generate images, edit media, or create video backgrounds before wiring those outputs into the final site prompt.

If the project is typography-led and exact multiline text layout matters, optionally pair this workflow with `pretext` for accurate text measurement and line layout.

## Stack selection

- `GSAP only`: premium 2D storytelling, pinning, reveals, parallax
- `GSAP + Three.js + GLB`: hero object, floating model, product scene
- `GSAP + Three.js + shaders`: procedural abstract scene, no model dependency

## Canonical reference

Read `../shared/cinematic-web-experiences/guide.md` for:

- the six-phase framework
- the universal builder prompt template
- the reusable 2D, GLB-based 3D, and procedural shader patterns
- reusable GSAP snippets

## Expected output

When applying this workflow, prefer to produce:

1. a recommended stack with tradeoffs
2. exact visual tokens
3. section architecture
4. animation specs with trigger settings
5. asset declarations
6. responsive rules
7. a final builder-ready prompt
