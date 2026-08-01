# awesome-oss-skills

A repository of reusable skills for contributing to and maintaining open source
projects.

## Goal

This repo is focused on two audiences:

1. **Contributors** who need help onboarding into a new repository.
2. **Maintainers** who need repeatable help with review, triage, and
   documentation upkeep.

The skills in this repository should be grounded in the files and conventions
that most healthy repositories already use, especially:

- `README.md`
- `CONTRIBUTING.md`
- `DEVELOPER.md` / `docs/development.md`
- `CODE_OF_CONDUCT.md`
- `SECURITY.md`
- issue templates
- pull request templates
- architecture or docs folders

## Skill categories

### Contributor onboarding skills

Skills that help a new or returning contributor understand how to work in a
repository.

- **Repository onboarding**
  - Summarize the project purpose, setup steps, development workflow, and ways
    to contribute from `README.md`, `CONTRIBUTING.md`, and development docs.
- **First contribution guide**
  - Identify beginner-friendly paths such as docs fixes, tests, small bug fixes,
    or labeled issues.
- **Local development bootstrap**
  - Extract install, build, test, and lint commands from contributor and
    developer documentation.
- **Contribution expectations**
  - Explain branching, commit, testing, and review expectations from
    `CONTRIBUTING.md` and PR templates.
- **Documentation map**
  - Point contributors to the right docs for setup, architecture, style, and
    release practices.

Current skills:

- [`skills/repository-onboarding.md`](skills/repository-onboarding.md)
- [`skills/local-development-bootstrap.md`](skills/local-development-bootstrap.md)

### Contributor one-off skills

Skills that help with a single contribution task.

- **Issue-to-plan**
  - Turn an issue into a small implementation plan using repository docs and
    local code context.
- **Docs improvement helper**
  - Improve unclear setup steps, API usage examples, or contribution guidance.
- **PR readiness check**
  - Verify that a change matches documented contribution expectations before
    opening a pull request.

Current skills:

- [`skills/first-contribution-plan.md`](skills/first-contribution-plan.md)

### Maintainer ongoing skills

Skills that help maintainers keep a repository healthy over time.

- **Issue triage**
  - Classify incoming issues, request missing details, and route bugs,
    questions, and feature requests.
- **Pull request review support**
  - Review changes against project docs, contribution rules, and repository
    conventions.
- **Documentation drift review**
  - Compare current repo behavior with `README.md`, `CONTRIBUTING.md`, and
    developer docs to find stale guidance.
- **Contributor onboarding audit**
  - Check whether a new contributor can discover setup steps, project norms, and
    first tasks from common repo files.
- **Maintainer workflow hygiene**
  - Keep issue templates, PR templates, labels, and contributing docs aligned.

Current skills:

- [`skills/maintainer-triage-and-review.md`](skills/maintainer-triage-and-review.md)

### Maintainer one-off skills

Skills that help maintainers make targeted improvements.

- **Create or improve `CONTRIBUTING.md`**
  - Add missing contribution workflow details and expectations.
- **Create or improve developer docs**
  - Fill in setup, testing, architecture, or release guidance.
- **Review process tune-up**
  - Improve pull request templates, review checklists, or contribution
    instructions.
- **Docs restructuring**
  - Reorganize scattered onboarding and maintenance documentation into clearer
    entry points.

## What good skills in this repo should do

Each skill should ideally:

- start from the repository's existing documentation and conventions
- help either a contributor or a maintainer complete a concrete task
- work for both **one-off** tasks and **ongoing** maintenance workflows
- reduce onboarding friction for new developers
- improve project health without requiring repository-specific hardcoding

## Repository structure

- `README.md` — repository purpose and skill index
- `skills/` — reusable contributor and maintainer skills
