---
name: project-bootstrap
description: >-
  Bootstrap a brand-new open source project, including choosing a license,
  scaffolding baseline docs and configuration, and setting up initial
  repository health files. Use when a user wants to start a new repository
  from scratch.
metadata:
  author: naorpeled
  version: "1.0.0"
---

# Project bootstrap

Use this skill when a maintainer is starting a new project and needs the
baseline files and decisions a healthy open source repository should have
from day one.

## Primary inputs

- the project's goals, language/runtime, and intended audience
- any existing files in the new repository (if not fully empty)
- organization or personal defaults for licensing, if any are already stated
- package manager manifests to be created (e.g. `package.json`,
  `pyproject.toml`, `go.mod`)

## Instructions

### Choose a license

1. Ask whether the project should be open source and, if so, what usage the
   maintainer wants to allow or restrict (e.g. permissive vs. copyleft,
   patent grants, commercial use).
2. If the maintainer has no preference, recommend a widely used permissive
   license such as MIT or Apache-2.0 for most projects, and explain the
   practical difference (Apache-2.0 adds an explicit patent grant; MIT is
   shorter and simpler).
3. Point to [choosealicense.com](https://choosealicense.com) for edge cases
   (e.g. copyleft with GPL/AGPL, or no-license "all rights reserved").
4. Add a `LICENSE` file with the chosen license text and the correct
   copyright holder and year.
5. If the project depends on other licensed code, confirm the chosen license
   is compatible with those dependencies.

### Scaffold baseline files

1. Use the ecosystem's standard scaffolding tool when one exists (e.g.
   `npm init`, `cargo init`, `go mod init`, language-specific project
   templates) instead of hand-writing manifests.
2. Add or generate:
   - `README.md` with project name, purpose, install/usage instructions, and
     a link to contribution docs
   - `CONTRIBUTING.md` describing setup, workflow, and pull request
     expectations
   - `CODE_OF_CONDUCT.md` (e.g. the Contributor Covenant)
   - `.gitignore` matching the project's language/tooling
   - a basic CI workflow that installs dependencies and runs lint/tests
   - issue and pull request templates if the host platform supports them
3. Keep initial scaffolding minimal and working rather than exhaustive;
   prefer a small set of files that build and run cleanly over a large,
   partially-configured template.

### Set expectations for ongoing health

1. Note which files a maintainer should revisit as the project grows (e.g.
   `SECURITY.md` once there are real users, a changelog once there are
   releases).
2. Suggest enabling repository settings that support healthy contribution
   (e.g. branch protection, required status checks) once CI exists.

## Recommendations to apply

- Default to a permissive, well-known license unless the maintainer states
  other requirements.
- Prefer official scaffolding tools over manually created config files to
  reduce mistakes.
- Keep the first commit's scope narrow: license, README, contribution docs,
  and a working CI check are enough to start.

## Output format

Return:

- the recommended license and a short justification
- the list of files created or scaffolded
- any follow-up decisions the maintainer should revisit later
