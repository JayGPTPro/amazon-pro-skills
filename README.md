# Amazon Pro Skills

64 production-grade Claude Code skills for serious Amazon sellers. Free and open.
Built by Jay Margaliot.

Every skill is a real framework, not a thin wrapper. Each one carries a named model,
a step-by-step process with decision logic, an output template, a worked example, a
self-check, and a list of the mistakes to avoid. Each works standalone. no MCP, no
API keys, no external tools. You bring your own data, the skill does the thinking.

## Install all 64 skills in one line

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

## The 64 skills

**Research and selection** (6)
amz-product-research, amz-trending-products, amz-sales-estimator,
amz-competitor-analysis, amz-private-label, amz-wholesale-sourcing

**Listing and content** (7)
amz-listing-optimization, amz-keyword-research, amz-backend-keywords,
amz-a-plus-content, amz-listing-images, amz-product-photography, amz-variation-strategy

**AI search and modern SEO** (4)
amz-ai-search-optimization, amz-attributes-completer, amz-aeo-external-content-plan,
amz-customer-question-mining

**Advertising** (4)
amz-advertising-strategy, amz-ppc-campaign, amz-negative-keywords, amz-display-ads

**Advertising and growth (advanced)** (4)
amz-tacos-diagnostic, amz-attribution-campaign-planner, amz-creator-connections-brief,
amz-sponsored-brands-video

**Pricing and profit** (4)
amz-fba-calculator, amz-profit-analyzer, amz-tariff-calculator, amz-buy-box

**Financial recovery and reconciliation** (5)
amz-reimbursement-audit, amz-cash-flow-forecaster-dd7, amz-chargeback-defense,
amz-fee-audit, amz-1099k-reconciliation

**Promotion and growth** (7)
amz-coupon-strategy, amz-deal-finder, amz-brand-tailored-promotions,
amz-subscribe-save, amz-product-bundling, amz-seasonal-planning, amz-launch-runway

**Reviews and analytics** (4)
amz-review-analyzer, amz-review-strategy, amz-brand-analytics, amz-rank-tracker

**Operations and account** (8)
amz-inventory-management, amz-fba-prep, amz-return-reduction,
amz-brand-registry, amz-category-ungating, amz-product-compliance,
amz-suspension-appeal, amz-storefront-design

**Account health and compliance defense** (6)
amz-account-health-triage, amz-ipi-recovery-plan, amz-hijacker-removal,
amz-listing-suppression-recovery, amz-category-renoding-fix, amz-buyer-abuse-defense

**Inventory, logistics, sourcing (advanced)** (4)
amz-removal-vs-storage-calculator, amz-inbound-placement-optimizer,
amz-sourcing-diversification, amz-supplier-negotiation-script

**Strategic and lifecycle** (1)
amz-pricing-war-defense

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
