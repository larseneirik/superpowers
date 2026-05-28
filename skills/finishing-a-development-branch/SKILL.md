---
name: finishing-a-development-branch
description: Use when implementation is complete and the remaining work is verification, commit, push, PR, merge, or branch/worktree cleanup.
---

# Finishing A Development Branch

## Goal
Finish integration deliberately after verification.

## Use When
- Code changes are complete.
- User asks to commit, push, open PR, merge, or clean up.
- A worktree/branch needs a finish decision.

## Do
- Run required verification before success claims.
- Inspect `git status --short`.
- Stage only files in scope.
- Use clear conventional commits when committing.
- Push only when user/repo workflow expects it.
- For PRs, include concise summary and test plan.
- Ask for explicit confirmation before discarding work.

## Do Not
- Merge, push, or delete branches with failing verification unless user explicitly overrides.
- Stage unrelated dirty or untracked files.
- Force-push without explicit request.
- Delete worktrees or branches without confirmation.
- Present branch-cleanup options when user only asked for a status report.

## Workflow
1. Verify: run project-required checks.
2. Inspect: status, branch, diff summary.
3. Decide requested finish path: commit, push, PR, merge, keep, or discard.
4. Execute the chosen path.
5. Re-check status and report result.

## Options When Needed
```text
Choose finish path:
1. Commit only
2. Commit and push
3. Push/open PR
4. Keep branch as-is
5. Discard work (requires exact confirmation)
```

## Status
Short only: verifying, blocked, committed, pushed, PR created, or kept.

## Verify
- Required checks passed or skipped reason stated.
- Status contains only expected files.
- Git action succeeded before reporting it.
