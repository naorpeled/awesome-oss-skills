---
name: local-development-bootstrap
description: >-
  Extract local setup, build, test, and lint instructions from repository docs
  and configuration files. Use when a contributor wants to run a project
  locally or verify that setup guidance is complete.
metadata:
  author: naorpeled
  version: "1.0.0"
---

# Local development bootstrap

Use this skill when a contributor wants a clean path from zero to a working
local environment.

## Primary inputs

- `README.md`
- `CONTRIBUTING.md`
- `DEVELOPER.md` or `docs/development.md`
- tool files such as `package.json`, `pyproject.toml`, `go.mod`, `Cargo.toml`,
  `Gemfile`, `Makefile`, and container/dev environment files

## Instructions

1. Collect the documented prerequisites and environment requirements.
2. Extract the setup sequence in the order a new contributor should run it.
3. Confirm the likely build, test, and lint commands from project config files.
4. Flag mismatches between documentation and the actual configuration files.
5. Call out missing details that would block a first-time contributor.

## Recommendations to apply

- Prefer the smallest successful setup path over optional tooling first.
- Mention platform-specific requirements or external services early.
- If documentation is incomplete, suggest a docs update as a valid first
  contribution.

## Output format

Return:

- prerequisites
- ordered setup commands
- build, test, and lint commands
- known gaps or confusing setup instructions
