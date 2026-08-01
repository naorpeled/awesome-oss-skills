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
- a repository/issue discovery source when no repository is chosen yet
  (e.g. the [goodfirstissues data
  feed](https://github.com/iedr/goodfirstissues/blob/master/backend/data.json),
  up-for-grabs.net, goodfirstissues.com, goodfirstissue.dev, CodeTriage, or
  firstcontributions/first-contributions)
- `README.md`
- `CONTRIBUTING.md`
- relevant code or docs files
- issue labels, issue templates, and pull request templates

## Instructions

### Confirm which repository to use

1. Check whether the current working context is already inside a cloned
   repository (e.g. a `.git` directory is present).
2. If it is, do not assume that repository is the target. Ask the
   contributor whether they want to work in the current repository or a
   different one before doing any deeper investigation.
3. If they confirm the current repository, gather context directly from it
   (skip discovery sources below). Otherwise, or if there is no repository
   present at all, continue with the discovery step below.

### When no repository is specified yet

1. If the contributor has not picked a repository or issue, help them find
   one using well-known discovery sources instead of guessing:
   - [goodfirstissues data
     feed](https://github.com/iedr/goodfirstissues/blob/master/backend/data.json)
     as the first stop — a frequently updated, scraped dataset of live
     `good first issue`-labeled issues across many projects
   - [firstcontributions/first-contributions](https://github.com/firstcontributions/first-contributions#first-contributions)
     for a hands-on, no-stakes practice contribution
   - [up-for-grabs.net](https://up-for-grabs.net) for projects that actively
     want help and label issues `up-for-grabs`, `jump-in`, or `help wanted`
   - [goodfirstissues.com](https://goodfirstissues.com) for the latest issues
     labeled `good first issue`
   - [goodfirstissue.dev](https://goodfirstissue.dev/) for curated easy
     issues from popular projects
   - [CodeTriage](https://www.codetriage.com/) to subscribe to a project and
     receive a new open issue to work on regularly
2. Match the source to the contributor's goal: prefer the goodfirstissues
   data feed when they want a real, currently open issue to pick from right
   now, use `first-contributions` for a pure workflow-learning exercise, and
   the other aggregator sites/CodeTriage when they want a real issue in a
   project they may keep contributing to.
3. Once a candidate repository or issue is chosen, continue with the steps
   below.

### With a repository and issue in hand

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
