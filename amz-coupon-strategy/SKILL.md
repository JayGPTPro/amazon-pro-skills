---
name: amz-coupon-strategy
description: >-
  Plan Amazon coupons that lift conversion without leaking margin. Decides
  between percentage and dollar-off coupons, sets the right discount depth,
  picks the goal (launch, conversion lift, review velocity, stock clearance),
  and checks the math against fees and margin. Use when a user asks about
  coupons, the green coupon badge, percentage vs dollar off, coupon discount
  depth, or whether a coupon is worth running. Trigger phrases: "coupon",
  "coupon strategy", "coupon badge", "percentage off coupon", "dollar off
  coupon". Works with zero tools. the user provides price, cost, and fees.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Coupon Strategy

The coupon badge is a green flag on the search page that earns clicks before a
shopper ever opens the listing. That visibility is the real value of a coupon. the
discount is almost secondary. This skill plans coupons that buy the badge and the
conversion lift without quietly destroying margin.

## When to use this

- Launching a product and wanting the badge for visibility and early velocity.
- A listing has traffic but a soft conversion rate.
- Clearing aging stock before long-term storage fees hit.
- A seller is running coupons by feel and is not sure they are profitable.

## The framework. The Coupon Decision

Three decisions, in order. Get them in this order or the coupon loses money.

### 1. The goal sets the depth

| Goal | Depth | Why |
|------|-------|-----|
| Badge visibility on a healthy listing | 5 to 10% | The badge does the work, not the price |
| Launch velocity | 10 to 20% | Buy early sales and rank |
| Conversion lift on a stalled listing | 10 to 15% | Enough to tip the hesitant buyer |
| Stock clearance before storage fees | 20%+ | The fee you avoid funds the discount |

### 2. Percentage or dollar off

- **Percentage off** scales with price and reads as generous on low-priced items.
- **Dollar off** reads stronger on higher-priced items. "15 USD off" beats "10% off"
  on a 150 USD product even though the math is identical.
- Pick the format that makes the bigger number visible to the shopper.

### 3. The margin floor

Compute the post-coupon contribution: price, minus coupon, minus referral fee, minus
FBA fee, minus unit cost. Amazon also charges a per-redemption coupon fee. that fee
is on the 2026 redemption fee tier, which Amazon adjusts periodically. before
launching, verify the current per-redemption rate in the Seller Central coupon
dashboard and plug that number into the math. do not run the math on a remembered
or stale rate.

If the post-coupon contribution is at or below zero, the coupon is a loss machine.
For launch you may accept a thin or zero margin deliberately. for an evergreen coupon
you may not.

## A note on the minimum

Amazon enforces a minimum coupon discount, currently 5 percent. Some categories
enforce more, and the Deal badge requires a deeper discount (typically 15 percent or
more). A coupon below the minimum will not run.

## Step by step

1. **Collect inputs.** Price, unit cost, referral fee percent, FBA fee, the goal, and
   any deadline (a storage-fee date, a launch window).

2. **Set depth from the goal**, using the table.

3. **Pick the format**, percentage or dollar off, by which number looks bigger to the
   shopper at this price point.

4. **Run the margin math.** Post-coupon contribution equals price minus coupon minus
   referral fee minus FBA fee minus unit cost minus the current per-redemption fee
   (2026 redemption fee tier, verify in the dashboard before launching). State the
   number.

5. **Decide go or no-go.** If contribution is positive, run it. If zero or negative,
   it is acceptable only for launch or clearance, and say so explicitly.

6. **Set the window and budget.** Coupons run until the budget is spent. Cap the
   budget so a viral redemption does not blow past the plan.

7. **Run the quality check**, then deliver.

## Output format

```
## Coupon Plan. [product]

Goal: [goal]
Format: [percentage / dollar off] . Depth: [X]
Shopper sees: ["X% off" or "$X off"]

### Margin math
Price [$] . coupon [-$] . referral fee [-$] . FBA [-$] . unit cost [-$] . redemption fee [-$]
Post-coupon contribution: [$]
Verdict: [profitable / launch-only / clearance-only / do not run]

### Run plan
Budget cap: [$]   Window: [dates or until budget]
```

## Worked example

Product at 45 USD, unit cost 14, referral fee 15 percent, FBA fee 6. Goal: conversion
lift on a stalled listing.

Depth 12 percent, 5.40 USD off. Format: percentage. at 45 USD, "12% off" reads
cleaner than "$5 off" even though the math is identical. Margin math: 45 minus 5.40
minus 6.75 referral minus 6 FBA minus 14 cost minus the current per-redemption fee
(pull from the dashboard, 2026 tier) leaves roughly 12 USD contribution. Positive.
Run it, budget capped at a defined dollar amount.

## Quality check

- The depth is set by the stated goal, not picked arbitrarily.
- The format choice is justified by which number looks bigger to the shopper.
- Post-coupon contribution is computed including the per-redemption fee.
- A zero or negative contribution coupon is flagged as launch-only or clearance-only.
- The coupon budget is capped so redemptions cannot overshoot.

## Common mistakes

- **Forgetting the redemption fee.** Amazon charges per redeemed coupon. margin math
  that omits it is wrong.
- **Going deep for visibility.** A healthy listing needs the badge, not a 25 percent
  cut. The badge earns the click at 5 percent.
- **No budget cap.** A coupon that goes mildly viral can redeem far past plan.
- **Wrong format.** "8% off" on a 12 USD item looks like nothing. dollar-off vs
  percentage is a real lever.
- **Evergreen coupons at zero margin.** Acceptable for launch, not as a permanent
  state.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. 50 production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
