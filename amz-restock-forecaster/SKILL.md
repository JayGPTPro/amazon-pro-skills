---
name: amz-restock-forecaster
description: >-
  Forecast Amazon FBA restock schedule per SKU. Combines 90-day sales velocity,
  lead time, safety stock, ASIN-level restock limits, and seasonality to output
  a week-by-week reorder schedule that avoids both stockouts and storage
  penalties. Use when a user asks about restock planning, reorder schedule,
  ASIN restock limits, days of cover, or 90-day forecast. Trigger phrases:
  "restock", "reorder schedule", "forecast", "days of cover", "ASIN restock
  limit". Works with zero tools. the user provides recent sales and lead times.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Restock Forecaster

Restocking by feel produces stockouts and overstock at the same time. A proper
forecast looks at velocity, lead time variance, capacity limits, and seasonality
together. This skill builds the week-by-week schedule.

## When to use this

- The seller has been restocking by gut and getting it wrong both ways.
- ASIN-level restock limits reactivated and the seller needs to fit within them.
- Q4 ramp planning where seasonal demand multiplies and lead times often slip.
- A new SKU stabilizing and needing its first forecast.

## The framework. The Days-of-Cover Model

Two metrics govern the forecast: days of cover (DoC) on hand and the reorder point.

- **DoC = units on hand / daily sales rate.** Watch it daily.
- **Reorder point = (daily rate x total lead time) + safety stock.** Watch the
  threshold.

The safety stock buffer absorbs lead-time variance and demand spikes. For a SKU
with steady demand and reliable supply, 14 days. For volatile demand or unreliable
supply, 21-30 days.

The schedule: project DoC forward week by week. When projected DoC dips below the
reorder point's days-equivalent, order. Order quantity = target days of cover x
daily rate, capped by ASIN restock limit.

## Step by step

1. **Collect inputs.** Per SKU: units on hand, last 90 days of sales (daily rate),
   total lead time including FBA check-in, current ASIN restock limit, any known
   seasonal multiplier.

2. **Compute the baseline.** Daily rate, safety stock days, reorder point.

3. **Project week-by-week DoC** for the next 12 weeks. Apply the seasonal
   multiplier per week if a peak is in the window.

4. **Find each order point.** Week when DoC dips below the reorder point's
   days-equivalent.

5. **Set order quantity.** Target days of cover (typically 60-90), respecting the
   ASIN restock limit. If the limit is binding, the seller will run lean. plan to
   request limit increases via amz-ipi-recovery-plan.

6. **Add the seasonal pre-order.** For peak windows, order earlier and larger to
   land before the peak (see amz-seasonal-planning).

7. **Run the quality check**, then deliver.

## Output format

```
## Restock Forecast. [SKU]

Daily rate: [units]   Safety stock: [days]   Reorder point: [units]
Lead time total: [days]   Restock limit: [units]

### 12-week DoC projection
Week 1: [DoC]   Week 2: [DoC]   ...   Week 12: [DoC]

### Order schedule
PO 1. Place by [date]. Quantity: [units]. Arrives in stock: [date]
PO 2. ...

### Constraints
Restock limit binding: [yes/no, when]
Seasonal multiplier: [Nx in week X]
```

## Worked example

A SKU at 25 units a day, 50 days total lead time, 21-day safety stock, 60-day
target cover, restock limit 3,000 units. Reorder point: (25 x 50) + (25 x 21) =
1,775 units. Current on hand 2,200. DoC = 88 days. The reorder point hits at week
4. Order 1,500 units to bring cover to 60 days post-arrival. Restock limit not
binding at this order size. Pre-order for week 10 peak (3x multiplier) adds an
earlier larger PO at week 7. The schedule shows the seller exactly when to place
each PO and how much, with no stockout risk and no excess.

## Quality check

- Daily rate is computed from real recent sales, not historical average.
- Safety stock scales with the SKU's volatility.
- DoC is projected weekly, not as a snapshot.
- ASIN restock limit is included as a hard cap on order quantity.
- Seasonal pre-orders are placed early enough to land before the peak.

## Common mistakes

- **Reordering on a fixed cadence.** A monthly PO regardless of cover is wrong both
  ways: stockouts in fast weeks, overstock in slow.
- **Forgetting the FBA check-in leg.** Lead time is not 'until the freight arrives'
  but 'until units are sellable'.
- **Ignoring the restock limit.** Ordering 5,000 when the limit is 3,000 means 2,000
  units stuck or expensive to send via STA capacity.
- **No seasonal multiplier.** A baseline forecast through a peak guarantees a stockout.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
