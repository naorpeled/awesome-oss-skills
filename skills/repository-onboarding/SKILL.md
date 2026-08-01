---
name: repository-onboarding
description: >-
  Onboard a contributor to an open source repository using the project's
  README, contribution docs, templates, and policy files. Use when a user
  wants to understand how a repository works before contributing.
metadata:
  author: naorpeled
  version: "1.0.0"
---

# Repository onboarding

Use this skill when a contributor needs a fast, reliable orientation to a
repository before making changes.

## Primary inputs

- `README.md`
- `CONTRIBUTING.md`
- `DEVELOPER.md`, `developer.md`, or `docs/development.md`
- `CODE_OF_CONDUCT.md`
- `SECURITY.md`
- issue templates and pull request templates
- architecture or docs folders

## Instructions

1. Read the repository's high-signal docs first.
2. Summarize:
   - what the project does
   - who it is for
   - how contributors are expected to work
3. Extract the contributor workflow:
   - setup steps
   - build, test, and lint commands
   - branching or commit expectations
   - pull request expectations
4. Identify project norms:
   - code of conduct or communication rules
   - security reporting instructions
   - labels or issue types that indicate where help is needed
5. End with the smallest sensible next steps for the contributor.

## Recommendations to apply

- Prefer reading the room before suggesting changes.
- Point new contributors to documentation and small starter work first.
- Highlight non-code ways to contribute when the repository supports them.
- If the repo uses labels such as `good first issue` or `help wanted`, call
  them out explicitly.

## Output format

Return:

- a short repository summary
- a checklist of first setup steps
- the most important repo norms
- a list of suggested next tasks for a newcomer
