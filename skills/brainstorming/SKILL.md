---
name: brainstorming
description: Use when creative or ambiguous work has unclear requirements, scope, UX, or tradeoffs.
---

# Brainstorming

## Goal
Clarify intent and choose a small, workable design before implementation.

## Use When
- User asks to design, brainstorm, or explore options.
- Feature scope is ambiguous.
- UX/product tradeoffs matter.
- Multiple implementation approaches are plausible.

## Do
- Inspect the smallest relevant project context first.
- Ask only the questions needed to remove real risk.
- Prefer one concise question at a time.
- Offer 2-3 approaches only when the choice matters.
- Recommend one approach with concrete reason.
- Scale output: tiny change = short plan; large feature = written spec.
- Use text by default. Use visual/browser aids only when explicitly useful and allowed by project rules.

## Do Not
- Force a spec, commit, reviewer loop, or visual companion for simple work.
- Block obvious small changes on ceremony.
- Propose unrelated refactors.
- Expand scope beyond user goal.
- Ask questions whose answer can be discovered from files.

## Workflow
1. Read relevant files/docs.
2. Identify unknowns that affect correctness or user experience.
3. Ask minimal clarifying questions, or proceed with clear assumptions.
4. Present selected approach and key tradeoffs.
5. If implementation follows, create a short stepwise plan or use `writing-plans` when complexity warrants it.

## Status
Keep updates short. Use one line when gathering context, one line when ready with approach.

## Verify
Before leaving brainstorming:
- Scope is explicit.
- Chosen approach fits repo patterns.
- Open assumptions are named.
- Next step is plan or implementation, not more discussion by default.
