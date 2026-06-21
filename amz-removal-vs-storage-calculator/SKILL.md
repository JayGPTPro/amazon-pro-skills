---
name: amz-removal-vs-storage-calculator
description: >-
  Decide per SKU whether to remove, liquidate, dispose, or keep aging FBA
  inventory. Breaks the math: base storage plus the monthly aged-inventory
  surcharge over the holding horizon vs removal fees vs recoverable resale value.
  Use when a user asks about aged inventory, aged-inventory surcharge, long-term
  storage fees, removal orders, liquidation, or what to do with slow
  movers. Trigger phrases: "aged inventory", "aged-inventory surcharge",
  "long-term storage", "removal order", "liquidate", "slow movers", "dispose",
  "old stock". Works with zero tools. the user provides unit cost, age, storage
  rate, and current price.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Removal vs Storage Calculator

Aging FBA inventory bleeds money two ways: base monthly storage and the aged-inventory
surcharge that stacks on top once the units get old. The question is whether to keep,
liquidate, remove, or dispose. The answer depends on the per-SKU math, not gut feel.
This skill runs that math.

## When to use this

- Units approaching or past the aged-inventory surcharge thresholds (it begins around
  181 days and gets steeper at 271+ and 365+ days).
- A slow mover that is not turning and is costing storage.
- Q4 prep where storage rates jump and aged stock costs more.
- April 2025 auto-removal rules in effect and the seller needs to decide.

## The framework. The Four Decisions

For each aging SKU, compute the dollar outcome of four options.

| Option | Math | Best when |
|--------|------|-----------|
| Keep and sell at full price | (price - fees - cost) x expected units sold - storage over horizon | Velocity supports sell-through before aged-inventory surcharges stack up |
| Liquidate (deep discount) | (sale price - fees - cost) x units - storage to clearance date | Sellable with a discount, recovers more than removal |
| Remove (back to seller or 3PL) | (resale or new sale price - removal fee - shipping) - storage to removal | Brand-controlled value off-Amazon, or relist later |
| Dispose (Amazon destroys) | -(disposal fee + lost cost) | No resale value and storage cost exceeds disposal fee |

The decision: the option with the highest dollar outcome (least negative) wins. for
many slow movers, dispose actually beats keep when factored over months.

## The aged-inventory surcharge (what makes old stock expensive)

The old "long-term storage fee at 180+ and 365 days" two-tier model is outdated. Since
2024 Amazon charges a monthly aged-inventory surcharge on a tiered scale that stacks on
top of the base monthly storage rate. The surcharge begins around 181 days and steps up
as the inventory ages, with steeper bands at 271+ days and again at 365+ days, charged
every month the units sit. Because it is monthly and rises with age, the cost of keeping
a slow mover compounds fast. check the current surcharge tiers in the Seller Central fee
schedule before quoting a number, and project the surcharge month by month across the
realistic time-to-sell horizon, not as a single one-time charge.

## Step by step

1. **Collect inputs per SKU.** Units on hand, age, unit cost (landed), current
   selling price, recent units-per-month rate, monthly storage rate, and removal /
   disposal fee.

2. **Project the holding cost.** Base monthly storage over the realistic time-to-sell
   horizon, plus the monthly aged-inventory surcharge for every month the units sit in
   a surcharge tier. check current surcharge tiers in the fee schedule.

3. **Compute each option.** Plug into the four formulas.

4. **Pick the winner.** Highest dollar outcome.

5. **Sequence the action.** Submit removal or disposal orders before the units cross
   into the next aged-inventory surcharge tier. plan liquidation campaigns with
   `amz-coupon-strategy` or `amz-deal-finder`.

6. **Apply across the aged catalog.** Run the calc on every SKU in the at-risk
   bucket. the decisions usually split: a few worth liquidating, several to
   remove, some to dispose.

7. **Run the quality check**, then deliver.

## Output format

```
## Removal vs Storage Decision. [SKU]

Units: [N]   Age: [days]   Unit cost: [$]   Price: [$]   Storage rate: [$/cubic ft]

### Option outcomes (per unit)
Keep and sell:  [$]
Liquidate:      [$]
Remove:         [$]
Dispose:        [$]

### Recommendation: [option]
[reasoning + dollar comparison]

### Action
[file removal order / set liquidation deal / dispose / hold]
By: [date before units cross into the next aged-inventory surcharge tier]
```

## Worked example

200 units of a SKU at 8 USD landed cost, age 240 days, selling 4 a month, current
price 22 USD. Standard size, unit volume 0.5 cu ft. Use a realistic 2026 standard-size
off-peak base storage rate of about 0.78 per cubic foot per month (use your current
per-cu-ft rate from the fee schedule). At 240 days the SKU is already in an aged-
inventory surcharge tier, and at this velocity it will climb into the steeper 271+ and
365+ bands while it sits.

- Keep and sell at full price: 200 / 4 = 50 months to clear. Base storage alone over 50
  months = 200 x 0.5 x 0.78 x 50 = 3,900 USD, before the monthly aged-inventory
  surcharge stacks on top and steepens with age. Margin per unit ~9 USD x 200 = 1,800.
  Net deeply negative once storage plus surcharge run the full horizon. keeping is a
  trap here.
- Liquidate at 14 USD via coupon: cleared in ~3 months. Margin ~2 USD x 200 = 400.
  Storage over 3 months ~234, plus a few months of surcharge. Net roughly breakeven to
  modestly positive, and the cash and IPI are freed fast.
- Remove and relist on a 3PL: removal fee ~1.10 x 200 = 220 (verify current removal
  rate). resale value uncertain. Net depends on the off-Amazon channel, but it stops
  the surcharge clock immediately.
- Dispose: disposal fee ~0.30 x 200 = 60 + lost cost 1,600 = -1,660 (verify current
  disposal rate).

Liquidate clearly beats Keep once the real base rate and the stacking surcharge are in
the math, and it is far better on cash and IPI. file a coupon for the next 90 days, and
do it before the units cross into the next surcharge tier.

## Quality check

- All four options are computed, not just two.
- The monthly aged-inventory surcharge is projected month by month across the horizon
  and stacked on top of base storage, with tiers marked for verification.
- Time-to-sell uses the realistic recent rate, not the launch rate.
- The chosen action is tied to a specific date before the next surcharge tier.
- The decision applies across the at-risk catalog, not one SKU in isolation.

## Common mistakes

- **Hoping it sells.** Holding aged stock at full price while storage fees
  compound.
- **Removing without checking liquidate.** Removal is sometimes worse than a deep
  Amazon discount.
- **Disposing too early.** Disposal is right when no other option recovers cost.
  often a brand-controlled remove-and-relist is better.
- **Missing the next surcharge tier date.** Acting after the aged-inventory surcharge
  steps up instead of before, and treating it as a one-time fee instead of a monthly
  charge that compounds with age.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
