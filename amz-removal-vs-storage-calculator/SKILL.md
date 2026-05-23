---
name: amz-removal-vs-storage-calculator
description: >-
  Decide per SKU whether to remove, liquidate, dispose, or keep aging FBA
  inventory. Breaks the math: storage fees over the holding horizon vs removal
  fees vs recoverable resale value. Use when a user asks about aged inventory,
  long-term storage fees, removal orders, liquidation, or what to do with slow
  movers. Trigger phrases: "aged inventory", "long-term storage", "removal
  order", "liquidate", "slow movers", "dispose", "old stock". Works with zero
  tools. the user provides unit cost, age, storage rate, and current price.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Removal vs Storage Calculator

Aging FBA inventory bleeds money two ways: monthly storage and long-term storage
fees. The question is whether to keep, liquidate, remove, or dispose. The answer
depends on the per-SKU math, not gut feel. This skill runs that math.

## When to use this

- Units approaching the long-term storage threshold (180+ or 365 days).
- A slow mover that is not turning and is costing storage.
- Q4 prep where storage rates jump and aged stock costs more.
- April 2025 auto-removal rules in effect and the seller needs to decide.

## The framework. The Four Decisions

For each aging SKU, compute the dollar outcome of four options.

| Option | Math | Best when |
|--------|------|-----------|
| Keep and sell at full price | (price - fees - cost) x expected units sold - storage over horizon | Velocity supports sell-through before long-term fees hit |
| Liquidate (deep discount) | (sale price - fees - cost) x units - storage to clearance date | Sellable with a discount, recovers more than removal |
| Remove (back to seller or 3PL) | (resale or new sale price - removal fee - shipping) - storage to removal | Brand-controlled value off-Amazon, or relist later |
| Dispose (Amazon destroys) | -(disposal fee + lost cost) | No resale value and storage cost exceeds disposal fee |

The decision: the option with the highest dollar outcome (least negative) wins. for
many slow movers, dispose actually beats keep when factored over months.

## Step by step

1. **Collect inputs per SKU.** Units on hand, age, unit cost (landed), current
   selling price, recent units-per-month rate, monthly storage rate, and removal /
   disposal fee.

2. **Project the holding cost.** Storage over the realistic time-to-sell horizon,
   including the long-term storage fee if it triggers.

3. **Compute each option.** Plug into the four formulas.

4. **Pick the winner.** Highest dollar outcome.

5. **Sequence the action.** Submit removal or disposal orders before the next
   long-term storage fee charge. plan liquidation campaigns with `amz-coupon-strategy`
   or `amz-deal-finder`.

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
By: [date before next long-term fee charge]
```

## Worked example

200 units of a SKU at 8 USD landed cost, age 240 days, selling 4 a month, current
price 22 USD. Monthly storage 0.30 per cubic foot, unit volume 0.5 cu ft.

- Keep and sell at full price: 200 / 4 = 50 months to clear. Storage over 50 months
  = 200 x 0.5 x 0.30 x 50 = 1,500 USD. Margin per unit ~9 USD x 200 = 1,800. Net
  +300. but the long-term storage fee fires multiple times, eroding most of that.
- Liquidate at 14 USD via coupon: cleared in ~3 months. Margin ~2 USD x 200 = 400.
  Storage over 3 months ~90. Net +310.
- Remove and relist on a 3PL: removal fee 1.10 x 200 = 220. resale value uncertain.
  Net depends on the off-Amazon channel.
- Dispose: disposal fee 0.30 x 200 = 60 + lost cost 1,600 = -1,660.

Liquidate wins by a hair over Keep on math, and far better on cash and IPI. file a
coupon for the next 90 days.

## Quality check

- All four options are computed, not just two.
- The long-term storage fee is included in the holding cost projection.
- Time-to-sell uses the realistic recent rate, not the launch rate.
- The chosen action is tied to a specific date before the next long-term fee.
- The decision applies across the at-risk catalog, not one SKU in isolation.

## Common mistakes

- **Hoping it sells.** Holding aged stock at full price while storage fees
  compound.
- **Removing without checking liquidate.** Removal is sometimes worse than a deep
  Amazon discount.
- **Disposing too early.** Disposal is right when no other option recovers cost.
  often a brand-controlled remove-and-relist is better.
- **Missing the long-term storage fee date.** Acting after it charges instead of
  before.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
