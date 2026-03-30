# Setup

## Core skill setup

No build step is required for the core skill. The repo-local files are already in the right places for:

- `Cursor`
- `Codex`
- `Claude Code`

If you are reusing the skill in another project, copy the platform-specific folders and root guidance files you need:

- `.cursor/skills/cinematic-web-experiences/`
- `.codex/skills/cinematic-web-experiences/`
- `.claude/`
- `CLAUDE.md`
- `AGENTS.md`

## Optional fal setup

If you want to generate images, textures, or video backgrounds as part of the workflow, use `fal` before integrating the final assets into the site build.

1. Copy `.env.example` to `.env`.
2. Add your fal API key:

```env
FAL_KEY=your_real_key_here
```

3. Keep `.env` local only. It is gitignored by default.
4. Use the companion fal scripts or repo before integrating the final assets back into the website workflow.

This matches the fal community skills expectation that `FAL_KEY` is provided before running generation or model-search scripts in [`fal-ai-community/skills`](https://github.com/fal-ai-community/skills).

`fal` is optional. Use it when the project needs generated source assets such as images, textures, or loops.

## Optional pretext setup

If your frontend is typography-led or you need deterministic multiline text layout:

```bash
npm install @chenglou/pretext
```

`pretext` is especially useful when you want to:

- pre-measure multiline headings without repeated DOM reads
- reduce layout shift for dynamic copy
- render balanced text in DOM, canvas, or SVG
- avoid `getBoundingClientRect` / `offsetHeight`-style layout reflow loops in text-heavy UI

Repo: [chenglou/pretext](https://github.com/chenglou/pretext)

## Running the demo locally

From the repo root:

```bash
python3 -m http.server 4173
```

Then open:

```text
http://127.0.0.1:4173
```
