---
name: verification-before-completion
description: Use when about to claim work is complete, fixed, passing, committed, pushed, or ready for review.
---

# Verification Before Completion

## Goal
Make success claims only after current evidence supports them.

## Use When
- You are about to say work is done or fixed.
- You are about to commit, push, open a PR, or move to the next task.
- A test/build/lint/browser result matters to the claim.

## Do
- Identify the exact proof required.
- Run the command or check fresh in this turn.
- Read exit code and relevant output.
- Report actual status, including failures or skipped checks.
- For UI work, verify in browser when practical.
- For delegated work, inspect diff and verify independently.

## Do Not
- Rely on previous runs, assumptions, or agent reports.
- Treat lint as proof that build/tests pass.
- Claim “done”, “fixed”, “passing”, or “ready” before verification.
- Hide skipped or blocked verification.

## Workflow
1. Claim planned: name the proof needed.
2. Run proof: command, browser check, diff review, or checklist.
3. Read result.
4. If pass: state claim with command/check.
5. If fail/blocked: state actual result and next action.

## Status
Use one concise line for failed or blocked verification. Passing details belong in final unless user needs progress.

## Verify
Evidence must match the claim:
- Tests pass: test command exit 0.
- Build succeeds: build command exit 0.
- Bug fixed: original symptom no longer reproduces.
- Requirements met: checklist against request/plan.
