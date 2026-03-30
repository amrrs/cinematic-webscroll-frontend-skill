# Cinematic Web Experiences

Cross-tool skill package for planning and prompting cinematic websites with:

- GSAP `ScrollTrigger`
- Three.js scenes
- custom shaders
- cinematic loading screens
- responsive scroll-based motion systems

The core workflow works on its own. For image-led or video-led builds, it can pair with [`fal-ai-community/skills`](https://github.com/fal-ai-community/skills). For typography-led interfaces with precise multiline layout, it can pair with [`pretext`](https://github.com/chenglou/pretext).

## What this repo includes

This repo packages the same workflow for:

- `Cursor`
- `Codex`
- `Claude Code`

The canonical deep reference lives in `shared/cinematic-web-experiences/guide.md`.

## Included demo

The repo includes a working demo site for `Aurel Gates` built from the same workflow:

- `index.html`
- `styles.css`
- `main.js`

The demo uses:

- `fal`-generated hero image, texture, and background loop
- GSAP + Three.js motion system
- pinned hero and scroll-driven reveals
- typography-led touches powered by `pretext`

Run it locally:

```bash
python3 -m http.server 4173
```

Then open [http://127.0.0.1:4173](http://127.0.0.1:4173).

![Aurel Gates demo screenshot](./assets/aurel-gates-demo-screenshot.png)

## Quick start

1. Clone or copy this repo into the project where you want the skill available.
2. Keep the hidden skill folders and root guidance files intact:
   - `.cursor/`
   - `.codex/`
   - `.claude/`
   - `CLAUDE.md`
   - `AGENTS.md`
3. Use the skill name `cinematic-web-experiences` in your prompt when needed.

Example:

```text
Use cinematic-web-experiences to help me design a premium GSAP + Three.js landing page.
```

## Docs

- Setup and local run instructions: `docs/setup.md`
- Platform usage for Cursor, Codex, and Claude Code: `docs/platforms.md`
- Prompt examples for core, fal, and pretext workflows: `docs/prompts.md`
- Workflow summary and what the skill teaches: `docs/workflow.md`
- Canonical deep reference: `shared/cinematic-web-experiences/guide.md`

## Repo layout

```text
.cursor/skills/cinematic-web-experiences/
.codex/skills/cinematic-web-experiences/
.claude/commands/cinematic-web-experiences.md
.claude/cinematic-web-experiences.md
shared/cinematic-web-experiences/guide.md
docs/
CLAUDE.md
AGENTS.md
```

## Publishing notes

- Keep `.claude`, `.codex`, and `.cursor` committed so the skills stay available on GitHub.
- Keep `CLAUDE.md` and `AGENTS.md` in the repo root.
- Keep `.env` out of version control and commit only `.env.example`.
- Tell users they can either use this repo directly or copy the relevant platform folder into an existing project.
