---
name: maintainer-triage-and-review
description: >-
  Support maintainers with issue triage, pull request review, onboarding
  audits, and documentation upkeep using the repository's templates, docs, and
  conventions. Use when a maintainer needs recurring or one-off repository
  health help.
metadata:
  author: naorpeled
  version: "1.0.0"
---

# Maintainer triage and review

Use this skill for ongoing maintainer workflows and targeted repo-health
improvements.

## Primary inputs

- issue templates
- pull request templates
- `README.md`
- `CONTRIBUTING.md`
- `DEVELOPER.md` or `docs/development.md`
- labels, governance docs, and repository conventions
- `AGENTS.md`/`CLAUDE.md` and output from automated review bots

## Instructions

### Ongoing workflows

1. Triage incoming issues by classifying them as bug, feature, question, docs,
   or support.
2. Request missing reproduction steps, expected behavior, or environment
   details when needed.
3. Review pull requests against the documented contribution and validation
   rules.
4. Check whether contributor-facing docs still match actual repository
   behavior.
5. Weigh findings from automated code review or compliance bots against the
   actual code before asking a contributor to act on them.

### One-off improvements

1. Audit whether a newcomer can understand the project from its top-level docs.
2. Improve templates or contribution guidance when repeated confusion appears.
3. Suggest clearer documentation paths for non-code contributions and beginner
   issues.

## Recommendations to apply

- Treat documentation, labeling, and review clarity as maintainer work, not
  just code review.
- Encourage beginner-friendly issue labeling where appropriate.
- Surface missing onboarding details that slow down first-time contributors.
- Give specific, actionable feedback in a friendly tone, and invite the
  contributor's input on open design questions rather than dictating them.

## Output format

Return one or more of:

- triage notes and follow-up questions
- review feedback grounded in repo conventions
- documentation drift findings
- a short list of maintainer improvements
