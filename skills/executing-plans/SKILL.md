---
name: executing-plans
description: Use when executing a written implementation plan or multi-step repo change in the current Codex session.
---

# Executing Plans

## Goal
Execute planned work with minimal chatter, scoped edits, and fresh verification.

## Use When
- A plan file already exists.
- User asks you to implement a multi-step change.
- Code changes should proceed without more design discussion.

## Do
- Read the plan and the smallest relevant files.
- Check `git status --short` before edits.
- Use `update_plan` for visible task tracking.
- Use `rg` for search and `apply_patch` for manual edits.
- Run focused verification while iterating.
- Run required repo-level verification before final success claims.
- Leave unrelated dirty/untracked files alone.

## Do Not
- Re-plan unless the plan is impossible, unsafe, or conflicts with higher-priority instructions.
- Add unplanned features or broad refactors.
- Spawn subagents unless user asked or tasks are clearly independent and multi-agent tools are available.
- Paste full passing command output.
- Say done before verification passes or limits are stated.

## Workflow
1. Read plan, relevant files, and git status.
2. Make a short progress checklist.
3. For each task: mark in progress, implement minimal change, verify, mark complete.
4. If verification fails, read output, fix the root cause, re-run.
5. Final: report changed files, verification, and unresolved risk.

## Status
Only message user on start, blocker, verification failure, major task completion, and final. One sentence each.

## Verify
- Focused checks from plan.
- Project-required checks from `AGENTS.md`.
- Browser check for UI when practical.
