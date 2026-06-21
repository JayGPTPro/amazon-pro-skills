---
name: amz-fba-calculator
description: >-
  Calculate the full Amazon FBA fee stack and the true net profit and margin for
  a product, and compare FBA versus FBM on cost. Walks the referral fee, the
  FBA fulfillment fee by size tier and weight, dimensional weight, monthly and
  Q4 storage, long-term storage risk, inbound shipping, removal fees, and the
  optional cost lines, then returns net profit, net margin, and break-even
  ACoS. Use when a user asks to calculate FBA fees, profit per unit, net
  margin, break-even, whether a product is profitable, fulfillment cost,
  shipping cost, dimensional weight, storage fees, inbound shipping, removal
  fees, or to compare FBA versus FBM. Trigger phrases. "FBA calculator", "FBA
  fees", "profit per unit", "net margin", "break-even", "is this profitable",
  "shipping calculator", "fulfillment cost", "FBA vs FBM", "dimensional
  weight", "storage fees", "inbound shipping", "removal fees". Works with zero
  tools. the user provides price, cost, dimensions, weight, and rates.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# FBA Profit Calculator

Most sellers know their price and their unit cost and assume the gap is profit. It is
not. Amazon takes a referral fee, a fulfillment fee, and storage, dimensional weight
can blow up the shipping line on a light-but-bulky product, and there are cost lines
sellers forget entirely. This skill builds the full stack and returns the real
number, and settles the FBA versus FBM question with cost evidence.

## When to use this

- Evaluating whether a product to source can actually be profitable.
- A product sells well but the bank balance does not grow and nobody knows why.
- Comparing FBA versus FBM, or comparing two product sizes or price points.
- Setting a price from a target margin instead of guessing.
- A product's fees feel high and the seller does not know which line to blame.
- Comparing two package designs by fulfillment cost.

## The framework. The FBA Fee Stack

Net profit per unit is price minus seven layers. Walk every layer. the forgotten ones
are where margin dies.

```
Selling price
  minus  Referral fee        (category percent of price, 6 to 20%+ by category, min ~0.30)
  minus  FBA fulfillment fee (by size tier and billable weight, see shipping layer)
  minus  Returns processing  (per-returned-unit in high-return-rate categories, see below)
  minus  Monthly storage     (per-unit share. cubic feet x rate, higher Oct to Dec)
  minus  Unit cost           (landed: factory price + freight + duty per unit)
  minus  Returns reserve     (return rate x cost of a returned unit)
  minus  Variable extras     (prep, inbound shipping to Amazon, aged-inventory risk)
  minus  Promo and ads       (allocate a realistic per-unit ad cost)
  =      Net profit per unit
```

Net margin equals net profit divided by selling price. Break-even ACoS equals
contribution margin before ads, divided by price, as a percent. it is the most ads
can cost before the unit loses money.

## The size tiers that drive the fulfillment fee

The FBA fulfillment fee is set by size tier and billable weight, not by price.

- **Small standard** and **large standard** cover most products. fee rises in steps
  with weight.
- **Bulky and oversize** tiers cost dramatically more. a product that crosses a tier
  boundary by one ounce or one inch can lose its entire margin.
- Always check which tier the dimensions and weight land in, and how close they are
  to the next tier up.

## Shipping cost layer

The shipping side of the FBA fee has three components that move it around
independent of price. Walk them before quoting a fulfillment number.

### Dimensional weight

Amazon charges on the greater of actual weight and dimensional weight. Dimensional
weight equals length times width times height, divided by the dim divisor (currently
139 for most US FBA size tiers, verify in Seller Central before quoting). A light
but bulky product is billed on its volume, not its scale weight. this surprises
sellers constantly. Always state both numbers and the billable one.

### Oversize tier surcharges

The fulfillment fee step between large standard and the oversize tiers is large,
and the oversize tier itself has internal bands (small, medium, large, special).
Crossing into oversize by a single dimension can multiply the fee. always confirm
which oversize band the longest side, the girth, and the unit weight produce.

### Peak surcharges and inbound

Q4 carries a peak fulfillment surcharge on top of the standard fulfillment fee,
distinct from the elevated Q4 storage rate. Inbound shipping from the supplier or
the seller to the Amazon warehouse is part of the unit's real fulfillment cost and
is routinely forgotten. add the per-unit share of inbound.

### Returns Processing Fee

Amazon adds a Returns Processing Fee per returned unit for high-return-rate
categories. Apparel and shoes have long been charged on every returned unit, and the
fee now reaches many other categories whose return rate runs above the category
benchmark. The charge is added per returned unit for high-return-rate categories.
check your category's rate in the current fee schedule. On a product with a meaningful
return rate this is a real per-sold-unit cost once spread across units sold, not just
across units returned. fold it into the returns line rather than ignoring it. Low-
volume products (below the monthly unit threshold) may be exempt. verify your status.

## FBA versus FBM

When the seller is choosing fulfillment model, compute the per-unit total each way.
The decision is not cost alone.

The FBM stack: pick/pack/labor, outbound carrier cost (also charged on dimensional
weight), packaging materials, your own storage, no FBA fee, no Prime badge unless on
Seller-Fulfilled Prime, lower Buy Box score.

- **FBA usually wins** on small, light, fast-moving products. the Prime badge and the
  Buy Box advantage lift conversion enough to outweigh the fee.
- **FBM can win** on large, heavy, slow-moving, or low-margin products where the FBA
  fee and storage would dominate, and on oversize items.
- A product can also be **split**: FBA for the velocity and badge, FBM as overflow or
  for oversize variants.

## A note on rates and reimbursement (2025+ rules)

Amazon's fee rates change each year. Quote the current Jan-Sep monthly storage rate
per cubic foot for the off-peak window and the Oct-Dec rate for Q4, then have the
seller verify both in the Seller Central fee schedule before final pricing. The
same applies to the FBA fulfillment fee bands and the Q4 peak surcharge. mark every
unverified rate with a warning symbol as an estimate.

Reimbursement policy changed in 2025. Amazon now reimburses lost or damaged
inventory based on the manufacturing cost the seller provides, not on retail price.
If the seller does not supply a manufacturing cost, Amazon uses a default that is
typically lower than retail. for accurate returns and shrinkage modeling, set the
manufacturing cost in Seller Central and use it as the returns-reserve baseline,
not the selling price.

## Step by step

1. **Collect inputs.** Selling price, landed unit cost, product dimensions and
   weight, category, expected return rate, prep and inbound cost per unit, units
   per inbound shipment, expected monthly turnover, the dim divisor, and a
   realistic per-unit ad cost. Ask one compact follow-up for missing pieces. If the
   user does not know fee rates, use current ranges and mark them with a warning
   symbol as estimates to verify in the dashboard.

2. **Referral fee.** Apply the category percentage to the price. note the small
   minimum.

3. **Billable weight and size tier.** Compute actual weight and dimensional weight,
   take the greater as billable. Determine the size tier. Flag if the product is
   within 10 percent of the next tier boundary or if dimensional weight is the
   driver.

4. **Fulfillment fee.** Look up the fee for the tier and billable weight. Add the
   Q4 peak surcharge if the plan covers Q4. If the category is high-return-rate
   (apparel, shoes, and others over the benchmark), add the Returns Processing Fee
   per returned unit, spread across units sold. verify the rate in the fee schedule.

5. **Storage.** Compute the unit volume in cubic feet. Use the current Jan-Sep
   monthly rate for off-peak and the current Oct-Dec rate for Q4 (verify in
   dashboard). Divide across expected monthly turnover for a per-unit share. Add a
   long-term storage risk reserve for slow movers.

6. **Inbound and removal.** Add the per-unit share of inbound shipping to Amazon.
   Reserve a small line for removal or disposal risk if the product is slow.

7. **Walk the rest of the stack.** Unit cost, returns reserve (use the
   manufacturing cost in the reimbursement baseline), and the allocated ad cost.

8. **If a model comparison is wanted, build the FBM stack.** Then compare per-unit
   totals plus the conversion and badge factor.

9. **Compute the results.** Net profit per unit, net margin, and break-even ACoS.

10. **Flag the levers.** If dimensional weight or a size-tier boundary is inflating
    the cost, note that a smaller or lighter package could move the product into a
    cheaper tier.

11. **Run the quality check**, then deliver.

## Output format

```
## FBA Profit. [product]

Selling price: [$]
Dimensions: [LxWxH]   Actual weight: [x]   Dimensional weight: [y]
Billable weight: [the greater]   Size tier: [tier]

### Fee stack
Referral fee:        [-$]
FBA fulfillment fee: [-$]   (size tier: [tier], billable weight: [w])
Q4 peak surcharge:   [-$]   (if Q4 plan)
Returns processing:  [-$]   (per returned unit, high-return-rate category, verify rate)
Storage (per unit):  [-$]   (rate band: [Jan-Sep / Oct-Dec], verify in dashboard)
Unit cost (landed):  [-$]
Returns reserve:     [-$]   (based on manufacturing cost, 2025+ rule)
Prep + inbound:      [-$]
Aged-inventory risk: [-$]
Ad cost (allocated): [-$]

### FBM comparison (if requested)
Pick/pack/labor, carrier, packaging, storage . total [$]
Recommendation: [FBA / FBM / split] . [reasoning including badge and conversion]

### Result
Net profit per unit: [$]
Net margin:          [%]
Break-even ACoS:     [%]

### Flags and cost levers
[tier-boundary warnings, dimensional-weight driver, estimate warnings, thin-margin
warnings, packaging-compression opportunities]
```

## Worked example

Product at 29.99 USD, large standard, 1.2 lb actual weight, dimensional weight 1.4
lb, landed cost 7.50.

Referral 15 percent is 4.50. Billable weight is 1.4 lb (dimensional drives).
Fulfillment fee for the tier and band roughly 5.80. Storage share roughly 0.20 at
the off-peak rate (verify in dashboard). Unit cost 7.50. Returns reserve roughly
0.45, baselined against the manufacturing cost not retail. Prep and inbound roughly
0.90. Allocated ad cost 3.00.

Net profit per unit roughly 7.64. Net margin roughly 25 percent. Break-even ACoS
before ads roughly 35 percent. The product is healthy, but dimensional weight is
the driver. compressing the packaging to lower the box volume would shrink the
billable weight and the fee on every single unit sold. The product also sits within
10 percent of a tier boundary. heavier holiday packaging could push it up. plan Q4
packaging accordingly.

## Quality check

- All seven stack layers are included. no missing storage, returns, or prep lines.
- Billable weight is the greater of actual and dimensional weight, and it is stated.
- A product driven by dimensional weight is explicitly flagged.
- The fulfillment fee is derived from size tier and billable weight, not from price.
- A high-return-rate category includes the Returns Processing Fee per returned unit,
  with the rate marked for verification rather than hardcoded.
- Any product within 10 percent of a tier boundary is flagged.
- Storage uses the current Jan-Sep or Oct-Dec rate band, marked as a dashboard
  verification, not a hardcoded number.
- Returns reserve is anchored to manufacturing cost (2025+ reimbursement rule).
- Fee rates the user did not supply are marked as estimates with a warning symbol.
- Net margin and break-even ACoS are both reported, not only net profit.
- If FBM is in scope, the comparison weighs the Prime badge and conversion, not just
  cost.

## Common mistakes

- **Price minus cost equals profit.** Ignoring three Amazon fees and three cost lines.
- **Forgetting storage and returns.** Small per-unit numbers that quietly erase a
  thin margin.
- **Budgeting on scale weight.** A bulky light product is billed on volume. the real
  fee can be several times the guess.
- **Ignoring the size tier.** A product an inch into the next tier can be unprofitable
  while a nearly identical one is fine.
- **Forgetting inbound shipping.** The cost to get inventory to Amazon is part of
  fulfillment and is routinely omitted.
- **No ad cost in the math.** A unit that is profitable before ads can be a loss after.
- **Using off-season storage rates for Q4.** Q4 storage is far higher. a Q4 plan
  needs the Q4 rate.
- **Quoting retail for reimbursement.** Under the 2025+ rule, reimbursement is on
  manufacturing cost, not retail. Set it in Seller Central or accept Amazon's
  default.
- **FBA versus FBM on cost alone.** FBM can look cheaper while quietly costing the
  Prime badge, the Buy Box, and conversion.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
