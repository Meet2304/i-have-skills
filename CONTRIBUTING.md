# Contributing

## Personal skills

Add skills authored or maintained by Meet under `skills/personal/<skill-id>/`.

## Community skills

Before adding a third-party skill:

1. Confirm that its license permits redistribution.
2. Preserve its license and copyright notices.
3. Record the original author, upstream URL, and pinned revision in `skill.yaml`.
4. Keep upstream content intact where practical; document local changes.
5. Never copy a skill whose redistribution terms are missing or incompatible.

## Naming

Use lowercase kebab-case for skill IDs and directory names.

## Required files

Every skill requires `SKILL.md` and `skill.yaml`. Optional supporting material belongs in `scripts/`, `references/`, `assets/`, or `tests/`.

## Changes

Keep canonical instructions harness-neutral. Put platform-specific installation details or transformations under `adapters/`.
