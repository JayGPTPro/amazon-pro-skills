---
name: amz-tacos-diagnostic
description: >-
  Diagnose whether a seller is stuck in the "ACoS trap" by reading ACoS, TACoS,
  organic rank, and conversion trends together. Identifies whether bid cuts
  are killing organic sales and outputs a rebalancing plan. Use when a user
  asks about TACoS, ACoS trap, ads cannibalizing organic, organic rank
  dropping, or rebalancing ad spend. Trigger phrases: "TACoS", "ACoS trap",
  "ad cannibalization", "organic rank dropping", "ad spend rebalance". Works
  with zero tools. the user pastes trend data.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# TACoS Diagnostic

The "ACoS trap" is the most common 2025 PPC mistake. ACoS looks fine, but TACoS is
climbing, organic rank is falling, and total profit is shrinking. The seller is
cutting bids on winning keywords and watching organic sales fall with them. This
skill diagnoses the pattern and rebalances.

## When to use this

- ACoS is acceptable but total profit is shrinking.
- Organic rank has been sliding for a few weeks.
- Sales feel flat but ad spend keeps rising.
- The seller cut bids to "improve ACoS" and noticed organic dropped too.

## The framework. The 4-Quadrant Diagnostic

Plot the trend of ACoS vs TACoS over the past 8-12 weeks.

| Quadrant | ACoS | TACoS | Diagnosis |
|----------|------|-------|-----------|
| Healthy | flat | flat | Organic is carrying. Ads are layering. Keep going |
| Trap | flat | rising | Ads replacing organic. Bid cuts hurt rank |
| Recovering | falling | falling | Strong organic, ads efficient |
| Crisis | rising | rising | Both bleeding. listing or product issue |

The trap is the most insidious because ACoS looks fine. you only catch it by
watching TACoS together.

## Step by step

1. **Collect inputs.** Weekly ACoS, TACoS, ad spend, total sales, organic
   conversion rate, and organic rank on the 5-15 money keywords (see
   amz-rank-tracker).

2. **Plot the trends.** Look at the 4-week and 12-week direction of each metric.

3. **Place the account on the quadrant grid.**

4. **If in the Trap:** identify the specific keywords where bids were cut. usually
   exact-match keywords on the harvest layer. The fix is restoring those bids and
   accepting a slightly higher ACoS for a healthier TACoS.

5. **If in Crisis:** the listing or product is the issue, not the ads. route to
   amz-listing-optimization, amz-search-optimization, or amz-buy-box.

6. **Set the rebalancing plan.** Specific bid changes per keyword tier. Test a
   targeted budget shift, do not flip everything at once.

7. **Watch TACoS as the lead metric** going forward, not ACoS alone.

8. **Run the quality check**, then deliver.

## Output format

```
## TACoS Diagnostic. [account]

### Trends (12 weeks)
ACoS: [direction]
TACoS: [direction]
Organic rank: [direction]
Total profit: [direction]

### Quadrant: [Healthy / Trap / Recovering / Crisis]

### If Trap
Keywords where bids were cut: [list]
Restoration plan: [specific bid changes]

### If Crisis
Route to: [listing/SEO/Buy Box skills]

### Going forward
Lead metric: TACoS (not ACoS alone)
Review cadence: weekly
```

## Worked example

12 weeks: ACoS held at 22%, TACoS climbed from 9% to 16%, organic rank slipped on
3 money keywords from page-1 to page-3. Quadrant: Trap. Diagnosis: exact-match bids
were cut over the past 2 months in pursuit of ACoS improvement. Without the ad
budget those keywords used to win, organic rank trailed because Amazon stopped
seeing the velocity. Plan: restore bids on those 3 exact-match keywords, accept
ACoS climbing to ~26% on them, watch TACoS pull back as organic recovers. Within
4 weeks TACoS should drop back below 12% and organic rank returns.

## Quality check

- Both ACoS and TACoS trends are read, not just ACoS.
- The quadrant placement is named, not inferred.
- Trap diagnosis identifies the specific keywords cut, not vague.
- Crisis is correctly routed to listing/SEO/Buy Box skills, not treated as a bid
  problem.
- TACoS is set as the lead metric going forward, not ACoS.

## Common mistakes

- **Optimizing ACoS in isolation.** The classic trap.
- **Cutting bids on proven keywords.** Save ACoS by cutting Harvest spend and lose
  organic rank as a side effect.
- **Treating Crisis as a PPC issue.** Both metrics rising means the listing or
  product is failing, not the ads.
- **Watching one metric.** ACoS, TACoS, organic rank, and total profit move together.
  watch them as a system.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
