# Workflow Summary

This skill teaches a repeatable process for:

- locking visual identity before motion
- choosing the right animation stack
- architecting sections before animation specs
- writing exact GSAP and Three.js instructions
- declaring files and external assets explicitly
- locking responsive behavior at the end

## What the workflow covers

The canonical guide includes:

- the six-phase framework
- stack selection rules
- the universal prompt template
- exact animation-spec wording patterns
- asset declaration patterns
- responsive lock-down rules
- reusable GSAP snippets

## Companion stack

The core skill does not require any external API, but it can pair well with `fal-ai-community/skills` for image-led or video-led work.

Repo: [fal-ai-community/skills](https://github.com/fal-ai-community/skills)

Typical uses for `fal` in this workflow:

- generate hero images, motion plates, textures, and supporting visuals before prompt integration
- provide source material to animate, layer, and sequence in the final build
- support image-led site concepts such as luxury, editorial, fashion, hospitality, architecture, and product storytelling

Suggested use:

1. Use the fal skills to generate concept art, background loops, textures, or other visual assets.
2. Save the resulting media into your project.
3. Use `cinematic-web-experiences` to integrate those assets into the final site prompt with explicit paths, animation specs, and responsive behavior.

If a project already has assets or is fully procedural, you can skip `fal`.

For typography-heavy frontends, this workflow can also pair well with `pretext`.

Repo: [chenglou/pretext](https://github.com/chenglou/pretext)

Typical use:

1. Use `pretext` when the design relies on tight editorial text lockups, dynamic multiline headings, balanced callouts, or text-heavy cards where line breaks matter visually.
2. Measure and lay out text ahead of time instead of relying on repeated DOM measurements.
3. Keep `cinematic-web-experiences` focused on the visual system, motion, and section architecture while `pretext` handles text measurement accuracy.

## Canonical reference

For the full workflow, use `shared/cinematic-web-experiences/guide.md`.
