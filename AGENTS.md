# AGENTS.md

## Overview

`awesome-oss-skills` is a catalog of [Agent Skills](https://agentskills.io/)
packaged for onboarding open source contributors and helping maintainers run
healthy repositories. There is no application code, build step, or runtime —
this repository is entirely Markdown and JSON:

- `skills/<skill-name>/SKILL.md` — one skill per directory, using the Agent
  Skills package layout so skills are installable via Vercel's skills CLI
  (`npx skills add naorpeled/awesome-oss-skills`)
- `skills.sh.json` — grouping metadata used by skills catalogs
- `README.md` — package overview, install instructions, and the skill list
- `CONTRIBUTING.md` — contribution workflow for this repository

## Setup

No install step is required. Clone the repository and edit files directly.

## Build & test commands

There is no build. Validate changes with:

```bash
python3 -c "import json; json.load(open('skills.sh.json'))"
```

This confirms `skills.sh.json` is valid JSON. There is no other automated
test suite; validation is manual (see "Boundaries" and "Consistency checks"
below).

## Code style

- Markdown only, prose wrapped to roughly 80 columns to match existing files.
- Every `SKILL.md` uses YAML frontmatter with `name`, `description`, and
  `metadata` (`author`, `version`), followed by these sections in order:
  `## Primary inputs`, `## Instructions`, `## Recommendations to apply`,
  `## Output format`. Write `description` as a folded block scalar
  (`description: >-`) wrapped to roughly 80 columns rather than a single
  long line, so the frontmatter matches the wrapping rule while still
  parsing as one string.
- Keep skill names kebab-case and matching their directory name.

## Consistency checks

Before committing a change that adds, renames, or removes a skill:

- Every skill under `skills/` must appear in both `README.md` and
  `skills.sh.json`, and vice versa.
- Links referenced in `README.md`, `CONTRIBUTING.md`, or skill files must
  resolve correctly.

## Boundaries

- Always: keep each skill scoped to a single contributor or maintainer
  workflow. Split a skill rather than let it cover unrelated concerns.
- Ask first: introducing new top-level catalog files or restructuring the
  grouping scheme in `skills.sh.json`.
- Never: fabricate tooling, sites, or bot names in a skill's guidance —
  only include sources that are verifiable and directly relevant.

## Pull request guidelines

- Keep pull requests focused on a single skill or catalog change.
- Update `README.md` and `skills.sh.json` in the same pull request as any
  skill you add, rename, or remove.
- Describe which contributor or maintainer workflow the change addresses.
