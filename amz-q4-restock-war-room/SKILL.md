---
name: amz-q4-restock-war-room
description: >-
  Builds a week-by-week Q4 restock plan from August through November with FBA
  inbound delay buffers, peak velocity multipliers, and FBM fallback triggers.
  Q4 is 30-40% of annual revenue and FBA receiving takes 2-3 weeks during peak.
  Standard restock math stocks out at the worst possible moment. Use when a user
  asks about Q4 planning, Black Friday inventory, or Prime Big Deal Days restock.
  Trigger phrases: "Q4 restock plan", "Black Friday inventory", "Prime Big Deal
  Days restock", "Christmas Amazon inventory", "FBM fallback for FBA". Works with
  zero tools.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Q4 Restock War Room

Q4 is where the year is won or lost. October through December delivers 30-40%
of annual revenue for most sellers. FBA receiving slows from 5 days to 14-21
days during peak. Container ports add another 7-10 days of unpredictability.
The standard "30-day cover" restock model breaks every Q4. A war-room plan
adds the right buffers and pre-stages FBM as a safety net. The cost of stocking
out on Black Friday is not just lost sales, it is permanent BSR damage that
takes 6-8 weeks to recover.

## When to use this

- August 1st, kicking off Q4 planning
- October cover check, deciding emergency air-freight or FBM
- A SKU is forecasted to peak 3x normal velocity in November
- Multiple SKUs sharing a container with mixed Q4 demand profiles

## The framework. The Q4 War-Room Plan

```
Q4 demand = (Last-year peak monthly velocity x YoY growth x 1.4 peak buffer)
Order quantity = Q4 demand + lead time cover + inbound delay buffer
```

### Inbound delay buffer by month received

| Receiving month | Buffer days to add |
|---|---|
| August | 0 |
| September | 7 |
| October | 14 |
| November | 14 |
| December | n/a (too late for FBA) |

### FBM fallback triggers

If FBA cover drops below 14 days by Nov 20, activate FBM:
- List FBM offer at +8% price (covers FBM fulfillment cost)
- Pre-stage 30 days of inventory at 3PL or home
- Switch buy box back to FBA when restock arrives

### Peak velocity multipliers (vs Q3 baseline)

Event dates move every year. Confirm the current-year dates in Seller Central
and map each multiplier to the right week.

| Event | Velocity multiplier |
|---|---|
| Prime Big Deal Days (early-to-mid October, confirm yearly) | 1.8x baseline for that week |
| Black Friday week | 2.5-3.5x baseline |
| Cyber Monday | 2.0x baseline |
| Early December (Christmas push) | 1.6x baseline |
| Late December (last-mile rush) | 0.9x (shipping cutoffs and carrier capacity throttle late-arriving orders) |

## Step by step

1. **Pull last year's Q4 sales by SKU by week.** Business Reports. Note the
   weekly peak.

2. **Apply YoY growth assumption.** Use trailing 90-day YoY for the same SKU.
   Default 1.15x if no data.

3. **Apply 1.4x peak buffer.** Q4 is more volatile than Q3, undershoot kills.

4. **Calculate inbound delay buffer per month.** Add to lead time per the table.

5. **Build the reorder calendar.** Confirm the current-year event dates first,
   then place PO dates so units land at FBA with cover ahead of each event:
   - about 1 week before the fall Prime event (early-to-mid October, confirm yearly)
   - about 3 weeks before Black Friday
   - by late November for early-December coverage

6. **Set the FBM trigger thresholds.** For each SKU, calculate the FBA-cover
   day count that triggers FBM activation. Pre-stage FBM inventory by Nov 1.

7. **Build the dashboard.** Weekly check-in: FBA cover days, sell-through rate
   vs forecast, time-to-FBM-trigger.

8. **Run the quality check**, then circulate to ops and finance.

## Output format

```
## Q4 War Room Plan. [Account]

**Per-SKU summary**
SKU | Last-yr peak/wk | YoY growth | Buffered Q4 demand | FBM trigger day
[rows]

**Reorder calendar**
Week of [date] | SKU | Order qty | PO ship date | Expected receive date
[rows for August through November]

**FBM fallback inventory**
SKU | FBM units to pre-stage | Location | Activation trigger
[rows]

**Weekly check-in metrics**
- FBA cover days (target: >= 21)
- Sell-through vs forecast (target: 90-110%)
- Days to FBM trigger (alarm if <= 7)
```

## Worked example

SKU: pet brush, last-year Nov peak = 320 units/week. YoY growth = 1.22x. Peak
buffer 1.4x. Q4 weekly peak forecast = 320 x 1.22 x 1.4 = 547 units/week.
November total Q4 demand = 4 weeks x 547 = 2,188 units.

Lead time supplier ship to FBA = 35 days normal. November receiving buffer
adds 14 days. Total lead time = 49 days. PO must ship by Sept 12 to land at
FBA by Nov 1.

FBM trigger: at peak 547 units/week, 14-day cover = 1,094 units. When FBA
inventory drops below 1,094 units after Nov 20, list FBM offer. Pre-stage
600 units (30 days FBM cover) at 3PL by Nov 1. Cost: 600 x $2.40 storage =
$1,440 insurance against $0 stockout. Worth it.

Skipping this plan = stockout Nov 26 historical pattern = 4 days dark = 4 x
547 x $9 margin = $19,692 lost plus 6-8 weeks BSR recovery.

## Quality check

- Last-year data is week-level, not month-level (smoothing hides peaks)
- YoY growth uses trailing 90 days, not full-year average
- Inbound buffer aligned to receive month, not ship month
- FBM trigger numerically defined per SKU, not "we will watch it"
- Reorder calendar shows PO ship dates, not just receive dates

## Common mistakes

- **Using 30-day cover.** Standard restock formula. Stocks out in Q4 every time.
- **Ignoring receiving delays.** FBA appointment slots fill up Oct-Dec. Plan adds 14 days.
- **No FBM fallback.** When FBA stocks out without FBM, BSR collapses. Recovery is 6+ weeks.
- **Forecasting in months, not weeks.** A monthly forecast hides the 3x Black Friday week spike.
- **One YoY growth number for all SKUs.** Seasonal SKUs grow 2x, evergreen 1.1x. Forecast per SKU.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
