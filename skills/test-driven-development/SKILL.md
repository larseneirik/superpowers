---
name: test-driven-development
description: Use when implementing behavior changes, bug fixes, data logic, user interaction state, or regressions that need automated proof before code.
---

# Test-Driven Development

## Goal
Prove behavior with a failing test before writing production code.

## Use When
- Bug fix needs regression proof.
- Feature changes behavior or state.
- Data mapping, validation, caching, routing, forms, playback, or error handling changes.
- Existing coverage can be extended cheaply.

## Skip Or Scale Down When
- Copy/docs-only edits.
- CSS-only visual tweaks.
- Asset swaps verified by build/browser.
- Tiny JSX structure changes with no behavior change.
- User or repo verification standard says lighter proof is enough.

## Do
- Write one focused test for one behavior.
- Run it and confirm expected failure.
- Implement the smallest code that passes.
- Re-run focused test.
- Refactor only after green.
- Run broader checks when risk or repo rules require it.

## Do Not
- Write production behavior before the failing test.
- Treat a passing-new test as proof unless it failed for the right reason first.
- Add broad mocks when real code is practical.
- Refactor unrelated code during green.
- Force TDD onto non-behavior changes.

## Workflow
1. RED: add focused failing test.
2. Verify RED: failure is expected and meaningful.
3. GREEN: minimal implementation.
4. Verify GREEN: focused test passes.
5. REFACTOR: clean only what the change touched.
6. Final verification: project-required checks.

## Status
Only report RED, blocker, failed verification, or final result. One sentence.

## Verify
Completion requires:
- Test failed first for expected reason, when TDD applies.
- Focused test passes.
- Broader checks match repo/user risk standard.
