---
name: amz-stockout-recovery-plan
description: >-
  Produces a 30-day day-by-day recovery plan after an Amazon stockout. Aggressive
  PPC, external traffic, review velocity, A+ refresh, in the right sequence. A
  structured sequence recovers BSR far faster than doing nothing, which can leave
  a listing depressed for a quarter. Use when a user mentions stockout, ranking
  lost, BSR recovery, or post-stockout. Trigger phrases: "Amazon stockout recovery",
  "ranking lost after stockout", "BSR recovery", "post-stockout playbook".
  Works with zero tools.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Stockout Recovery Plan

You stocked out. Three days dark, ranking gone. PPC bid suggestions look
insane. Most sellers either burn cash trying to claw back with no plan,
or they do nothing and watch BSR sit depressed for weeks. There is a real
playbook. Execute it day-by-day and you give the listing the best shot at a
fast recovery. Skip it and you risk a quarter of lost momentum. The numbers
in this skill are illustrative examples. your actual recovery curve depends on
category, stockout length, competition, and how cleanly you execute.

## When to use this

- Inventory just arrived after a 3+ day stockout
- BSR has dropped 40%+ from pre-stockout baseline
- A new variation launched after the parent stocked out
- A SKU recovered units from FBA hold and is back live

## The framework. The 30-Day Recovery Curve

The recovery has 4 phases. Each phase has a specific PPC posture, traffic
source, and check-in metric.

| Phase | Days | PPC posture | Traffic priority | Metric to watch |
|---|---|---|---|---|
| 1. Re-entry blast | 1-3 | Bids 2x suggested, all match types, full coupon | Full coupon stack | Sessions/day |
| 2. External burst | 4-7 | Bids 1.5x, focus exact match | TikTok, IG, attribution links | Off-Amazon CTR |
| 3. Velocity push | 8-14 | Bids 1.2x, harvest converters | Review velocity, A+ refresh | Reviews/day, CVR |
| 4. Stabilize | 15-30 | Bids 1.0x, normalize ACoS | Organic | BSR vs baseline |

Illustrative outcome: in a clean recovery, you might see BSR climb back toward
its pre-stockout level over the 30 days, with most of the gain in the back half
of the curve. Treat any specific percentage as an example, not a promise. the
real curve depends on category, stockout length, and competition. Stockouts
longer than 7 days tend to lose this curve and need a relaunch strategy instead.

## Step by step

1. **Confirm inventory live.** Verify FBA shows In Stock, Buy Box won, Prime
   badge active. Do not start the curve until all 3 are true.

2. **Day 1-3 Re-entry Blast.** Raise all keyword bids to 2x Amazon suggested.
   Enable all match types (broad, phrase, exact, auto). Stack a 15% coupon +
   Subscribe & Save 10% + Sponsored Display retargeting. Daily budget = 3x
   normal. Goal: flood with sessions, force algorithm to re-evaluate.

3. **Day 4-7 External Burst.** Drop PPC to 1.5x. Run 3 TikTok creator partnerships
   ($150-$300 each) with attribution links. Post 5 IG stories with product
   tag. Send to email list with 10% off code. Goal: external traffic signals
   high to A9/COSMO.

4. **Day 8-14 Velocity Push.** Drop PPC to 1.2x, focus exact match converters.
   Refresh A+ Content (even minor edits trigger a re-crawl). Push review
   velocity with Request a Review on every eligible order. Target 1.5x normal
   review rate. Goal: review momentum and on-page relevance signals.

5. **Day 15-30 Stabilize.** Normalize PPC to 1.0x. Monitor BSR vs pre-stockout
   baseline daily. Use the day-21 gate below to judge whether the curve is
   tracking or needs an extension. these thresholds are decision triggers you
   set, not a predicted result.

6. **Daily check-ins.** Build a tracker: Sessions, CVR, BSR, ACoS, Reviews
   added. Compare to pre-stockout 7-day average.

7. **Decision gate day 21.** If BSR < 60% of baseline, extend Phase 3 by 7
   days with additional review velocity push. If BSR >= 80%, transition to
   normal ops.

8. **Run the quality check**, then execute.

## Output format

```
## Stockout Recovery Plan. [ASIN]

**Baseline metrics (7-day avg pre-stockout)**
- Sessions/day: [N]
- CVR: [N%]
- BSR: [N]
- Reviews/day: [N]
- Avg daily ad spend: $[N]

**Phase 1: Days 1-3 Re-entry Blast**
- PPC: All bids x2 suggested, all match types ON, daily budget $[N x 3]
- Coupon: [N%] + S&S [N%] + Sponsored Display retargeting
- Daily check: sessions/day target [N x 1.5]

**Phase 2: Days 4-7 External Burst**
[same structure]

**Phase 3: Days 8-14 Velocity Push**
[same structure]

**Phase 4: Days 15-30 Stabilize**
[same structure]

**Day 21 decision gate**
- BSR < 60% baseline -> extend Phase 3 by 7 days
- BSR 60-79% -> continue Phase 4
- BSR >= 80% -> normal ops
```

## Worked example (illustrative)

The numbers below are a made-up scenario to show the shape of the plan, not a
benchmark to expect. Your sessions, costs, and recovery pace will differ.

ASIN: B0EXAMPLE, dog leash. Pre-stockout baseline: 220 sessions/day, CVR 9.4%,
BSR #847 in Pet Supplies, 1.2 reviews/day, $86/day ad spend. Stockout duration
5 days, recovery starts Nov 4 with 600 units in FBA.

Phase 1 (Nov 4-6): PPC bids raised from $0.84 avg to $1.68 avg, all match
types on, $258 daily budget. 15% coupon active + 10% S&S + Sponsored Display
retargeting last-90-day viewers. Day 3 sessions: 312 (1.4x baseline). Cost
$774 over 3 days.

Phase 2 (Nov 7-10): PPC dropped to 1.5x. 3 TikTok creators booked at $180
each ($540). Attribution links generate 47 off-Amazon sessions/day. Email
blast to 3,400 subscribers with code DOGLEASH10. Day 7 sessions: 380.

Phase 3 (Nov 11-17): PPC at 1.2x exact match only. A+ Content refreshed with
2 new modules. Request a Review on all 156 orders from Phase 1+2. Reviews
added in Phase 3: 14 (vs baseline 8 over 7 days).

Phase 4 (Nov 18 onward): PPC normalized. In this example the listing climbs back
toward its #847 baseline over the back half of the curve, with the day-21 and
day-30 checks used to decide whether to extend Phase 3. Your own BSR path will
look different. the point is the sequence and the gates, not these specific ranks.

Costs in this scenario run to a few thousand dollars of incremental PPC plus a
modest creator spend. Whether that pencils out depends on your margin and unit
economics. run your own avoided-loss math rather than assuming a fixed return.
A structured recovery is generally cheaper than letting BSR sit depressed, but
the exact net is yours to compute, not a number this skill can promise.

## Quality check

- Inventory confirmed live before Day 1 start (Buy Box + Prime badge + In Stock)
- Daily metrics logged, not weekly averages
- External traffic uses attribution links, not vanity URLs
- A+ refresh is real edit, not just save-without-change
- Day 21 decision gate is enforced, not waved past

## Common mistakes

- **Starting at "normal" PPC bids.** Algorithm needs the signal flood. 2x bids day 1-3 is the price of admission.
- **Skipping external traffic.** Off-Amazon signals are weighted in 2026 A9/COSMO. PPC alone is not enough.
- **No A+ refresh.** Page-edit signals trigger a re-crawl and can lift conversion. treat any specific percentage as listing-dependent, not guaranteed.
- **No daily tracking.** Without metrics, you cannot tell if Phase 3 needs an extension.
- **Stockouts over 7 days.** Past 7 days, the curve breaks. Treat as relaunch, not recovery.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
