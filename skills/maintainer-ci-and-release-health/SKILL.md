---
name: maintainer-ci-and-release-health
description: Help maintainers keep CI, release automation, and distribution channels healthy and consistent across a repository's workflows, packaging manifests, and agent-instruction files. Use when a maintainer needs to audit or improve CI coverage, releases, or multi-channel distribution.
metadata:
  author: naorpeled
  version: "1.0.0"
---

# Maintainer CI and release health

Use this skill for recurring checks on continuous integration, release
automation, and package distribution, and for keeping agent-instruction files
in sync with the conventions they are meant to enforce.

## Primary inputs

- `.github/workflows/*.yml`
- release tooling such as `.goreleaser.yml`, `Makefile`, or `package.json`
  scripts
- distribution manifests: npm `package.json`, Homebrew formulas, install
  scripts (`install.js`, `install.sh`)
- `AGENTS.md`, `CLAUDE.md`, or other agent-instruction files
- automated code review or CI bot output (e.g. compliance or lint findings)

## Instructions

### Ongoing workflows

1. Check that CI runs the same validation on every platform the project
   ships for (e.g. Linux, macOS, Windows), not just the maintainer's default
   environment.
2. Verify pull request validation workflows and nightly/scheduled smoke tests
   stay aligned with the current build and release process.
3. When a release changes install paths (npm, Homebrew, binaries), confirm
   every distribution channel was updated together, not just one.
4. Cross-check automated review or compliance bot findings against the
   project's documented conventions (e.g. `AGENTS.md`) to confirm they are
   still accurate, and flag stale or contradictory rules.

### One-off improvements

1. Add missing cross-platform coverage to CI when a bug report is
   platform-specific.
2. Consolidate duplicated install/build logic across distribution channels.
3. Update `AGENTS.md`/`CLAUDE.md` when project conventions change so
   AI-assisted contributions and automated reviewers stay accurate.

## Recommendations to apply

- Treat CI, release, and distribution consistency as maintainer work, on par
  with code review.
- Prefer fixing the root cause once (e.g. shared install logic) over
  patching each platform or channel separately.
- Keep agent-instruction files (`AGENTS.md`, `CLAUDE.md`) as living documents
  that reflect current conventions, since automated reviewers and
  AI-assisted contributors rely on them.
- When responding to automated review findings, verify them against the
  actual code before asking a contributor to act on them.

## Output format

Return one or more of:

- a list of platform or channel gaps in CI, release, or distribution
- specific workflow or manifest changes to close those gaps
- notes on agent-instruction files that are stale or inconsistent with the
  codebase
