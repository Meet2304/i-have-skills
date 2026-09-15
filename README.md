# Master Skills

A portable collection of personal and community-built AI agent skills for use across coding harnesses.

## Purpose

Master Skills is the source of truth for reusable instructions, workflows, scripts, and references that can be shared across projects and adapted to different AI coding agents.

- Keep skills harness-agnostic whenever possible.
- Separate original skills from third-party skills.
- Preserve attribution, source revisions, and licenses.
- Put harness-specific installation or translation logic in `adapters/`.

## Repository layout

```text
master-skills/
├── skills/
│   ├── personal/          # Skills authored or substantially maintained by Meet
│   └── community/         # Third-party skills preserved with attribution
├── adapters/              # Harness-specific installation and compatibility notes
├── templates/skill/       # Starter files for a new skill
├── docs/                  # Format and maintenance guidance
└── registry.yaml          # Searchable index of all skills
```

## Skill contract

Each skill lives in its own directory and should include:

- `SKILL.md` — the instructions an agent reads.
- `skill.yaml` — portable metadata, ownership, compatibility, and provenance.
- Optional `scripts/`, `references/`, `assets/`, and `tests/` directories.

Third-party skills must retain their original copyright and license files. Their `skill.yaml` must record the upstream URL and pinned revision so changes remain auditable.

## Add a skill

1. Copy `templates/skill/` into `skills/personal/<skill-id>/` or `skills/community/<skill-id>/`.
2. Write the skill instructions in `SKILL.md`.
3. Complete `skill.yaml`, including provenance for community skills.
4. Add the skill to `registry.yaml`.
5. Add or update a harness adapter only when the skill needs harness-specific behavior.

## Portability

The canonical skill stays under `skills/`. Adapters may copy, link, or translate it into the directory layout expected by a particular harness, but generated copies should not become the source of truth.

## Status

The repository structure is ready. Skills and harness adapters will be added as they are collected.

## Included skills

| Skill | Origin | Purpose |
|---|---|---|
| [i-have-adhd](skills/community/i-have-adhd/) | [ayghri/i-have-adhd](https://github.com/ayghri/i-have-adhd) | ADHD-friendly output and execution style |
| [frontend-design](skills/community/frontend-design/) | [anthropics/skills](https://github.com/anthropics/skills) | Distinctive, intentional frontend design |
| [docker-compose-workshop](skills/community/docker-compose-workshop/) | [14-848 Cloud Infrastructure](https://github.com/14-848-Cloud-Infrastructure/docker-compose) | Docker Compose fundamentals through a WordPress/MySQL lab |
