---
name: using-superpowers
description: Use when starting a session or deciding whether a named or clearly relevant superpowers skill should be loaded.
---

# Using Superpowers

## Goal
Load only the skills that materially improve the current Codex task.

## Priority
User instructions, `AGENTS.md`, and platform/developer instructions override this skill. When a skill conflicts with higher-priority instructions, follow the higher-priority instruction and note the conflict only if it affects the work.

## Use When
- Session starts and a superpowers skill may apply.
- User names a superpowers skill.
- Task clearly matches a skill description.
- You need to choose between process skills.

## Do
- Read the smallest relevant skill body before relying on it.
- Use direct or clear trigger matches, not "1% chance" guesses.
- Prefer one process skill that controls the workflow.
- Use native Codex tools: `update_plan` for progress, shell/apply_patch for local work, multi-agent tools only when available and useful.
- Keep skill status notes to one short line when the user benefits from knowing the workflow.

## Do Not
- Load skills for simple answers that do not match a trigger.
- Chain multiple workflow skills unless each is needed.
- Follow legacy tool names from old runtimes.
- Let skill ceremony block small, obvious work.

## Workflow
1. Check user request and `AGENTS.md` for explicit skill/tool rules.
2. Match only named skills or strong trigger matches.
3. Read matched skill content.
4. Apply the leanest workflow that satisfies the task.
5. If no skill fits, proceed normally.

## Status
Use one sentence: `Using <skill> for <purpose>.` Skip this for trivial work.
