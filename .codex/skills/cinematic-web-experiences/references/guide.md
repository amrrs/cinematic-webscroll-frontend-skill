# Codex Reference

This is the Codex-local companion to the shared guide at `../../../shared/cinematic-web-experiences/guide.md`.

## Stack selection

- `GSAP only`: best for reveal-heavy and typography-first sites
- `GSAP + Three.js + GLB`: best when a product or sculpture model is central
- `GSAP + Three.js + shaders`: best for abstract procedural worlds with no model files

If the site uses Three.js, include:

```text
Install three@0.136.0, @types/three@0.136.0
```

Prefer Lenis in the same stack when the experience leans on continuous 3D motion.

## Six-phase workflow

1. `Visual identity`
   - background, card, primary, accent, foreground, muted, fonts, weights
2. `Animation stack`
   - decide 2D, GLB-based 3D, or procedural 3D
3. `Section architecture`
   - loading screen, fixed navbar, hero, content sections, outro
4. `Precise animation specs`
   - transforms, start/end, scrub, stagger, mouse tracking, keyframes
5. `Files and assets`
   - asset paths, loaders, procedural texture generation
6. `Responsive behavior`
   - `clamp()`, mobile nav, collapsed layout, camera distance, overflow lock

## Durable patterns

- For 3D, use a fixed fullscreen canvas with `pointer-events: none`.
- Drive all 3D motion from one normalized `scrollProgress` variable.
- Give each section its own `ScrollTrigger` ownership.
- Keep dark themes disciplined: one strong accent, not several competing neon colors.

## Build references

- pure GSAP scroll identity
- GLB model with scroll-reactive Three.js motion
- procedural `ShaderMaterial` scene with code-generated textures

## Response shape

When using this skill, try to produce:

1. a stack recommendation with tradeoffs
2. exact visual tokens
3. section architecture
4. animation specs with trigger syntax
5. asset declarations
6. responsive rules
7. a final builder-ready prompt
