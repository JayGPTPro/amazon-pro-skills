---
name: amz-vine-roi-decision
description: >-
  Calculates whether Amazon Vine enrollment is net-positive for a given SKU before
  the seller commits the enrollment fee plus units on a Tier 3 enrollment. Uses
  category-specific CVR lift benchmarks and a hard cap rule to catch the enrollments
  that quietly lose money. Use when a user asks about Vine math, Vine
  ROI, or which tier to pick. Trigger phrases: "Vine ROI", "is Vine worth it",
  "Vine math", "Vine Tier 0 1 3 decision". Works with zero tools.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Vine ROI Decision

Sellers default to Tier 3 (up to 30 reviews) on every new SKU because it sounds like
"the most reviews fastest". The cash adds up. The Tier 3 enrollment fee plus 30 units at
landed cost. For a $14 supplement with $4 margin, the fee plus the give-away units run
several hundred dollars to get reviews. The fee itself is charged about seven days after
the first Vine review posts, and if no review ever posts you are not charged the fee
(you still eat the units shipped). The payback only comes from the extra conversion
those reviews earn on future traffic, so if the lift is too small to cover the outlay,
the SKU is net-negative. A meaningful share of enrollments fail this test. This skill
catches them before the spend.

## When to use this

- Launching a new ASIN and deciding Tier 0, 1, or 3
- 90 days post-launch, asking if Vine is worth a second enrollment on a variation
- Comparing Vine vs paid Rebates vs PPC review velocity
- A new brand with 18 SKUs and a fixed Vine budget

## The framework. The Vine ROI Calc

The gain is incremental. Reviews lift conversion only on the sessions that happen after
the reviews land, and only by the lift itself (the extra CVR points), not by recrediting
your whole existing conversion rate. So apply the lift to forward sessions at the margin:

```
Incremental gain = (CVR lift in points x Forward sessions over the window x AOV x Margin per order)
Vine net = Incremental gain minus (Vine fee + N units x landed cost)
```

Where:
- CVR lift in points = the percentage-point increase, not a new total CVR applied to baseline
- Forward sessions = sessions expected after reviews post, over the measurement window
- N = 2 for Tier 0, 10 for Tier 1, 30 for Tier 3 (units given away)
- Vine fee = $0 for Tier 0, $75 for Tier 1, $200 for Tier 3, per parent ASIN. confirm current Vine fees in Seller Central, the tiers shown in your account can vary
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

2. **Project forward sessions.** Sessions per day x the days in the window that fall
   after reviews post (reviews drip over 30 to 60 days, so the early window earns no
   lift). Call this Forward Sessions.

3. **Apply lift in points to each tier.** Use the category benchmark midpoint as a
   percentage-point increase. Incremental gain = lift in points x Forward Sessions x
   AOV x margin %. Do this for Tier 0, Tier 1, Tier 3. This is the gain on top of
   baseline, never a recredit of baseline conversion.

4. **Subtract enrollment cost.** Tier cost = Vine fee + (N x landed cost). Net gain =
   Incremental gain minus Tier cost.

5. **Apply the hard cap.** Per-review cost / projected gross profit over the window. If
   > 15% on the best tier, skip Vine entirely.

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

**Forward sessions over the window**: [X]

**Tier comparison**
| Tier | CVR lift (pts) | Incremental gain | Cost | Net gain | Per-review cost % |
| 0    | [pts]          | $[X]             | $[Y] | $[Z]     | [%]               |
| 1    | [pts]          | $[X]             | $[Y] | $[Z]     | [%]               |
| 3    | [pts]          | $[X]             | $[Y] | $[Z]     | [%]               |

**Verdict**: [GO Tier X | CAUTION Tier X | SKIP]
**Reasoning**: [1-2 sentences]
```

## Worked example

ASIN: collagen peptides, $26 price, $9 margin, $7 landed cost. Category:
Supplements. Sessions/day = 85. Current CVR = 11%. AOV = $26.

The gain is incremental, on forward traffic only. Reviews are not live day one, so over a
90-day window count roughly 60 days of post-review sessions: forward sessions = 85 x 60 =
5,100. The lift is in CVR points, not a recredit of the existing 11%.

Tier 3: benchmark midpoint as a lift of about 1.5 CVR points. Incremental orders =
0.015 x 5,100 forward sessions = ~76.5 extra orders. Incremental gain = 76.5 x $9 margin
= $689. Cost = $200 + (30 x $7) = $410. Net gain = $689 minus $410 = $279. Per-review
cost = $410 / projected window gross profit. Clears cap.

Tier 1: benchmark midpoint as a lift of about 1.0 CVR point. Incremental orders = 0.010 x
5,100 = ~51 extra orders. Incremental gain = 51 x $9 margin = $459. Cost = $75 + (10 x $7)
= $145. Net gain = $459 minus $145 = $314. Per-review cost is lower still.

Verdict: GO Tier 1. Higher net gain than Tier 3 with a third of the cash outlay, because
the marginal 20 units cost more than the marginal lift returns. Note the gain is the
extra orders only, never the whole baseline re-credited at a higher rate.

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
