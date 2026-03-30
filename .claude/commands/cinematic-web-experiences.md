description: Generate or refine a prompt for a cinematic GSAP/Three.js website
argument-hint: [site concept or brand brief]

Read `../cinematic-web-experiences.md` and `../../shared/cinematic-web-experiences/guide.md` first.

Then help the user by:

1. choosing the right stack: `GSAP only`, `GSAP + Three.js + GLB`, or `GSAP + Three.js + shaders`
2. defining exact visual tokens
3. outlining the site sections in scroll order
4. writing exact animation specs with triggers, scrub values, and transforms
5. declaring all files, asset paths, loaders, or procedural generation rules
6. adding a responsive block with `clamp()` typography and overflow protection
7. producing a final builder-ready prompt

Use exact values, not aesthetic adjectives by themselves. If Three.js is involved, pin `three@0.136.0` and `@types/three@0.136.0`.
