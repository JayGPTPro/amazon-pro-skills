---
name: amz-deal-finder
description: >-
  Decide which Amazon deal type to run, when, and whether it will pay off.
  Compares Lightning Deals, Best Deals, Prime-exclusive discounts, and coupons,
  checks the deal fee against the expected lift, and times the deal to an event.
  Use when a user asks about running a deal, Lightning Deals, Best Deals, Prime
  Day or event deals, deal fees, or whether a deal is worth it. Trigger phrases:
  "lightning deal", "best deal", "should I run a deal", "deal fee", "prime day
  deal", "deal strategy". Works with zero tools. the user provides price, cost,
  and goal.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Deal Finder

Amazon deals are a paid visibility event, not a discount. You pay a deal fee to be
placed on the Deals page during a window of concentrated traffic. A deal pays off
when the visibility lift outlasts the deal itself. This skill decides which deal,
when, and whether the math works.

## When to use this

- A seller is considering a Lightning Deal or Best Deal and is not sure it pays.
- Planning the deal calendar around Prime Day, Prime Big Deal Days, or Q4.
- A product needs a rank push and the seller is weighing deal versus coupon.
- A past deal felt expensive and the seller wants a go or no-go rule.

## The framework. The Deal Worth-It Test

A deal is worth running when three things are true. miss one and skip the deal.

1. **The product is deal-ready.** Solid rating (4.0-plus), enough reviews to convert
   a cold visitor, and stock to survive a spike. A deal that floods a weak listing
   with traffic just buys cheap proof that it does not convert.

2. **The math clears.** Deal price, minus referral fee, minus FBA fee, minus unit
   cost, minus the deal fee spread across expected units, is not deeply negative. A
   small loss can be acceptable as a rank investment. a large one is not.

3. **The timing concentrates traffic.** A deal during a major event reaches far more
   shoppers per dollar of deal fee than a deal on a random Tuesday.

## The deal types

| Type | Best for | Notes |
|------|----------|-------|
| Lightning Deal | A short, sharp spike and rank push | A few hours, a fixed fee, limited slots |
| Best Deal | Sustained visibility | Runs days to weeks, higher fee, broader reach |
| Prime-exclusive discount | Event windows, Prime members | Strong during Prime Day and Big Deal Days |
| Coupon | Always-on visibility badge | Lowest cost, see amz-coupon-strategy |
| Outlet | Clearing aged or overstocked inventory | Built for stock you need gone |

## Step by step

1. **Collect inputs.** Price, unit cost, fees, current rating and review count, stock
   on hand, the goal (rank push, event sales, clearance), and any target event date.

2. **Run the deal-ready check.** Rating, reviews, and stock. If the listing is not
   deal-ready, recommend fixing that first. a deal does not fix a weak listing.

3. **Pick the deal type** from the table, matched to the goal and timing.

4. **Run the math.** Per-unit contribution at the deal price, with the deal fee spread
   across a realistic unit estimate. State the number and whether a loss, if any, is
   an acceptable rank investment.

5. **Time it.** Anchor the deal to the highest-traffic window available. an event
   deal is worth far more than the same deal off-peak.

6. **Plan the after.** A deal spikes rank. Define how to hold the gain: ads ready to
   defend the new rank, stock to stay in stock, no price jump right after.

7. **Run the quality check**, then deliver.

## Output format

```
## Deal Plan. [product]

Goal: [goal]
Deal-ready: [yes / no, with what to fix first]

### Recommended deal
Type: [deal type]   Timing: [event or date]
Deal price: [$]

### Math
Per-unit contribution at deal price (deal fee included): [$]
Verdict: [profitable / acceptable rank investment / do not run]

### Hold the gain
[post-deal plan to keep the rank]
```

## Worked example

Product at 50 USD, 4.3 stars, 600 reviews, healthy stock. Goal: rank push before Q4.

Deal-ready: yes. Recommended: a Lightning Deal timed to Prime Big Deal Days, deal
price 40 USD. Math: per-unit contribution roughly 4 USD after fees and the deal fee
spread, a thin but positive number. The deal is run as a rank investment. After the
deal, Sponsored Products bids are raised for two weeks to defend the new rank and the
price returns to 50 without a gap that would stall momentum.

## Quality check

- The deal-ready check ran first. rating, reviews, stock.
- A listing that is not deal-ready is told to fix that before any deal.
- The math spreads the deal fee across a realistic unit estimate.
- Any loss is explicitly labeled an acceptable rank investment or rejected.
- The deal is timed to the highest-traffic window available.
- There is a written plan to hold the rank gain after the deal ends.

## Common mistakes

- **Dealing a weak listing.** Pouring event traffic into a 3.8-star listing buys
  proof that it does not convert and wastes the fee.
- **Ignoring the deal fee.** The fee can turn a "profitable" deal price into a loss.
- **Off-peak deals.** The same fee buys a fraction of the reach off-event.
- **No after-plan.** The deal spikes rank, then rank slides back because nothing was
  in place to defend it.
- **Stocking out mid-deal.** A deal that sells out early wastes the visibility window.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
