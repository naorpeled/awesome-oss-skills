# Contributing

Thanks for your interest in contributing to `awesome-oss-skills`! This repo
is a catalog of [Agent Skills](https://agentskills.io/) for onboarding
open source contributors and helping maintainers run healthy repositories.
Contributions of new skills, improvements to existing skills, and catalog
fixes are all welcome.

## Repository structure

- `skills/<skill-name>/SKILL.md` — one skill per directory, using the Agent
  Skills package layout
- `skills.sh.json` — grouping metadata used by skills catalogs
- `README.md` — package overview, install instructions, and the skill list

## Ways to contribute

- Add a new skill for a recurring contributor or maintainer workflow that
  isn't covered yet
- Improve an existing skill's instructions, inputs, or recommendations
- Fix inaccuracies or broken links in the catalog
- Improve this documentation

## Adding or updating a skill

1. Create a new directory under `skills/` named after the skill (kebab
   case), containing a single `SKILL.md` file.
2. Follow the shape used by existing skills:
   - YAML frontmatter with `name`, `description`, and `metadata` (`author`,
     `version`)
   - a short intro describing when to use the skill
   - `## Primary inputs` — the repo files or context the skill reads
   - `## Instructions` — the concrete steps the skill follows
   - `## Recommendations to apply` — the guidance or best practices it
     should incorporate
   - `## Output format` — what the skill should return
3. Add the new skill to the relevant grouping in `README.md` and
   `skills.sh.json` so it shows up in the catalog.
4. Keep skills scoped to one workflow. If a skill is trying to cover both
   contributor and maintainer concerns, consider splitting it.

## Validating changes

This repository has no build step or test suite; changes are markdown and
JSON only. Before opening a pull request:

- Confirm `skills.sh.json` is valid JSON (for example, `python3 -c
  "import json; json.load(open('skills.sh.json'))"`).
- Confirm every skill listed in `README.md` and `skills.sh.json` has a
  matching `skills/<skill-name>/SKILL.md` file, and vice versa.
- Check that any links you add resolve correctly.

## Pull request expectations

- Keep pull requests focused on a single skill or catalog change.
- Describe which workflow or gap the change addresses.
- Update `README.md` and `skills.sh.json` in the same pull request as any
  skill you add, rename, or remove.
