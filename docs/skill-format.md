# Portable skill format

## `SKILL.md`

The canonical instruction document. It should explain when the skill applies, the workflow to follow, safety constraints, and any supporting files the agent must read or execute.

## `skill.yaml`

Use the metadata template in `templates/skill/skill.yaml`.

Required fields:

- `id`
- `name`
- `description`
- `origin`
- `license`
- `compatibility`

For community skills, also set `source.url` and pin `source.revision` to a commit or release. Do not use a floating branch name as the only provenance record.

## Supporting directories

- `scripts/`: deterministic helpers used by the skill.
- `references/`: documentation loaded only when needed.
- `assets/`: templates and non-instruction resources.
- `tests/`: validation fixtures or smoke tests.

Harness-specific generated files belong in `adapters/`, not inside the canonical skill unless they are part of the upstream skill.
