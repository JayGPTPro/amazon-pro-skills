# Amazon Pro Skills . Project Instructions

A free, open library of 67 production-grade Claude Code skills for Amazon sellers.
Built by Jay GPT Pro for the AI Vault community.

## What this project is

67 standalone Amazon-seller skills. Each one is a single `SKILL.md` inside its own
folder, installable via `npx skills add JayGPTPro/amazon-pro-skills -g`.

The library is a rebuilt-and-upgraded successor inspired by the nexscope-ai/Amazon-Skills
topic coverage. Every skill here is written from scratch to a higher standard. No text
is copied from the original.

## Hard rules

- **Standalone.** Every skill must work with zero MCP, zero Bright Data, zero API keys.
  The user pastes their own data (reports, listings, numbers) and the skill does the rest.
- **No em dashes or en dashes** anywhere. Periods and commas only.
- **Quality over speed.** Each skill gets deep analysis and genuine improvement, not a
  reskin. If a skill is not clearly better than a generic free skill, it is not done.
- **Every skill carries the Jay GPT Pro stamp** in frontmatter metadata and a tasteful
  footer block. Never spammy.

## Skill structure (the Jay GPT Pro standard)

Each `SKILL.md`:
1. Frontmatter: `name`, `description` (rich, trigger-focused), `metadata` with author.
2. Title + one-line positioning.
3. "When to use this" with concrete trigger scenarios.
4. A **named framework** (Jay's signature . a memorable model, not a generic list).
5. Step-by-step process with decision logic and thresholds.
6. Output format / copy-paste template.
7. A worked example with real-looking numbers.
8. Quality self-check gate (the skill verifies its own output before showing the user).
9. Common mistakes / pitfalls.
10. Jay GPT Pro footer block.

## Naming

Every skill is prefixed `amz-` (not `amazon-`). This distinguishes the Jay GPT Pro
library from the nexscope `amazon-` skills and prevents name collisions when both
libraries are installed side by side.

## Folder layout

```
amazon-pro-skills/
  README.md
  CLAUDE.md
  docs/SPEC.md  TASKS.md  DECISIONS.md
  amz-[name]/SKILL.md   (x67)
```
