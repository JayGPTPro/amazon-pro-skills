---
name: amz-exit-valuation-prep
description: >-
  Prepare an Amazon business for sale. Calculates SDE/EBITDA, applies a 2.5-4x
  multiplier band based on diversification, traffic mix, and IP, and builds a
  12-month pre-exit cleanup roadmap. Use when a user asks about selling their
  Amazon business, exit valuation, FBA business sale, aggregator valuation,
  SDE, or EBITDA multiplier. Trigger phrases: "exit", "sell my Amazon business",
  "valuation", "SDE", "EBITDA", "multiplier", "FBA acquisition", "aggregator".
  Works with zero tools.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Exit Valuation Prep

The aggregator boom is over. Sellers now have to do the prep work themselves to
sell well, often to private buyers or smaller acquirers. The multiplier is no
longer 5-6x. it is 2.5-4x for most brands, and the seller's prep work determines
where on that band you land. This skill builds the roadmap.

## When to use this

- Considering selling in the next 12-24 months.
- A broker has approached and the seller wants to know the realistic price.
- Cleaning up the business so it does not need a fire-sale.
- Building toward a target valuation.

## The framework. The Valuation Formula

```
Valuation = SDE (Seller's Discretionary Earnings) x Multiplier
```

**SDE** is annual profit + owner add-backs (salary, personal expenses run through
the business, one-time costs). Use TTM (trailing twelve months) SDE.

**Multiplier band**: 2.5-4x. The exact number depends on six factors. each one is
worth +/- 0.2-0.4x.

| Factor | Pushes multiplier up | Pushes down |
|--------|---------------------|-------------|
| Diversification | Multiple categories, multiple SKUs, multiple traffic sources | One hero SKU, one category |
| Traffic mix | Strong organic + off-Amazon | All paid, ad-dependent |
| IP and brand | Trademark + Brand Registry + own domain + social | No brand, no IP |
| Trajectory | Growing or stable | Declining last 6 months |
| Margins | Healthy net margin (15%+) | Thin (under 10%) |
| Owner involvement | Process-documented, runs without you | Owner is the operation |

## The 12-month roadmap

To shift up the multiplier band, work backward from sale date.

- **Months 1-3.** Clean the books. SDE add-backs documented. P&L reconciled.
- **Months 4-6.** Reduce single-SKU concentration. expand the catalog or grow
  underweight SKUs.
- **Months 7-9.** Diversify traffic. start off-Amazon (see amz-aeo-external-
  content and amz-attribution-campaign-planner).
- **Months 10-12.** Documented SOPs. owner extraction. the business runs without
  daily input. data room ready.

## Step by step

1. **Collect inputs.** TTM revenue, TTM net profit, owner add-backs, SKU
   concentration, traffic mix, IP status, growth rate, margin profile, owner
   hours-per-week.

2. **Compute SDE.** Net profit plus reasonable add-backs.

3. **Score the six factors.** Where is the brand on each.

4. **Land the multiplier.** Start at 3.0x and adjust +/- per factor.

5. **Project the valuation.** SDE x multiplier = expected price.

6. **Build the 12-month roadmap.** Target a higher multiplier by acting on the
   lowest-scoring factors first.

7. **Project the post-prep valuation.** What the business is worth after a year of
   prep, vs today.

8. **Run the quality check**, then deliver.

## Output format

```
## Exit Valuation Prep. [brand]

### TTM numbers
Revenue: [$]   Net profit: [$]   Add-backs: [$]   SDE: [$]

### Multiplier scorecard
1. Diversification: [score, factor adjustment]
2. Traffic mix: [score, adjustment]
3. IP and brand: ...
4. Trajectory: ...
5. Margins: ...
6. Owner involvement: ...

### Current multiplier: [X.Xx]
### Current valuation: [$]

### 12-month roadmap
Months 1-3: [actions]
Months 4-6: [actions]
Months 7-9: [actions]
Months 10-12: [actions]

### Projected post-prep multiplier: [X.Xx]
### Projected post-prep valuation: [$]
```

## Worked example

A brand at $2M TTM revenue, $300k net profit, $40k owner add-backs (salary, home
office, personal credit card on biz). SDE = $340k. Scorecard: heavy single-SKU
concentration (-0.3), all traffic from Amazon ads (-0.2), Trademark + Brand
Registry + domain (+0.2), stable growth (0), 14% net margin (0), owner involved
daily (-0.2). Start 3.0, adjusted: 2.5x. Current valuation: ~$850k.

Roadmap: expand from 1 hero to 4-5 SKUs across the category (lifts diversification
+0.3), start external content cluster (lifts traffic mix +0.2), document SOPs and
hire a VA to remove the owner from daily ops (+0.3). Projected post-prep multiplier:
3.3x. Projected valuation: ~1.12M. That is roughly 270k of value created by 12
months of prep work, on top of any organic SDE growth.

## Quality check

- SDE is computed with documented add-backs, not assumed.
- The six factors are each scored, not lumped.
- The 12-month roadmap acts on the lowest-scoring factor first.
- Both current and post-prep valuations are projected with the same method.
- The seller is not pushed to sell. the skill outputs what selling now would yield
  and what waiting and prepping would yield.

## Common mistakes

- **Selling without prep.** Taking the first offer at 2.5x when 12 months of work
  brings 3.5x.
- **Inflating SDE.** Add-backs that a buyer's due diligence will strip out.
- **Single hero SKU.** The biggest multiplier killer. one product = one risk =
  buyers discount.
- **All-Amazon traffic.** A buyer sees full Amazon dependency as a risk and pays less.
- **Owner-as-business.** If the brand falls apart without the owner, the buyer is
  not buying a business, they are buying a job.

This skill is general guidance, not financial or legal advice. A broker and a CPA
should be involved in any actual sale.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
