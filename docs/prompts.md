# Prompting and Examples

## Prompting guidelines

The skill works best when the prompt is concrete and ordered. A good request usually includes:

1. `Brand or concept`
   - what the site is for
   - who it is for
   - the tone or mood
2. `Visual identity`
   - exact background, primary, accent, card, and text values
   - preferred typefaces and weights
3. `Animation stack`
   - `GSAP only`
   - `GSAP + Three.js + GLB`
   - `GSAP + Three.js + procedural shaders`
4. `Section architecture`
   - hero
   - content sections
   - outro/footer
   - optional loading screen
5. `Motion instructions`
   - exact transforms
   - exact `start`, `end`, `scrub`, and pinning behavior
6. `Asset plan`
   - existing file paths, or a request to generate assets first with `fal`
7. `Responsive rules`
   - `clamp()` typography
   - mobile nav behavior
   - camera adjustments
   - `overflow-x: hidden`

## Prompting rules of thumb

- Use exact hex or `hsl(...)` values instead of vague color names.
- Ask for one clear aesthetic direction instead of mixing many competing moods.
- Tell the model whether the page should be image-led, 3D-led, or typography-led.
- If assets do not exist yet, generate them first, then reference them by explicit path.
- If the design depends on exact multiline text lockups, call out `pretext` as an optional text-measurement helper.
- Treat each section as its own animation stage with clear ownership.
- End with a dedicated responsive block.

## Example prompt shape

```text
Use cinematic-web-experiences to create a premium single-page site for a luxury architectural fencing brand.

Visual direction:
- Background: #050505
- Card: #15120f
- Primary: hsl(28 42% 58%)
- Accent: hsl(46 78% 70%)
- Fonts: Syne 700/800 + Inter 300/400/500

Stack:
- GSAP + Three.js
- fixed fullscreen canvas
- looping background video

Sections:
- pinned hero
- three feature sections
- editorial outro with CTA

Animations:
- hero pins and scales down on scroll
- content cards reveal from x offsets with scrub
- 3D atmosphere reacts to a shared scrollProgress value

Assets:
- use existing images from /assets
- if needed, generate one additional bronze texture and one background loop first
- use pretext if headline wrapping and balanced multiline layout need to be deterministic

Responsive:
- clamp() typography
- stacked mobile layout
- overflow-x hidden on html, body, #root
```

## Example prompts by goal

Use these as copy-paste starters when you want to design something specific with the skills in this repo.

`Brand-first cinematic landing page`

```text
Use cinematic-web-experiences to design a premium landing page for a contemporary furniture studio called Obsidian Form.

Visual direction:
- Background: #060606
- Surface: #141414
- Primary: hsl(22 20% 72%)
- Accent: hsl(48 92% 70%)
- Foreground: #f5f1eb
- Fonts: Syne 700/800 + Inter 300/400/500

Stack:
- GSAP + ScrollTrigger
- fixed fullscreen background layer
- no 3D model unless clearly justified

Sections:
- loading screen
- pinned hero
- three collection sections
- editorial outro with CTA

Motion:
- hero pins for 180vh and scales from 1 to 0.82
- section cards reveal from alternating x offsets with scrub
- ambient background elements drift slowly with mouse tracking

Responsive:
- clamp() typography
- stacked mobile layout below 900px
- overflow-x hidden on html, body, #root
```

`Generate assets with fal, then integrate them`

```text
First use fal-ai-community/skills to generate these assets for a luxury travel brand called Serein Isles:
- one hero image with limestone architecture at dusk
- one looping ocean-haze background video
- two supporting material/detail images

Save the outputs into /assets.

Then use cinematic-web-experiences to build a premium single-page website that integrates those exact asset paths.

Requirements:
- GSAP + Three.js with a fixed fullscreen canvas
- soft parallax over the generated hero image
- background video behind the WebGL atmosphere
- explicit section architecture and exact ScrollTrigger settings
- responsive rules for mobile camera distance and stacked layout
```

`Typography-led experience with pretext`

```text
Use cinematic-web-experiences and pretext to design a typography-led microsite for a fashion imprint called Afterlight Bureau.

Goal:
- the site should feel editorial, restrained, and text-driven
- multiline headings must stay visually balanced across breakpoints
- one section should include an interactive text composition with draggable objects

Stack:
- GSAP + ScrollTrigger
- pretext for measured multiline headlines, balanced pull quotes, and interactive text layout
- minimal Three.js only if it improves the atmosphere without distracting from the typography

Output:
- exact section plan
- exact animation specs
- where pretext should be used and why
- responsive rules for deterministic text lockups on tablet and mobile
```

`Full-stack cinematic concept`

```text
Use cinematic-web-experiences to create a builder-ready prompt for a luxury skincare brand called Vanta Veil.

Visual identity:
- Background: #040404
- Card: #12100f
- Primary: hsl(18 32% 60%)
- Accent: hsl(160 58% 68%)
- Foreground: #f4efe8
- Fonts: Syne 700 + Inter 300/400/500

Stack:
- GSAP + Three.js + procedural shader atmosphere
- optional fal-generated texture and background loop
- pretext for the hero lockup and one balanced editorial callout

Sections:
- cinematic loading screen
- pinned 100vh hero
- ingredient story section
- product ritual section
- testimonial/editorial quote section
- final CTA

Animations:
- exact hero pinning, start/end, scrub, scale, and y transforms
- shader scene reacts to shared scrollProgress
- cards reveal with staggered viewport-entry motion
- mouse-tracked accent elements in the hero

Responsive:
- clamp() typography
- mobile nav overlay
- simplified shader intensity on small screens
- camera.position.z adjustment for mobile
```

## Best practices

- If Three.js is used, pin `three@0.136.0` and `@types/three@0.136.0`.
- For 3D scenes, prefer a fixed fullscreen canvas with `pointer-events: none`.
- Keep prompts exact: colors, transforms, trigger points, asset paths, and responsive rules should all be explicit.
- Treat each section as its own animation stage with its own trigger ownership.
- Default to one strong accent color on a restrained background unless the project clearly needs a different palette.

## Short example requests

```text
Use cinematic-web-experiences to build a prompt for a premium one-page studio website with GSAP reveals and a pinned hero.
```

```text
Use cinematic-web-experiences to decide whether this concept should be GSAP-only, GLB-based Three.js, or fully procedural shaders.
```

```text
Use cinematic-web-experiences to transform this moodboard and brand brief into exact color tokens, section architecture, and animation specs.
```

```text
Use fal-ai-community/skills to generate a hero image, texture, and looping background video for a luxury brand, then use cinematic-web-experiences to integrate them into a GSAP + Three.js landing page.
```

```text
Use cinematic-web-experiences with pretext to design a typography-led landing page with balanced multiline headlines, draggable editorial text composition, and clear responsive text rules.
```
