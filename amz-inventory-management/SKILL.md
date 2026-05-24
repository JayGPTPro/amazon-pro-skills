---
name: amz-inventory-management
description: >-
  Plan Amazon FBA inventory end to end. Calculates reorder timing and quantity,
  safety stock, week-by-week days of cover, builds a 12-week PO schedule,
  applies ASIN-level restock limits and seasonal multipliers, watches the IPI
  score levers, and surfaces stranded and aged inventory. Use when a user asks
  about restocking, when to reorder, how much to order, running out of stock,
  the IPI score, restock limits, ASIN restock limit, days of cover, 90-day
  forecast, restock schedule, long-term storage fees, aged inventory, or
  stranded inventory. Trigger phrases. "inventory management", "when to
  reorder", "restock", "safety stock", "IPI score", "stockout", "aged
  inventory", "long-term storage", "reorder schedule", "forecast", "days of
  cover", "ASIN restock limit". Works with zero tools. the user provides sales
  rate and lead times.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Inventory Manager

Inventory is where Amazon sellers lose money in both directions. Stock out and you
lose rank and sales that do not come back. Overstock and you pay storage fees and
freeze cash. Restocking by feel produces stockouts and overstock at the same time.
This skill finds the reorder point and the order quantity that keep a product in
stock without burying cash in a warehouse, and projects the schedule 12 weeks
forward with capacity limits and seasonality baked in.

## When to use this

- A seller does not have a reorder rule and restocks by feel.
- A product stocked out, lost rank, and the seller wants it never to happen again.
- Storage fees or long-term storage fees are eating margin.
- The IPI score is low or restock limits are biting.
- ASIN-level restock limits reactivated and the seller needs to fit within them.
- Stranded or aged inventory is sitting unsold.
- Q4 ramp planning where seasonal demand multiplies and lead times often slip.
- A new SKU stabilizing and needing its first forecast.

## The framework. The Reorder Equation

Two numbers govern inventory: when to order and how much. Both come from sales rate
and lead time.

**Reorder point.** Order when stock on hand falls to:

```
Reorder point = (daily sales rate x total lead time in days) + safety stock
```

Total lead time is everything from placing the purchase order to the units being
live and sellable: production, freight, customs, Amazon receiving and check-in.
Sellers forget the receiving leg and stock out anyway.

**Safety stock.** A buffer for demand spikes and lead-time slippage:

```
Safety stock = daily sales rate x buffer days
```

Buffer days scale with volatility. a steady product with reliable supply needs ~14
days, a volatile or unreliable supply chain needs 21 to 30.

**Order quantity.** Enough to cover the cycle until the next reorder lands, balanced
against storage cost and cash. A common target is 60 to 90 days of cover. more than
that risks long-term storage fees and frozen cash, less risks stockouts on any lead-
time slip.

## The 12-week schedule. Days-of-Cover model

The reorder equation tells you when one PO fires. The schedule tells you when the
next three or four will. Two metrics drive it.

- **DoC on hand = units on hand / daily sales rate.** Watch daily.
- **Reorder point** as defined above.

Project DoC forward week by week for 12 weeks. apply any seasonal multiplier in the
weeks where a peak lands (see amz-seasonal-planning). When projected DoC dips below
the reorder point's days-equivalent, that is an order week. Compute order quantity
as target days of cover x daily rate, then apply the ASIN restock limit and the
account capacity limit as hard caps.

For peak windows, pull the order forward and increase the size to land stock before
the peak begins, not during it.

## The IPI and FBA capacity limits

Amazon replaced the strict IPI minimum with **FBA capacity limits** in March 2023.
Capacity is now governed by recent sales, IPI, and forecast demand together, not by a
hard IPI floor. IPI still matters as one input. it is driven by four levers: low
excess inventory, healthy sell-through, fixing stranded inventory, and keeping
in-stock rate high. Manage all four, and watch the capacity dashboard for the actual
restock limit on the account.

## Step by step

1. **Collect inputs.** Per SKU: daily or weekly sales rate (use last 90 days of
   real sales, not historical average), current stock on hand, each leg of the
   lead time (production, freight, customs, Amazon receiving), demand volatility,
   any seasonality multipliers per week, current IPI, the account capacity limit,
   and any ASIN-level restock limit.

2. **Compute total lead time** including the Amazon receiving leg.

3. **Set safety stock** from the volatility. larger buffer for spiky or seasonal
   SKUs.

4. **Compute the reorder point.** Flag any SKU already at or below it as order now.

5. **ASIN restock limit binding check.** Compare the desired order quantity (target
   DoC x daily rate) against the ASIN-level restock limit. If the limit is below
   the desired quantity, the limit is binding. the SKU will run lean unless the
   limit is raised. plan to request a capacity increase or to space POs more
   tightly. Note this as a constraint in the output, not as a fix to ignore.

6. **Project the 12-week DoC schedule.** Apply seasonal multipliers per week.
   Mark each order week and order quantity.

7. **Set the order quantity** for 60 to 90 days of cover, capped by the binding
   restock limit and adjusted for upcoming seasonality. Pull peak-window POs
   earlier and larger.

8. **Scan for waste.** Identify aged inventory approaching long-term storage fees
   and any stranded inventory (in stock but not sellable), and recommend the fix:
   markdown, removal, or relisting.

9. **Check the IPI levers** and name the weakest one.

10. **Run the quality check**, then deliver.

## Output format

```
## Inventory Plan. [SKU or catalog]

### Per SKU
[SKU] . daily rate . on hand . reorder point . status [ok / order now] . order qty
       . restock limit binding? [y/n]
...

### 12-week DoC projection (per priority SKU)
Week 1: [DoC]   Week 2: [DoC]   ...   Week 12: [DoC]
Seasonal multipliers applied: [Nx in week X, ...]

### Order schedule
PO 1. Place by [date]. Quantity: [units]. Arrives in stock: [date]
PO 2. ...

### Waste scan
Aged inventory: [SKUs approaching long-term storage fees]
Stranded inventory: [SKUs in stock but not sellable]

### Constraints
Restock limit binding on: [SKUs]
Capacity increase request needed: [y/n]

### IPI
Current: [score]   Weakest lever: [which]   Fix: ...

### This week
[ordered by urgency]
```

## Worked example

A SKU sells 25 units a day. Lead time: 30 days production, 25 days freight and
customs, 7 days Amazon receiving, total 62 days. Volatility is moderate, buffer 21
days. ASIN restock limit 3,000 units.

Safety stock: 25 x 21 = 525. Reorder point: (25 x 62) + 525 = 2,075 units. The SKU
is at 2,200 on hand. DoC = 88 days. Reorder point hits at roughly week 1-2. Order
quantity for 75 days of cover: about 1,875 units. ASIN restock limit binding check.
3,000 limit, 1,875 desired, not binding at this order, fine. A week-10 peak with a
3x multiplier needs an earlier larger PO at week 7. landed-before-peak schedule
shows PO1 at week 1 (1,875 units), PO2 at week 7 (3,000 units, restock limit now
binding for the peak, request an increase before week 5).

The seller had been reordering at 600 units on hand and stocking out during every
freight delay. The new schedule shows exactly when to place each PO and how much,
with no stockout risk and no excess.

## Quality check

- Total lead time includes the Amazon receiving leg, not just production and freight.
- Daily rate is computed from real recent sales, not historical average.
- Safety stock scales with the SKU's demand volatility.
- Every SKU at or below its reorder point is flagged order now.
- DoC is projected weekly for 12 weeks, not as a snapshot.
- ASIN-level restock limit is checked as a binding constraint, not ignored.
- Account capacity limit is respected.
- Order quantity targets 60 to 90 days of cover.
- Seasonal pre-orders are placed early enough to land before the peak.
- Aged and stranded inventory are surfaced with a specific fix.
- The weakest IPI lever is named.

## Common mistakes

- **Forgetting the receiving leg.** Units are not sellable the day they arrive at the
  warehouse. that gap causes stockouts.
- **Reordering by feel or on a fixed cadence.** A monthly PO regardless of cover is
  wrong both ways: stockouts in fast weeks, overstock in slow.
- **Overordering.** Burying cash and triggering long-term storage fees to feel safe.
- **Ignoring the ASIN restock limit.** Ordering 5,000 when the ASIN limit is 3,000
  means 2,000 units stuck or expensive to send via STA capacity.
- **Ignoring stranded inventory.** Units in the warehouse that are not even listed as
  sellable, earning nothing and costing storage.
- **No seasonal multiplier.** A baseline forecast through a peak guarantees a stockout.
- **Letting IPI drift.** A low IPI caps restock limits right when a product is taking off.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
