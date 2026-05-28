---
name: writing-skills
description: Use when creating, editing, compressing, or verifying Codex skills and their SKILL.md files.
---

# Writing Skills

## Goal
Create Codex skills that trigger accurately, load fast, and guide action without ceremony.

## Use When
- Creating a new skill.
- Editing an existing `SKILL.md`.
- Compressing a verbose skill.
- Auditing skill triggers, clarity, or token cost.

## Do
- Make frontmatter trigger-only: `description: Use when ...`.
- Keep `description` about when to load, not workflow.
- Put high-value instructions in the first 200 words.
- Use Codex-native terms and tools.
- Keep the main skill short; move heavy examples, APIs, scripts, or research to separate files.
- Prefer imperative bullets over essays.
- Add status rules that minimize user-facing chatter.
- Verify word count and trigger clarity after edits.

## Do Not
- Include narratives about one past session.
- Force-load references with inline paths unless required.
- Repeat content from related skills.
- Add flowcharts for linear steps.
- Add moral language, persuasion essays, or multiple examples of the same point.
- Preserve old runtime tool names in main guidance.

## Target Structure
```md
---
name: skill-name
description: Use when [specific trigger]
---

# Skill Name
## Goal
## Use When
## Do
## Do Not
## Workflow
## Status
## Verify
```

## Word Budgets
- Frequently loaded/core skills: 150-250 words.
- Normal workflow skills: 250-400 words.
- Complex reference skills: main file under 500 words; details in `references/` or scripts.

## Workflow
1. Identify trigger and main failure the skill prevents.
2. Remove nonessential explanation.
3. Rewrite as goal, triggers, do/do-not, workflow, status, verify.
4. Move long examples/reference material out of `SKILL.md`.
5. Run checks below.

## Verify
```bash
wc -w path/to/SKILL.md
rg "old runtime|visual companion|long example|status essay" path/to/SKILL.md
```

Pass criteria:
- Description starts with `Use when`.
- Description contains trigger, not workflow.
- Main file meets word budget or has a stated reason.
- No old runtime tool names unless explicitly documenting a compatibility mapping.
- Status guidance is short and specific.
