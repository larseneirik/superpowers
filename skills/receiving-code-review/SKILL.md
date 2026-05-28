---
name: receiving-code-review
description: Use when receiving code review feedback that must be evaluated, implemented, clarified, or pushed back on.
---

# Receiving Code Review

## Goal
Handle review feedback with technical accuracy, not automatic agreement.

## Use When
- User or reviewer gives review comments.
- Feedback is unclear, broad, or possibly wrong.
- Multiple review items must be implemented safely.
- GitHub inline comments need replies.

## Do
- Read all feedback before editing.
- Restate or infer the technical requirement.
- Verify each item against the codebase.
- Clarify blocking ambiguity before implementing.
- Implement in risk order: breaking/security, simple fixes, complex changes.
- Test each meaningful fix.
- Push back when feedback conflicts with code, tests, or user decisions.
- Reply to GitHub inline comments in their threads.

## Do Not
- Use performative agreement.
- Implement unclear items.
- Batch unrelated fixes without verification.
- Add “proper” features that are unused or out of scope.
- Ignore valid critical or important feedback.

## Workflow
1. List feedback items.
2. Mark each: clear, unclear, questionable, or accepted.
3. Investigate unclear/questionable items.
4. Fix accepted items in safe order.
5. Run focused and required checks.
6. Report what changed and what remains.

## Status
Short only: investigating feedback, blocked on ambiguity, fixed and verified.

## Verify
- Each accepted item has code/diff evidence.
- Relevant tests/checks pass.
- Any pushback cites code, tests, or project constraints.
