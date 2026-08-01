# awesome-oss-skills

A collection of [Agent Skills](https://agentskills.io/) for onboarding open
source contributors and helping maintainers run healthy repositories.

These skills are packaged in the `SKILL.md` format so they can be installed
with Vercel's skills CLI:

```bash
npx skills add naorpeled/awesome-oss-skills
```

## Available skills

### Contributors

- `repository-onboarding`
  - Summarize a repository from `README.md`, `CONTRIBUTING.md`,
    `CODE_OF_CONDUCT.md`, developer docs, and templates.
- `local-development-bootstrap`
  - Extract setup, build, test, and lint steps from docs and config files.
- `first-oss-contribution`
  - Help a contributor pick a small first change, understand the workflow, and
    prepare a pull request.

### Maintainers

- `maintainer-triage-and-review`
  - Support issue triage, PR review, documentation drift checks, and
    contributor-onboarding audits.
- `maintainer-ci-and-release-health`
  - Audit cross-platform CI coverage, release automation, distribution
    channel consistency, and agent-instruction files.

### Pull request workflows

- `green-pr`
  - Resolve AI code review comments, fix failing CI checks, and address
    human review feedback with user-approved replies until a PR is
    mergeable.

## Repository structure

This repository follows the Agent Skills package layout used by the Vercel
skills CLI:

- `skills/<skill-name>/SKILL.md` — one skill per directory
- `skills.sh.json` — grouping metadata for skills catalogs
- `README.md` — package overview and installation instructions

## Skill design goals

Each skill in this repository should:

- start from common repository artifacts such as `README.md`,
  `CONTRIBUTING.md`, developer docs, templates, and policy files
- help either contributors or maintainers complete a concrete task
- support both one-off tasks and ongoing repository workflows
- reduce onboarding friction for new developers
- incorporate open source contribution guidance such as:
  - start small
  - look for documentation and `good first issue` style work
  - read project norms before making changes
  - communicate clearly and respond to review feedback
