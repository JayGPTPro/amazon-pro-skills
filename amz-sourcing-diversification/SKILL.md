---
name: amz-sourcing-diversification
description: >-
  Plan supplier diversification away from China-only sourcing into Vietnam,
  India, Mexico, or domestic light-assembly. Compares HS-code duty rates, lead
  times, MOQ, and tariff exposure across alternative origins. Use when a user
  asks about diversifying suppliers, moving sourcing out of China, alternative
  manufacturing countries, tariff exposure, or de-risking supply chain. Trigger
  phrases: "diversify suppliers", "out of China", "Vietnam supplier", "India
  supplier", "Mexico", "tariff exposure", "supply chain risk". Works with zero
  tools.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Sourcing Diversification

Tariff volatility, geopolitical risk, and trade-policy whiplash made China-only
sourcing a liability for many Amazon sellers. Diversification is not just moving
factories. It is matching the product, the cost structure, and the lead-time
profile to alternative origins. This skill builds the migration plan.

## When to use this

- Heavy or full China exposure and tariff-policy risk is real.
- Stacked duties (Section 301, reciprocal or other country-specific tariffs,
  antidumping where relevant) are eroding margin.
- The seller wants a backup supplier without a full move.
- Planning a new SKU and deciding where to source from the start.

## The framework. The Diversification Map

For each candidate origin (Vietnam, India, Mexico, domestic assembly, etc.), score
on five factors.

| Factor | What to check |
|--------|---------------|
| Duty + tariff | HS code base rate plus all applicable add-on duties for that origin (Section 301, reciprocal or other country-specific tariffs, antidumping where relevant). Check the current rate, the regime shifts |
| Unit cost | Factory price for comparable quality |
| Lead time | Production + ocean/air freight + customs |
| MOQ | Often higher in alternative origins still ramping |
| Quality and reliability | Sample tested, references, IP protection |

A clear winner per factor is rare. the diversification is usually about reducing
risk while accepting a higher unit cost or longer lead time.

## Step by step

1. **Collect inputs.** Current China supplier details (price, MOQ, lead time, HS
   code, total tariff), the product, current monthly volume, the seller's risk
   tolerance.

2. **Compute current total landed cost.** With current tariffs (use
   amz-tariff-calculator). This is the baseline.

3. **Identify 2-3 candidate alternative origins.** Vietnam (apparel, accessories,
   electronics assembly), India (textiles, leather, certain home goods), Mexico
   (USMCA benefits for some categories), domestic assembly (specialty, low-volume).

4. **Source quotes.** Contact suppliers or use industry directories.

5. **Compute landed cost per origin.** Through amz-tariff-calculator. Compare to
   the China baseline.

6. **Build the migration roadmap.** Start with samples and a small parallel
   production run before any volume shift. Most sellers diversify gradually,
   keeping China for some SKUs while shifting others.

7. **Plan the dual-source state.** Many sellers settle on a 70/30 or 50/50 split
   for resilience, not a full move.

8. **Run the quality check**, then deliver.

## Output format

```
## Sourcing Diversification Plan. [product]

Current origin: China. Total landed cost: [$/unit]
Current tariff exposure: [%]

### Candidate origins
1. [country] . duty + tariff [%] . landed cost [$/unit] . lead time [d] . MOQ [N] . notes
...

### Recommended path
[primary candidate, why]

### Migration roadmap
Phase 1 (weeks 1-6): Samples + small parallel run
Phase 2 (weeks 7-16): Production at the new origin
Phase 3 (weeks 17+): Dual-source split [%] / [%]

### Risk reduction
[which trade-policy risks the diversification removes]
```

## Worked example

A home-goods SKU sourced from China at 4.20 USD landed, where the stacked
China-origin duties (base duty plus the add-on tariffs that apply to this HS
code and origin) add most of the gap from the 2.80 factory price. Vietnam
alternative: factory price 3.20, a different and currently lower duty stack for
this origin, landed 4.40. Cost slightly higher but the China-specific tariff
exposure is removed. Migration: order 200 units sample from a vetted Vietnam
supplier (6 weeks), test quality and lead-time reliability. If clean, place a
5,000 unit parallel order while continuing China for the bulk. After 3 months,
split production 40 Vietnam / 60 China for resilience. The seller is now
insulated from a tariff hike on the China-origin duty stack for this SKU, at a
small landed-cost premium that is manageable. Verify the current duty stack for
each origin before committing. the rates shift.

## Quality check

- Current landed cost is computed before any comparison.
- 2-3 candidate origins are scored on all five factors, not just price.
- The plan starts with samples and parallel runs, not a full switch.
- A dual-source split is recommended for resilience, not a binary move.
- Trade-policy risks are explicitly named, not vague "geopolitical risk".

## Common mistakes

- **Cost-only comparison.** Vietnam may be slightly more expensive but eliminates
  tariff exposure. that risk reduction is real value.
- **All-or-nothing move.** Full migration before testing the new supplier produces
  quality and lead-time surprises.
- **Forgetting MOQ and lead time.** Alternative origins often have higher MOQs and
  longer lead times during ramp-up.
- **No backup plan.** Single-source from any country, including the new one, is
  itself a risk.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
