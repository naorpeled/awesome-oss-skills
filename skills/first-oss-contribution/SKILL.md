---
name: first-oss-contribution
description: Help a contributor prepare a small first open source contribution using the repository's docs, issue labels, and contribution workflow. Use when a user wants to make a safe, well-scoped first pull request.
metadata:
  author: naorpeled
  version: "1.0.0"
---

# First OSS contribution

Use this skill when a contributor wants to move from orientation to a small,
successful first pull request.

## Primary inputs

- issue text or requested task
- `README.md`
- `CONTRIBUTING.md`
- relevant code or docs files
- issue labels, issue templates, and pull request templates

## Instructions

1. Find the smallest acceptable change that matches the repository's workflow.
2. Prefer starter-friendly work such as:
   - documentation fixes
   - test improvements
   - typo fixes
   - small bug fixes
   - issues labeled `good first issue`, `help wanted`, or equivalent
3. Explain the expected workflow:
   - fork or branch strategy if documented
   - local validation steps
   - pull request expectations
   - how to respond to review feedback
4. Keep the plan intentionally narrow and concrete.
5. Suggest non-code contributions if they are a better fit than code changes.

## Recommendations to apply

- Start small instead of aiming for a large feature.
- Encourage contributors to read the code of conduct and contribution guide
  before opening a pull request.
- Treat review feedback as part of the normal contribution loop.

## Output format

Return:

- a minimal contribution plan
- files or issue areas to inspect first
- validation steps
- a short pull-request-readiness checklist
