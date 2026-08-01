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
  - Help a contributor find a project via discovery sources like
    up-for-grabs.net or CodeTriage when they don't have one yet, then pick a
    small first change, understand the workflow, and prepare a pull request.

### Maintainers

- `maintainer-triage-and-review`
  - Support issue triage, PR review, documentation drift checks, and
    contributor-onboarding audits.
- `maintainer-ci-and-release-health`
  - Audit cross-platform CI coverage, release automation, distribution
    channel consistency, and agent-instruction files.
- `project-bootstrap`
  - Bootstrap a new project: choose a license, scaffold baseline docs and
    CI, and flag follow-up repository health work.

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

## Contributing

New to this repository? See [`CONTRIBUTING.md`](CONTRIBUTING.md) for how to
add or update a skill and what a pull request should include. Agent-facing
maintenance instructions live in [`AGENTS.md`](AGENTS.md) (`CLAUDE.md` is a
symlink to the same file).

## License

This project is licensed under the [MIT License](LICENSE).
