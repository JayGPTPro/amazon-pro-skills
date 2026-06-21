# Amazon Pro Skills

67 production-grade Claude Code skills for serious Amazon sellers. Free and open.
Built by Jay Margaliot.

Every skill is a real framework, not a thin wrapper. Each one carries a named model,
a step-by-step process with decision logic, an output template, a worked example, a
self-check, and a list of the mistakes to avoid. Each works standalone. no MCP, no
API keys, no external tools. You bring your own data, the skill does the thinking.

## Install all 67 skills in one line

```
npx skills add JayGPTPro/amazon-pro-skills -g
```

The skills install globally and become available in every Claude Code session.

## Verify installation

**macOS / Linux**
```
ls ~/.agents/skills/ | grep amz-
```

**Windows (PowerShell)**
```
Get-ChildItem "$env:USERPROFILE\.agents\skills" | Select-String amz-
```

## The 67 skills

**Research and selection** (6)
amz-product-research, amz-trending-products, amz-sales-estimator,
amz-competitor-analysis, amz-private-label, amz-wholesale-sourcing

**Listing and content** (8)
amz-listing-optimization, amz-keyword-research, amz-backend-keywords,
amz-a-plus-content, amz-listing-images, amz-product-photography, amz-variation-strategy,
amz-ai-image-policy-compliance

**AI search and modern SEO** (4)
amz-ai-search-optimization, amz-attributes-completer,
amz-customer-question-mining, amz-listing-indexation-audit

**Advertising** (5)
amz-advertising-strategy, amz-ppc-campaign, amz-negative-keywords, amz-display-ads,
amz-search-term-report-miner

**Advertising and growth (advanced)** (2)
amz-tacos-diagnostic, amz-sponsored-brands-video

**Pricing and profit** (4)
amz-fba-calculator, amz-profit-analyzer, amz-tariff-calculator, amz-buy-box

**Financial recovery and reconciliation** (6)
amz-reimbursement-audit, amz-cash-flow-forecaster-dd7, amz-chargeback-defense,
amz-fee-audit, amz-1099k-reconciliation, amz-cogs-tax-pack

**Promotion and growth** (8)
amz-coupon-strategy, amz-deal-finder, amz-brand-tailored-promotions,
amz-subscribe-save, amz-product-bundling, amz-seasonal-planning, amz-launch-runway,
amz-q4-restock-war-room

**Reviews and analytics** (5)
amz-review-analyzer, amz-review-strategy, amz-brand-analytics, amz-rank-tracker,
amz-vine-roi-decision

**Operations and account** (9)
amz-inventory-management, amz-fba-prep, amz-return-reduction,
amz-brand-registry, amz-category-ungating, amz-product-compliance,
amz-suspension-appeal, amz-storefront-design, amz-stockout-recovery-plan

**Account health and compliance defense** (5)
amz-account-health-triage, amz-hijacker-removal,
amz-listing-suppression-recovery, amz-category-renoding-fix,
amz-ip-complaint-retraction-kit

**Inventory, logistics, sourcing (advanced)** (5)
amz-removal-vs-storage-calculator, amz-inbound-placement-optimizer,
amz-sourcing-diversification, amz-supplier-negotiation-script,
amz-supplier-sample-evaluation

## How to use a skill

Just ask Claude Code naturally. The skill triggers on its own when the request
matches. For example:

> Audit my listing and rewrite the bullets, here is the current copy: [paste]

> Build me a PPC campaign structure for a new product at 29.99 with a 12 dollar margin

> Here is my search term report, find the negative keywords: [paste]

## License

MIT.

---

Built by Jay Margaliot. I share a new AI play for Amazon sellers every week, free,
in my WhatsApp group: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
