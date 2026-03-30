# Platform Guide

## Cursor

Cursor reads the repo-local skill from:

` .cursor/skills/cinematic-web-experiences/ `

What is included:

- `SKILL.md`: short trigger-focused skill entry
- `reference.md`: compact Cursor-friendly playbook

How to use it:

1. Open this repo, or copy `.cursor/skills/cinematic-web-experiences/` into another repo.
2. Ask Cursor for a cinematic website workflow, prompt, or architecture.
3. Mention the skill name explicitly if needed.

Example:

```text
Use cinematic-web-experiences to write a prompt for a shader-driven microsite with GSAP scroll choreography.
```

More examples:

```text
Use cinematic-web-experiences to plan a dark editorial landing page with pinned hero sections and scroll-triggered reveals.
```

```text
Use cinematic-web-experiences to turn this brand brief into a GSAP + Three.js build prompt with exact color values and section architecture.
```

## Codex

Codex reads the skill from:

` .codex/skills/cinematic-web-experiences/ `

What is included:

- `SKILL.md`: skill trigger and workflow summary
- `references/guide.md`: Codex-local reference
- `agents/openai.yaml`: UI metadata for the skill
- `AGENTS.md`: repo-level guidance

How to use it:

1. Open this repo in Codex, or copy `.codex/skills/cinematic-web-experiences/` into a repo where you want it available.
2. Keep `AGENTS.md` in the repo root so Codex has a clear top-level hint.
3. Invoke the skill by name in your prompt.

Example:

```text
Use $cinematic-web-experiences to create a multi-section website concept with a fixed Three.js canvas and exact ScrollTrigger settings.
```

More examples:

```text
Use $cinematic-web-experiences to choose between a GSAP-only build and a GLB-based Three.js build for this luxury interior brand.
```

```text
Use $cinematic-web-experiences to produce a final builder-ready prompt for a cinematic hero with shader-based background distortion.
```

## Claude Code

Claude Code uses:

- `CLAUDE.md`
- `.claude/cinematic-web-experiences.md`
- `.claude/commands/cinematic-web-experiences.md`

How to use it:

1. Open this repo in Claude Code, or copy the `.claude/` folder and `CLAUDE.md` into another repo.
2. Ask naturally for help with a cinematic site, or use the slash command:

```text
/cinematic-web-experiences
```

3. Pass a concept, brand brief, or rough goal after the command if useful.

Examples:

```text
/cinematic-web-experiences Create a prompt for a near-black fashion site with lime accents, pinned hero motion, and procedural shader background.
```

```text
Use the cinematic web workflow to convert this rough idea into a structured prompt with exact sections, animations, and responsive rules.
```

## What each platform should read

If you are adapting this repo or debugging behavior, these are the key files:

- Canonical workflow: `shared/cinematic-web-experiences/guide.md`
- Cursor wrapper: `.cursor/skills/cinematic-web-experiences/SKILL.md`
- Codex wrapper: `.codex/skills/cinematic-web-experiences/SKILL.md`
- Claude wrapper: `.claude/cinematic-web-experiences.md`
- Claude slash command: `.claude/commands/cinematic-web-experiences.md`
- Repo-level Codex hint: `AGENTS.md`
- Repo-level Claude hint: `CLAUDE.md`
