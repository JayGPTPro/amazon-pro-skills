---
name: amz-launch-runway
description: >-
  Build a complete Amazon product launch plan. the 30-day runway from go-live to
  established rank. Sequences the pre-launch checklist, the review ramp, the ad
  and deal cadence, the price strategy, and the daily and weekly milestones that
  turn a new listing into a ranking product. Use when a user asks how to launch
  a product on Amazon, a launch plan, a launch strategy, a launch checklist, a
  product launch timeline, or how to rank a new product. Trigger phrases:
  "launch plan", "launch strategy", "how to launch", "product launch", "launch
  checklist", "launch runway", "rank a new product". Works with zero tools.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Launch Runway

A launch is the most important 30 days in a product's life. Amazon decides early how
much organic traffic a new listing deserves, and that early verdict is hard to
reverse. A launch is not "publish the listing and run ads". it is a sequenced runway.
This skill builds it.

## When to use this

- A new product is about to go live and needs a launch plan.
- A product launched flat and the seller wants to understand what was missed.
- A relaunch of a product that never gained traction.
- Planning the launch budget and timeline before committing inventory.

## Launch budget by category tier

Total 30-day launch spend (ads, deal fees, coupon redemptions, Vine costs)
scales with category and ASP. A 12 USD pantry item and a 120 USD electronics
item have different launch math. plan to a tier, not a flat number.

| Category tier | Typical ASP | 30-day launch budget |
|---------------|-------------|----------------------|
| Small / lifestyle / impulse | Under 20 USD | 500 to 2,000 USD |
| Mid / household / utility   | 20 to 50 USD | 2,000 to 10,000 USD |
| Premium / electronics / gear| Above 50 USD | 10,000 USD and up |

The ranges are not the cost of the product, they are the cost of the launch. CPC
in the small/lifestyle tier is low and ranking is mostly a long-tail
conversion-rate game, so the runway is cheap. In the premium tier CPC is high,
Phase 1 ACoS runs hot, and the launch needs depth to survive 30 days at the rate
needed to earn rank. Picking the wrong tier is the most common reason a launch
runs out of money in week 2.

Inside the tier, split the budget roughly. 60 percent Phase 1 (ignition, hottest
ACoS), 25 percent Phase 2 (velocity push, deals or coupon), 15 percent Phase 3
(stabilize, shifting to harvest). adjust if the price ladder calls for a deeper
mid-launch deal.

## The framework. The Four-Phase Runway

A launch runs in four phases. Each phase has one job, and the next phase fails if the
previous one was skipped.

### Phase 0. Pre-launch (before go-live)

The launch is mostly won here. Before the listing is public, confirm:

- The listing is complete and converting-ready: title, bullets, the full image set
  (see amz-listing-images), A+ Content, backend keywords, the keyword map.
- The unit economics work and the break-even ACoS is known (see amz-fba-calculator).
- Inventory is checked in at FBA with enough depth to survive the launch spike. a
  stockout mid-launch is fatal.
- The first reviews are arranged: Vine units enrolled (see amz-vine-program).
- The launch budget is set: ad spend plus any deal fees.

If a Phase 0 item is not done, do not go live. A launch into an incomplete listing
burns the early-traffic verdict.

### Phase 1. Days 1 to 7. Ignition

The job is the first sales and the first reviews, not profit.

- Price slightly low to lift early conversion. not a fire sale, a gentle edge.
- Turn on Sponsored Products: an auto campaign for discovery and an exact campaign on
  the launch-priority long-tail keywords (see amz-ppc-campaign and amz-keyword-research).
- ACoS will be high. that is expected. Phase 1 buys rank, not margin.
- The first Vine reviews start landing.

### Phase 2. Days 8 to 21. Velocity

The job is sustained sales velocity on the target keywords to earn organic rank.

- Hold the ad push. Start reading the search term report. negate the drains, raise
  bids on the converters.
- Graduate converting discovery terms into the exact campaign.
- Consider a Lightning Deal or a coupon for a mid-launch velocity spike (see
  amz-deal-finder and amz-coupon-strategy).
- Watch organic rank on the launch-priority keywords. it should be climbing.

### Phase 3. Days 22 to 30. Stabilize

The job is to convert the bought rank into self-sustaining organic rank.

- Begin easing the launch price toward the target price, in steps, watching that
  conversion and rank hold.
- Shift ad budget from pure discovery toward the proven harvest keywords. ACoS should
  be falling toward target.
- The product should now hold rank with less ad support. that is the launch succeeding.

## Step by step

1. **Collect inputs.** The product, the listing readiness, the unit economics and
   break-even ACoS, the inventory position, the keyword map, the review plan, and the
   launch budget.

2. **Audit Phase 0.** Mark every pre-launch item done or not done. If anything is
   not done, the plan is to finish Phase 0 before go-live, full stop.

3. **Build the Phase 1 to 3 calendar.** Specific actions per phase, with the daily
   and weekly checkpoints.

4. **Set the price ladder.** The launch price, and the steps back up to the target
   price across Phase 3.

5. **Set the ad plan per phase.** Campaign types, the ACoS expectation per phase
   (high in Phase 1, falling by Phase 3), and the budget split.

6. **Set the metrics and the alarms.** Organic rank on the priority keywords, units
   per day, conversion rate, and the alarms: a stockout risk, conversion below
   expectation, rank not climbing by mid-launch.

7. **Run the quality check**, then deliver.

## Output format

```
## Launch Runway. [product]

### Phase 0. Pre-launch audit
[item] . [done / not done]
Go-live gate: [clear / finish Phase 0 first]

### Phase 1. Days 1 to 7. Ignition
Price: [launch price]   Ads: [setup]   ACoS expectation: [high]
Actions and checkpoints: ...

### Phase 2. Days 8 to 21. Velocity
Actions: [search term report, graduations, deal or coupon]
Watch: organic rank climbing on [priority keywords]

### Phase 3. Days 22 to 30. Stabilize
Price ladder: [steps back to target]
Ad shift: [discovery to harvest]   ACoS expectation: [falling to target]

### Metrics and alarms
Track: organic rank, units/day, conversion rate
Alarms: [stockout risk, low conversion, rank not climbing]
```

## Worked example

A new 32 oz insulated water bottle, target price 30 USD, break-even ACoS 40 percent.

Phase 0: listing complete, 30 Vine units enrolled, inventory in with launch-spike
depth, budget set. Go-live gate clear. Phase 1: launch price 26, auto plus exact
campaigns on the long-tail launch keywords, ACoS running near 70 percent and that is
fine, it is buying rank. Phase 2: search term report worked weekly, converters
graduated, a Lightning Deal on day 14 for a velocity spike, organic rank on "32 oz
insulated bottle for hiking" climbing from page 4 toward page 2. Phase 3: price
stepped 26 to 28 to 30 while conversion holds, ad budget shifted to the proven
harvest keywords, ACoS settling toward 35 percent. By day 30 the bottle holds page-2
rank on its priority keywords with far less ad support than it needed on day 1.

## Quality check

- The Phase 0 audit is run first, and an incomplete Phase 0 blocks go-live.
- Each of the four phases has its one clear job, and the actions match the job.
- Phase 1 ACoS is expected to be high. the plan does not judge the launch on it.
- A price ladder steps from the launch price back to the target price across Phase 3.
- The plan tracks organic rank on the priority keywords, not just total sales.
- Alarms cover the launch killers: stockout, weak conversion, rank not climbing.

## Common mistakes

- **Launching into an incomplete listing.** The early-traffic verdict is spent on a
  listing that cannot convert.
- **Judging Phase 1 by ACoS.** Phase 1 buys rank. a high ACoS there is the plan
  working, not failing.
- **Stocking out mid-launch.** The single most damaging launch failure. momentum and
  rank are lost and do not fully return.
- **Never raising the price.** Camping at the launch price forever and never reaching
  the target margin.
- **No keyword focus.** Spreading the launch across head terms instead of winning the
  priority long-tail first.
- **Quitting at day 14.** The launch is 30 days. Phase 3 is where bought rank becomes
  organic rank.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
