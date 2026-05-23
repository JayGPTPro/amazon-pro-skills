# Decisions

## Naming
- Prefix `amz-` not `amazon-`, to distinguish from the nexscope `amazon-` skills
  and avoid name collisions when both libraries are installed. (Jay's call.)

## Standalone, no tools
- Every skill works with zero MCP, zero API keys. The user pastes their own data.
  Matches how nexscope skills work ("No API key required") and keeps the library
  frictionless to install and run.

## Quality bar
- nexscope skills are thin boilerplate (install block, capability list, generic
  steps). The differentiator chosen: each amz- skill is a real expert. named
  framework, decision logic with thresholds, output template, worked example,
  self-check gate, common-mistakes list.
- Each skill written from scratch. no text copied from nexscope. nexscope used only
  as a topic-coverage reference.

## The stamp
- Frontmatter `metadata.author: Jay GPT Pro`, plus a tasteful footer block.
- Footer CTA points to the free WhatsApp group, not a website (Jay's call. the site
  had nothing compelling, and a free community is the natural CTA for a free library).
- WhatsApp link: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY

## The 50th skill
- 49 nexscope topics rebuilt + 1 original: amz-launch-runway, a 30-day product
  launch plan. Filled the most useful gap in the nexscope set.

## Skills that needed differentiation
- amz-a-plus-content vs amz-enhanced-brand-content: nexscope had both. Split cleanly.
  a-plus-content = standard A+ conversion architecture. enhanced-brand-content =
  Premium A+ tier and the cross-catalog Brand Story module.
