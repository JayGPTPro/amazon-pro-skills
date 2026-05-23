---
name: amz-ipi-recovery-plan
description: >-
  Build a 30-60-90 day plan to recover Amazon's Inventory Performance Index
  (IPI) and lift FBA capacity limits. Diagnoses which of the four IPI levers
  (excess, sell-through, stranded, in-stock) is pulling the score down and
  prescribes a weekly action list. Use when a user asks about IPI score, FBA
  capacity limits, restock limits, low IPI, excess inventory, or stranded
  inventory. Trigger phrases: "IPI", "IPI score", "capacity limits", "restock
  limits", "excess inventory", "stranded inventory". Works with zero tools.
  the user provides IPI score and inventory breakdown.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# IPI Recovery Plan

A low IPI tightens FBA capacity limits just when a seller wants to grow. The score
moves on four levers, and the recovery requires sustained weekly action, not a one-
time push. This skill identifies the binding lever and builds the 30-60-90 plan.

## When to use this

- IPI dropped 30-100 points overnight after the mid-2025 tightening.
- Capacity limits are now restrictive and the seller cannot send in enough inventory.
- Routine quarterly IPI check.
- Preparing for Q4 and need IPI strong enough to support the seasonal restock.

## The framework. The Four Levers

IPI is driven by four levers. Diagnose which is binding before any plan.

| Lever | What it measures | Quick lift |
|-------|------------------|-----------|
| Excess inventory | Units beyond 90-day demand | Remove or destroy aging stock |
| Sell-through rate | Units sold / units in inventory | Promote slow movers or cut them |
| Stranded inventory | Units that exist but cannot sell (suppressed listings, no offer) | Fix listing or relist |
| In-stock rate | % of time the active SKUs are in stock | Restock the right SKUs on schedule |

A single binding lever usually accounts for most of the drop. fix that first.

## The 30-60-90

- **Days 1-7.** Diagnose the binding lever from the inventory dashboard. Open the
  Manage Excess Inventory and Stranded Inventory tools. Build the action list.
- **Days 8-30.** Execute on the binding lever. Remove or liquidate excess. Fix
  stranded listings. The IPI score typically responds within 2 to 3 weeks.
- **Days 31-60.** Sell-through improvements (promotions, ad pushes on the slow
  movers) and in-stock improvements (reorder schedule).
- **Days 61-90.** Stabilize. Weekly review. Confirm the score holds and the capacity
  limit lifted.

## Step by step

1. **Collect inputs.** Current IPI score, the four-lever breakdown if available,
   excess inventory units and SKUs, stranded inventory units and reasons, in-stock
   rate per top SKU.

2. **Identify the binding lever.** Where the most points are being lost.

3. **Build the 30-60-90 plan.** Specific actions tied to the binding lever first.

4. **Compute the inventory implications.** Removing excess costs removal fees but
   frees capacity. liquidating loses some margin but recovers some cash and lifts
   IPI. Weigh per SKU.

5. **Set the score-watch cadence.** IPI updates weekly. plan a weekly review during
   the 90 days.

6. **Tie to next steps.** A recovered IPI lifts capacity. Plan the restock that
   uses the new room.

7. **Run the quality check**, then deliver.

## Output format

```
## IPI Recovery Plan. [account]

Current IPI: [score]   Binding lever: [which]

### 30 days
[binding-lever actions, weekly]

### 60 days
[secondary-lever actions]

### 90 days
[stabilization + capacity utilization]

### Watch
IPI weekly. capacity limit weekly. flag if either moves the wrong way.
```

## Worked example

IPI at 380, binding lever is excess inventory (220 units across 8 SKUs aged past 180
days). Plan: days 1-7 review removal vs liquidate per SKU through
`amz-removal-vs-storage-calculator`, file removals for the 5 SKUs with no recoverable
value and run liquidation deals on the other 3. Days 8-30: execute, watch the IPI
weekly. Days 31-60: address sell-through on the next-slowest tier with promotions and
ad pushes. Days 61-90: stabilize and use the recovered capacity to restock the top
movers for Q4. Score typically lifts to the 450-500 range and the capacity limit
loosens by week 6.

## Quality check

- The binding lever is identified before any plan is written.
- The plan addresses the binding lever in the first 30 days, not later.
- Removal vs liquidation is weighed per SKU, not flat.
- A weekly review cadence is set.
- The plan ends with using the recovered capacity, not just hitting the score.

## Common mistakes

- **Cutting blindly.** Mass-removing all aging stock without weighing recovery value.
- **Ignoring stranded.** Stranded inventory is often the cheapest lever to fix
  because it just needs a listing or offer fix.
- **Restocking before recovery.** Adding more inventory while the score is low
  worsens the excess metric and tightens the limit further.
- **No weekly review.** IPI updates weekly. monthly checks miss the trajectory.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
