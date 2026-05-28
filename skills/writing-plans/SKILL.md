---
name: writing-plans
description: Use when turning approved requirements into an implementation plan before code, especially for Codex, TDD, UI, or multi-step repo work.
---

# Writing Plans

## Goal
Create a plan another Codex agent can execute without guessing or over-building.

## Use When
- User asks for a plan.
- `AGENTS.md` requires a stepwise plan.
- Change touches multiple files, behavior, data flow, or deployment.
- Requirements are approved but implementation has not started.

## Do
- Ground every task in files you inspected.
- Keep scope to requested behavior, required plumbing, and proof.
- Name exact files to create/modify/test.
- Use imperative, concrete task steps.
- Include exact commands and expected results.
- Add browser verification for UI when practical.
- Follow repo/user commit rules.

## Do Not
- Plan future-ready abstractions, optional modes, or unused dependencies.
- Plan data/state/API behavior that does not exist.
- Add shadcn components if existing primitives fit.
- Write long architecture theory.
- Commit after every small step unless explicitly required.

## Plan Shape
```md
# [Feature] Implementation Plan

Goal: [one sentence]
Files:
- Create: `path` - reason
- Modify: `path` - reason
- Test: `path` - reason

Tasks:
1. [Small outcome]
   - Do: [exact change]
   - Verify: `[command]`
   - Expected: [pass/fail reason]
```

## Workflow
1. Inspect smallest relevant repo context.
2. Reduce scope.
3. Write file map.
4. Write small ordered tasks.
5. Add verification per task and final repo checks.
6. Save only if user/project expects a plan file.

## Status
One line when starting and one line when saved/ready. No progress essays.

## Verify
Before handing off, self-check:
- No uninspected file claims.
- No speculative features.
- Each task has proof.
- Commands match this repo.
