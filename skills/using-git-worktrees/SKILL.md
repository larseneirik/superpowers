---
name: using-git-worktrees
description: Use when feature work needs an isolated git worktree or when a plan should not run in the current dirty workspace.
---

# Using Git Worktrees

## Goal
Create isolation only when it reduces branch or dirty-workspace risk.

## Use When
- Current workspace has unrelated dirty changes.
- Work is large, risky, or branch-specific.
- User asks for a worktree.
- Plan requires isolation from current branch.

## Do
- Check `git status --short` and current branch first.
- Prefer existing project convention: `.worktrees/`, `worktrees/`, then user/project config.
- Use `codex/` branch prefix unless user asks otherwise.
- Verify project-local worktree dirs are ignored before creating.
- Install dependencies only when needed for verification.
- Run a cheap baseline check when practical.
- Report absolute worktree path.

## Do Not
- Create a worktree for tiny edits in a clean workspace.
- Auto-commit `.gitignore` or setup changes without user intent.
- Delete worktrees or branches without explicit confirmation.
- Proceed if baseline failure makes new failures indistinguishable without noting it.

## Workflow
1. Inspect branch and status.
2. Decide whether isolation is needed.
3. Pick worktree directory by existing convention.
4. If project-local dir is not ignored, patch ignore rules only if appropriate and report it.
5. Create branch/worktree.
6. Run minimal setup/baseline verification.

## Status
One line when creating, one line when ready or blocked.

## Verify
- Worktree path exists.
- Branch name is correct.
- Ignore rule prevents nested worktree tracking.
- Baseline result is known.
