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

## Quality pass, merge, and curation round. June 2026, 74 to 67
A 6-agent audit scored all 74 skills against the amz-buy-box bar, then an 8-agent
fix pass applied the findings. The library was already strong (most skills passed).
the round targeted three things: 2026 factual accuracy, framework naming, and
duplicate consolidation.

Merges (74 to 72):
- amz-returns-root-cause-loop into amz-return-reduction. Both clustered returns into
  the same five root causes. The survivor absorbed the Returns Processing Fee
  financial angle and got a named model (the Returns Fault Tree).
- amz-ipi-recovery-plan into amz-inventory-management. The inventory skill already
  carried the IPI levers. it absorbed the one distinct asset (a 30-60-90 day phased
  recovery plan) and dropped the weaker skill's invented "mid-2025 tightening" claim.

Curation cut (72 to 67): to land on a clean "67 Free Skills for Amazon Sellers"
brand, the five weakest-by-standalone-value skills were cut. Same criterion as the
earlier cleanup rounds (audience size, immediacy, standalone value, overlap):
- amz-pricing-war-defense. mostly a router to four sibling skills. also clears the
  orphan one-skill Strategic category.
- amz-creator-connections-brief. the thinnest skill, niche influencer-campaign audience.
- amz-attribution-campaign-planner. narrow off-Amazon-traffic audience, paired with
  creator-connections.
- amz-aeo-external-content-plan. overlapped amz-ai-search-optimization on AI-citation
  strategy. off-Amazon content is a narrower play.
- amz-buyer-abuse-defense. overlapped amz-chargeback-defense on evidence packets.
  chargeback-defense is the more universal of the pair and was kept.
The core toolkit (research, listing, PPC, fees, reviews, inventory) is untouched.

2026 factual corrections, each verified against a primary source or hedged:
- Subscribe & Save: removed the retired "10% for 5-or-more items" auto-tier.
- Chargeback: A-to-z merchant response window made consistent at 3 calendar days.
- Reimbursement: corrected to reflect Amazon still auto-reimburses FC loss/damage.
  cost basis fixed to manufacturing cost excluding freight and duty (Mar 2025).
- Aged inventory: replaced the old 180/365-day LTSF model with the 181-day tiered
  Aged-Inventory Surcharge.
- Named the live 2024 fees where missing: Returns Processing Fee, Low-Inventory-Level
  Fee, Inbound Placement Service Fee.
- Coupon: corrected to the $5 + 2.5%-of-coupon-sales fee model (June 2025).
- Tariffs: made regime-agnostic and added the Section 321 / de minimis suspension.
- Dates: relativized hard-coded Prime Day and PBDD dates (they shift yearly. Prime
  Day 2026 landed in June, which is why fixed dates were wrong).
- AI image: removed fabricated rejection stats. the Delta-E tolerance is now framed
  as the skill's own QA heuristic, not an Amazon-published rule.
- Vine: fixed the ROI math so the conversion lift applies to incremental future
  sessions, not retroactively to all baseline traffic.

Framework naming: nine skills that carried a bare table or list got a memorable
named model (product-photography, negative-keywords, suspension-appeal, rank-tracker,
sales-estimator, subscribe-save, creator-connections-brief, inbound-placement-
optimizer, account-health-triage).

De-duplication without merge: ai-search-optimization and ppc-campaign now hand off to
the canonical deep-dive skills (attributes-completer, negative-keywords) instead of
reproducing their audits.

Principle held throughout: when an exact 2026 figure could not be confidently
verified, the skill hedges ("confirm in Seller Central") rather than stating a
number. a correct hedge beats a confident wrong number.
