# The Build Loop

An [Agent Skill](https://agentskills.io) that runs the Build Loop operating model inside your AI tool.

> Frame the problem. Build something testable. Validate with real people. Decide.

A short Qualify step checks the decision is worth a loop at all, then four modes: Frame, Create, Validate, Decide. Learn more at [thebuildloop.com](https://thebuildloop.com).

## Install

Download `build-loop.zip` from [the latest release](https://github.com/rosspchapman/build-loop-skill/releases/latest), then:

**Claude** — go to **Customize → Skills**, click **+**, then **+ Create skill**, then **Upload a skill**, and upload the zip. Skills need code execution enabled.

**Claude Code** — unzip into `~/.claude/skills/build-loop/`.

**Codex** — unzip into `~/.agents/skills/build-loop/`, so that `SKILL.md` sits inside that folder. Restart Codex, then run `/skills` or type `$` to call it. To scope it to one repo instead, use `.agents/skills/` at the repo root.

## Releases

This repo versions and distributes the skill. Each release attaches three assets:

| Asset | What it's for |
|-------|---------------|
| `build-loop.zip` | All of the above — a folder with `SKILL.md` inside it |
| `SKILL.md` | The raw file, to read or place yourself |
| `build-loop.skill` | Claude's bundle format, kept so older links keep working |

The "always latest" download URLs:

```
https://github.com/rosspchapman/build-loop-skill/releases/latest/download/build-loop.zip
https://github.com/rosspchapman/build-loop-skill/releases/latest/download/SKILL.md
```

## Format

One `SKILL.md` file, no vendor lock-in. It follows the [open Agent Skills format](https://agentskills.io) — originally developed by Anthropic, released as an open standard, and since adopted by a growing number of agent products.

The frontmatter stays inside the spec (`name`, `description`, `metadata`), so the same file works across tools that support the format. Tool-specific fields are deliberately avoided: they cause hard errors on upload outside the tool that defines them.
