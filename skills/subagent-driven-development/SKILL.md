---
name: subagent-driven-development
description: Use when executing a written plan with independent tasks that benefit from isolated Codex agents in the same session.
---

# Subagent-Driven Development

## Goal
Coordinate isolated agents for independent plan tasks while keeping integration controlled.

## Use When
- A written plan exists.
- Tasks are mostly independent.
- Multi-agent tools are available.
- Isolation or parallel review is worth the extra tokens.

## Do
- Read the plan once and extract task text.
- Dispatch one implementer per independent task or batch.
- Provide full task context; do not rely on session history.
- Scale review depth to risk: self-review for small tasks, reviewer agent for high-risk or broad changes.
- Inspect each diff before marking task complete.
- Run integrated verification after all agent work.

## Do Not
- Use subagents for tiny local edits.
- Dispatch agents on shared files without coordination.
- Let agents commit, push, or clean up branches unless explicitly requested.
- Move forward with unresolved reviewer issues.
- Trust “done” reports without diff and test verification.

## Workflow
1. Confirm plan and task independence.
2. Create a short controller checklist.
3. For each task/batch: dispatch focused agent with files, constraints, verification.
4. Review result, diff, and checks.
5. Fix or re-dispatch only with new context.
6. Run final verification and finish via repo workflow.

## Status
One line when dispatching agents, one line for blockers, one line after integrated verification.

## Verify
- Agent diff matches task.
- No conflicting edits.
- Focused task checks pass.
- Final repo checks pass before completion.
