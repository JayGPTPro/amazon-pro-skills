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

## Editorial cleanup. May 2026, 80 → 71
- A full audit of all 80 skills identified 8 merge candidates with high overlap
  and 1 cut candidate.
- Cut: amz-listing-versioning-tracker. Manage Your Experiments now covers this
  natively. low standalone value.
- Merges (kept the richer name, absorbed the second as a subsection):
  - niche-finder → product-research (single-product vs niche-level tests under
    one skill)
  - search-optimization → listing-optimization (ranking diagnosis is part of
    the same workflow)
  - voice-search-listing → ai-search-optimization (Rufus and Alexa+ share the
    COSMO layer)
  - enhanced-brand-content → a-plus-content (Premium A+ is the same model
    with extra modules)
  - shipping-calculator → fba-calculator (same fee stack)
  - vine-program → review-strategy (Vine is one source inside the strategy)
  - restock-forecaster → inventory-management (same reorder equation)
  - dayparting-strategy → ppc-campaign (advanced appendix, gated on data
    threshold)
- 11 surviving skills got targeted improvements (brand-registry post-enrollment
  plan, customer-question-mining Rufus citation patterns, coupon-strategy
  2026 fee tier, etc).
- Net result: 71 skills, each carrying its own decision. no two skills produce
  the same artifact from the same inputs.

## Editorial cleanup round 2. May 2026, 71 → 64
After a 1-to-71 ranking exercise, the bottom 7 were cut. The criterion was
"sub-audience size + immediacy of action." Each cut skill is fine on its own,
but addresses a sub-segment too narrow for the library's positioning as a
universal seller toolkit.

Cut (7):
- amz-3pl-vs-fba-decision. Narrow segment (oversize, slow, large operations)
- amz-repricing-strategy. Mostly reseller use case, not PL-first
- amz-seller-analytics. Competitive intel, doesn't drive immediate action
- amz-dsp-readiness-audit. Audience too small (large brands only)
- amz-global-selling. Few sellers expand internationally
- amz-international-listings. Even smaller sub-audience
- amz-exit-valuation-prep. One moment in a brand's life

Result: The Expansion category is gone. Strategic and lifecycle has one skill.

## Round 3 additions. May 2026, 64 → 74
After cleanup the library was at 64. A community-research pass (Reddit
r/FulfillmentByAmazon, GitHub awesome-claude-skills lists, Amazon seller
blogs, 2026 policy updates) surfaced 15 strong candidates. Top 10 built.

The selection criterion was "loved skill patterns": decision triggers with
hard numbers, bulk-file outputs you literally upload to Seller Central,
high-urgency moments (suspension, Q4, stockout, tax season), and skills
tied to specific 2026 policy changes (Returns Processing Fee, AI image
disclosure, manufacturing-cost reimbursement basis).

The 10 added:
- amz-cogs-tax-pack
- amz-vine-roi-decision
- amz-ip-complaint-retraction-kit
- amz-search-term-report-miner
- amz-q4-restock-war-room
- amz-ai-image-policy-compliance
- amz-listing-indexation-audit
- amz-supplier-sample-evaluation
- amz-stockout-recovery-plan
- amz-returns-root-cause-loop

Library now 74. Categories: Operations & account (9), Promotion & growth (8),
Listing & content (8), Account health & compliance defense (8), Research (6),
AI search (5), Advertising (5), Reviews (5), Financial recovery (6),
Logistics advanced (5), Pricing (4), Ads advanced (4), Strategic (1).
