---
name: systematic-debugging
description: Use when a bug, failing command, test failure, build failure, performance issue, or unexpected behavior needs investigation before fixing.
---

# Systematic Debugging

## Goal
Find the root cause before changing code.

## Use When
- Tests, build, lint, CI, or runtime fail.
- Behavior differs from expected.
- A previous fix did not work.
- Multiple components may be involved.
- You are tempted to guess.

## Do
- Read the exact error and relevant output.
- Reproduce the issue or state why it cannot be reproduced.
- Check recent diffs and relevant config.
- Compare broken code with nearby working patterns.
- Form one hypothesis at a time.
- Make the smallest change that tests or fixes that hypothesis.
- Add a regression test when behavior changed or a bug can recur.

## Do Not
- Apply multiple fixes at once.
- Fix symptoms without tracing where they originate.
- Ignore failing output because the cause seems obvious.
- Keep trying after repeated failed fixes without re-evaluating the hypothesis.
- Add broad refactors while debugging.

## Workflow
1. Gather: error, reproduction, recent changes.
2. Localize: boundary, file, component, or data flow where it breaks.
3. Compare: working pattern vs broken pattern.
4. Hypothesize: `X causes Y because Z`.
5. Test/fix minimally.
6. Verify original symptom and regressions.

## Escalate
After three failed fix attempts, stop and question architecture, assumptions, or missing evidence before another fix.

## Status
Short updates only: reproduced, root cause found, blocked, verification failed, fixed.

## Verify
- Original failure no longer reproduces.
- Focused relevant checks pass.
- Regression test exists when practical and valuable.
