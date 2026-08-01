---
name: green-pr
description: >-
  Drive an open pull request to a mergeable, "all green" state by resolving AI
  code review comments, fixing failing CI checks, and addressing human review
  feedback. Use when a contributor or maintainer wants a PR's checks and
  review threads cleared before merge.
metadata:
  author: naorpeled
  version: "1.0.0"
---

# Green PR

Use this skill to work an existing pull request toward a fully green state:
every automated review comment resolved, every CI check passing, and every
human review thread addressed.

## Primary inputs

- the pull request's diff, commits, and description
- automated code review comments (e.g. Qodo, Copilot code review, CodeQL,
  Baz, CodeRabbit, Greptile, BugBot)
- CI check runs and their logs (unit tests, lint, type checks, mutation
  testing, platform-specific test jobs)
- human reviewer comments and review threads
- repository conventions from `CONTRIBUTING.md`, `AGENTS.md`, or similar

## Instructions

### 1. Resolve AI code review comments

1. Collect every open comment from automated reviewers (bots such as Qodo,
   Copilot code review, Baz, CodeRabbit, Greptile, or BugBot, and static
   analysis like CodeQL).
2. For each finding, verify it against the actual code before acting — AI
   review comments can be stale, duplicated, or based on a misunderstanding.
3. Apply a fix for genuine issues. If a finding is a false positive, leave it
   unresolved with a short note explaining why, rather than silently
   dismissing it.
4. Mark each addressed thread as resolved once the fix is committed.

### 2. Make CI pass

1. List all required CI checks for the PR (tests across platforms, lint,
   type-check, security scans, mutation testing, etc.).
2. For each failing check, pull the job logs and fix the root cause rather
   than only the symptom.
3. Re-run or wait for checks after each fix, and keep iterating until every
   required check is green.

### 3. Address human review feedback

1. For each human reviewer comment or requested change, make the
   corresponding code change first.
2. Do not post a reply on the maintainer's or reviewer's behalf. Instead,
   prompt the user with a suggested reply for each thread:
   - concise and minimal
   - human-readable
   - includes a precise explanation of what changed and why (or a precise
     answer if it was a question)
3. Let the user approve, edit, or reject each suggested reply before it is
   posted.

## Recommendations to apply

- Treat AI and human review the same way in terms of rigor: verify before
  fixing, and fix root causes.
- Never assume an AI reviewer finding is correct just because it was flagged;
  confirm it against the code and existing conventions first.
- Keep replies to human reviewers short — a one-line "Done" style reply is
  often enough once the fix is clear from the commit, but always let the user
  have the final say on tone and content.
- Treat "green" as checks passing AND review threads resolved, not just CI
  status.

## Output format

Return:

- a checklist of AI review comments and how each was addressed (fixed /
  false positive with reason)
- a checklist of CI checks and their final status, with root-cause notes for
  any fixes
- for each human review thread: the code change made, plus a suggested reply
  for the user to approve before posting
