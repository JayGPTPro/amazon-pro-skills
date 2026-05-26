---
name: amz-vine-roi-decision
description: >-
  Calculates whether Amazon Vine enrollment is net-positive for a given SKU before
  the seller burns $620 all-in on a Tier 3 enrollment. Uses category-specific CVR
  lift benchmarks and a hard cap rule. About 15% of Vine enrollments are
  net-negative, this catches them. Use when a user asks about Vine math, Vine
  ROI, or which tier to pick. Trigger phrases: "Vine ROI", "is Vine worth it",
  "Vine math", "Vine Tier 0 1 3 decision". Works with zero tools.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Vine ROI Decision

Sellers default to Tier 3 (30 reviews) on every new SKU because it sounds like
"the most reviews fastest". The math is brutal. $200 Vine fee + 30 units at
landed cost. For a $14 supplement with $4 margin, that is $620 all-in to get
30 reviews. If those reviews lift CVR by less than 4% over 90 days, the SKU
is net-negative. About 15% of enrollments fail this test. This skill catches
them before the credit card hits.

## When to use this

- Launching a new ASIN and deciding Tier 0, 1, or 3
- 90 days post-launch, asking if Vine is worth a second enrollment on a variation
- Comparing Vine vs paid Rebates vs PPC review velocity
- A new brand with 18 SKUs and a fixed Vine budget

## The framework. The Vine ROI Calc

```
Vine ROI = (Expected CVR lift x Sessions x AOV x Margin x 90 days)
          minus (Vine fee + N units x landed cost)
```

Where:
- N = 2 for Tier 0, 10 for Tier 1, 30 for Tier 3
- Vine fee = $0 for Tier 0, $75 for Tier 1, $200 for Tier 3
- Expected CVR lift comes from category benchmarks below

### Category CVR lift benchmarks (90-day window, post-Vine)

| Category | Tier 0 (2) | Tier 1 (10) | Tier 3 (30) |
|---|---|---|---|
| Electronics | 2-4% | 5-9% | 8-15% |
| Home & Kitchen | 1-3% | 3-6% | 4-9% |
| Supplements & Beauty | 2-5% | 4-8% | 6-12% |
| Apparel | 1-2% | 2-5% | 3-7% |
| Toys & Games | 2-4% | 4-7% | 6-11% |
| Tools & Auto | 1-3% | 3-5% | 4-8% |

### The hard cap rule

If fully-loaded per-review cost > 15% of projected 90-day gross profit, SKIP.
The lift cannot mathematically pay it back.

## Step by step

1. **Pull the inputs.** Sessions per day (Business Reports), current CVR, AOV,
   margin per unit, landed cost per unit, category.

2. **Project 90-day baseline.** Sessions x 90 x current CVR x AOV x margin %.
   Call this Baseline Profit.

3. **Apply lift to each tier.** Use the category benchmark midpoint. Calculate
   Lifted Profit for Tier 0, Tier 1, Tier 3.

4. **Subtract enrollment cost.** Tier cost = Vine fee + (N x landed cost). Net
   gain = Lifted Profit. Baseline Profit. Tier cost.

5. **Apply the hard cap.** Per-review cost / 90-day gross profit. If > 15% on
   the best tier, skip Vine entirely.

6. **Pick the winning tier.** Highest net gain that clears the cap. Often Tier
   1 wins over Tier 3 because the marginal 20 units cost more than the marginal
   lift returns.

7. **Run the quality check**, then deliver verdict.

## Output format

```
## Vine Decision. [ASIN]

**Inputs**
- Sessions/day: [X] | Current CVR: [Y%] | AOV: $[Z] | Margin: $[M]/unit
- Landed cost: $[L]/unit | Category: [cat]

**90-day baseline profit**: $[X]

**Tier comparison**
| Tier | CVR lift | Lifted profit | Cost | Net gain | Per-review cost % |
| 0    | [%]      | $[X]          | $[Y] | $[Z]     | [%]               |
| 1    | [%]      | $[X]          | $[Y] | $[Z]     | [%]               |
| 3    | [%]      | $[X]          | $[Y] | $[Z]     | [%]               |

**Verdict**: [GO Tier X | CAUTION Tier X | SKIP]
**Reasoning**: [1-2 sentences]
```

## Worked example

ASIN: collagen peptides, $26 price, $9 margin, $7 landed cost. Category:
Supplements. Sessions/day = 85. Current CVR = 11%. AOV = $26. Baseline 90-day
profit = 85 x 90 x 0.11 x 9 = $7,573.

Tier 3: CVR lift 9% midpoint -> new CVR 12%. Lifted profit = 85 x 90 x 0.12 x 9
= $8,262. Cost = $200 + (30 x $7) = $410. Net gain = $8,262. $7,573. $410 = $279.
Per-review cost = $410 / $7,573 = 5.4%. Clears cap.

Tier 1: CVR lift 6% midpoint -> new CVR 11.66%. Lifted profit = $8,025. Cost =
$75 + (10 x $7) = $145. Net gain = $307. Per-review cost = 1.9%.

Verdict: GO Tier 1. Higher net gain than Tier 3 with 1/3 the cash outlay.

## Quality check

- Sessions pulled from Business Reports, last 30 days average
- Current CVR is unit session percentage, not order session
- Margin is fully loaded (Amazon fees, PPC ACoS, returns reserve)
- Category benchmark applied at midpoint, not optimistic top
- Hard cap rule enforced on per-review cost

## Common mistakes

- **Defaulting to Tier 3.** The marginal 20 units rarely return their cost. Tier 1 often wins.
- **Using list price instead of net AOV.** Coupons and promotions are not in list price.
- **Ignoring landed cost.** A $20 unit at $7 landed has very different math than a $20 unit at $1.50 landed.
- **Forgetting the 90-day window.** Vine reviews drip in over 30-60 days. Lift does not show up day 1.
- **Enrolling SKUs with zero traffic.** Vine reviews on a 5 sessions/day ASIN compound nothing. Fix traffic first.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
