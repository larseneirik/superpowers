---
name: requesting-code-review
description: Use when substantial implementation is complete, before merge/PR, or when a fresh review would reduce real risk.
---

# Requesting Code Review

## Goal
Catch correctness, regression, and maintainability issues before integration.

## Use When
- Feature or bugfix is substantial.
- Change touches shared behavior or multiple files.
- Before merge, push, or PR when review is expected.
- You are stuck and need a fresh technical read.

## Do
- Review your own diff first.
- Provide reviewer with requirements, changed files, base/head refs, and verification run.
- Ask for findings ordered by severity.
- Fix critical and important issues before proceeding.
- Push back with code/tests when reviewer is wrong.
- Re-run relevant verification after fixes.

## Do Not
- Request review for tiny low-risk edits unless user asks.
- Send session history instead of precise context.
- Accept vague feedback without checking code.
- Treat reviewer approval as verification.

## Context Shape
```text
Implemented: [short summary]
Requirements: [source or plan]
Changed files: [paths]
Diff/base: [git refs if available]
Verification: [commands/results]
Review for: bugs, regressions, missing tests, scope drift
```

## Workflow
1. Inspect `git diff`.
2. Prepare concise review context.
3. Request review through available Codex/GitHub/multi-agent review path.
4. Evaluate findings.
5. Fix, verify, and summarize.

## Status
Only report when review is requested, blocked, or resolved.
