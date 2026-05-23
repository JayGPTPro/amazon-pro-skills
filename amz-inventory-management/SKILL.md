---
name: amz-inventory-management
description: >-
  Plan Amazon FBA inventory. calculates reorder timing and quantity, safety
  stock, days of cover, the IPI score levers, and surfaces stranded and aged
  inventory. Use when a user asks about restocking, when to reorder, how much to
  order, running out of stock, the IPI score, restock limits, long-term storage
  fees, aged inventory, or stranded inventory. Trigger phrases: "inventory
  management", "when to reorder", "restock", "safety stock", "IPI score",
  "stockout", "aged inventory", "long-term storage". Works with zero tools. the
  user provides sales rate and lead times.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Inventory Manager

Inventory is where Amazon sellers lose money in both directions. Stock out and you
lose rank and sales that do not come back. Overstock and you pay storage fees and
freeze cash. This skill finds the reorder point and the order quantity that keep a
product in stock without burying cash in a warehouse.

## When to use this

- A seller does not have a reorder rule and restocks by feel.
- A product stocked out, lost rank, and the seller wants it never to happen again.
- Storage fees or long-term storage fees are eating margin.
- The IPI score is low or restock limits are biting.
- Stranded or aged inventory is sitting unsold.

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

Buffer days scale with volatility. a steady product needs a small buffer, a seasonal
or spiky product needs a large one.

**Order quantity.** Enough to cover the cycle until the next reorder lands, balanced
against storage cost and cash. A common target is 60 to 90 days of cover. more than
that risks long-term storage fees and frozen cash, less risks stockouts on any lead-
time slip.

## The IPI and FBA capacity limits

Amazon replaced the strict IPI minimum with **FBA capacity limits** in March 2023.
Capacity is now governed by recent sales, IPI, and forecast demand together, not by a
hard IPI floor. IPI still matters as one input. it is driven by four levers: low
excess inventory, healthy sell-through, fixing stranded inventory, and keeping
in-stock rate high. Manage all four, and watch the capacity dashboard for the actual
restock limit on the account.

## Step by step

1. **Collect inputs.** Daily or weekly sales rate per SKU, current stock on hand,
   each leg of the lead time, demand volatility, any seasonality, and current IPI and
   any restock limit.

2. **Compute total lead time** including the Amazon receiving leg.

3. **Set safety stock** from the volatility, larger buffer for spiky or seasonal SKUs.

4. **Compute the reorder point.** Flag any SKU already at or below it as order now.

5. **Set the order quantity** for 60 to 90 days of cover, adjusted for seasonality and
   for restock limits.

6. **Scan for waste.** Identify aged inventory approaching long-term storage fees and
   any stranded inventory (in stock but not sellable), and recommend the fix:
   markdown, removal, or relisting.

7. **Check the IPI levers** and name the weakest one.

8. **Run the quality check**, then deliver.

## Output format

```
## Inventory Plan. [SKU or catalog]

### Per SKU
[SKU] . daily rate . on hand . reorder point . status [ok / order now] . order qty
...

### Waste scan
Aged inventory: [SKUs approaching long-term storage fees]
Stranded inventory: [SKUs in stock but not sellable]

### IPI
Current: [score]   Weakest lever: [which]   Fix: ...

### This week
[ordered by urgency]
```

## Worked example

A SKU sells 20 units a day. Lead time: 30 days production, 25 days freight and
customs, 7 days Amazon receiving, total 62 days. Volatility is moderate, buffer 14
days.

Safety stock: 20 x 14 = 280. Reorder point: (20 x 62) + 280 = 1,520 units. The SKU is
at 1,400 on hand, already below the reorder point, so it is order now. Order quantity
for 75 days of cover: about 1,500 units. The seller had been reordering at 600 units
on hand and stocking out during every freight delay.

## Quality check

- Total lead time includes the Amazon receiving leg, not just production and freight.
- Safety stock scales with the SKU's demand volatility.
- Every SKU at or below its reorder point is flagged order now.
- Order quantity targets 60 to 90 days of cover and respects restock limits.
- Aged and stranded inventory are surfaced with a specific fix.
- The weakest IPI lever is named.

## Common mistakes

- **Forgetting the receiving leg.** Units are not sellable the day they arrive at the
  warehouse. that gap causes stockouts.
- **Reordering by feel.** No reorder point means restocking late and stocking out.
- **Overordering.** Burying cash and triggering long-term storage fees to feel safe.
- **Ignoring stranded inventory.** Units in the warehouse that are not even listed as
  sellable, earning nothing and costing storage.
- **Letting IPI drift.** A low IPI caps restock limits right when a product is taking off.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. 50 production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
