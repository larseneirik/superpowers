---
name: dispatching-parallel-agents
description: Use when two or more independent investigations or tasks can run safely in parallel without shared files, state, or sequence dependencies.
---

# Dispatching Parallel Agents

## Goal
Use parallel agents only when independence saves time without increasing merge risk.

## Use When
- Multiple failures have different likely root causes.
- Tasks touch separate files or subsystems.
- Each task can be explained with self-contained context.
- Multi-agent tools are available in Codex.

## Do
- Group work by independent domain.
- Give each agent one narrow goal.
- Provide exact files, errors, constraints, and expected output.
- Require summary of root cause and changes.
- Wait for all agents, inspect diffs, resolve conflicts, then verify together.
- Close agent threads when done if the tool requires it.

## Do Not
- Parallelize tightly coupled work.
- Send broad prompts like “fix all tests”.
- Let agents edit the same files unless explicitly coordinated.
- Trust agent success without local verification.
- Use agents when a single local edit is faster.

## Prompt Shape
```text
Goal: [one task]
Files: [exact paths]
Context: [errors/relevant requirements]
Constraints: [do not touch X]
Return: root cause, changes, verification run
```

## Workflow
1. Confirm independence.
2. Write one focused prompt per domain.
3. Dispatch agents in parallel.
4. Review summaries and diffs.
5. Run integrated verification.

## Status
One line when dispatching, one line if blocked, one final integration result.

## Verify
- No conflicting edits.
- Each domain’s focused check passes.
- Full relevant suite passes after integration.
