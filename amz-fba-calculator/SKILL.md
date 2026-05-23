---
name: amz-fba-calculator
description: >-
  Calculate the full Amazon FBA fee stack and the true net profit and margin for
  a product. Walks the referral fee, the FBA fulfillment fee by size tier and
  weight, monthly storage, and the optional cost lines, then returns net profit,
  net margin, and break-even ACoS. Use when a user asks to calculate FBA fees,
  profit per unit, net margin, break-even, whether a product is profitable, or
  to compare FBA versus FBM. Trigger phrases: "FBA calculator", "FBA fees",
  "profit per unit", "net margin", "break-even", "is this profitable". Works
  with zero tools. the user provides price, cost, dimensions, and weight.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# FBA Profit Calculator

Most sellers know their price and their unit cost and assume the gap is profit. It is
not. Amazon takes a referral fee, a fulfillment fee, and storage, and there are cost
lines sellers forget entirely. This skill builds the full stack and returns the real
number.

## When to use this

- Evaluating whether a product to source can actually be profitable.
- A product sells well but the bank balance does not grow and nobody knows why.
- Comparing FBA versus FBM, or comparing two product sizes or price points.
- Setting a price from a target margin instead of guessing.

## The framework. The FBA Fee Stack

Net profit per unit is price minus seven layers. Walk every layer. the forgotten ones
are where margin dies.

```
Selling price
  minus  Referral fee        (category percent of price, 6 to 20%+ by category, min ~0.30)
  minus  FBA fulfillment fee (by size tier and shipping weight)
  minus  Monthly storage     (per-unit share. cubic feet x rate, higher Oct to Dec)
  minus  Unit cost           (landed: factory price + freight + duty per unit)
  minus  Returns reserve     (return rate x cost of a returned unit)
  minus  Variable extras     (prep, inbound shipping to Amazon, long-term storage risk)
  minus  Promo and ads       (allocate a realistic per-unit ad cost)
  =      Net profit per unit
```

Net margin equals net profit divided by selling price. Break-even ACoS equals
contribution margin before ads, divided by price, as a percent. it is the most ads
can cost before the unit loses money.

## The size tiers that drive the fulfillment fee

The FBA fulfillment fee is set by size tier and shipping weight, not by price.

- **Small standard** and **large standard** cover most products. fee rises in steps
  with weight.
- **Bulky and oversize** tiers cost dramatically more. a product that crosses a tier
  boundary by one ounce or one inch can lose its entire margin.
- Always check which tier the dimensions and weight land in, and how close they are
  to the next tier up.

## Step by step

1. **Collect inputs.** Selling price, landed unit cost, product dimensions and
   weight, category, expected return rate, prep and inbound cost per unit, and a
   realistic per-unit ad cost. Ask one compact follow-up for missing pieces. If the
   user does not know fee rates, use current standard ranges and mark them with a
   warning symbol as estimates.

2. **Referral fee.** Apply the category percentage to the price. note the small
   minimum.

3. **Fulfillment fee.** Determine the size tier from dimensions and weight, then the
   fee for that tier and weight band. Flag if the product is within 10 percent of the
   next tier boundary.

4. **Storage.** Compute the unit volume in cubic feet, multiply by the monthly rate,
   and divide across expected monthly turnover for a per-unit share. note the Q4 rate
   is higher.

5. **Walk the rest of the stack.** Unit cost, returns reserve, variable extras, and
   the allocated ad cost.

6. **Compute the results.** Net profit per unit, net margin, and break-even ACoS.

7. **Run the quality check**, then deliver.

## Output format

```
## FBA Profit. [product]

Selling price: [$]

### Fee stack
Referral fee:        [-$]
FBA fulfillment fee: [-$]   (size tier: [tier])
Storage (per unit):  [-$]
Unit cost (landed):  [-$]
Returns reserve:     [-$]
Prep + inbound:      [-$]
Ad cost (allocated): [-$]

### Result
Net profit per unit: [$]
Net margin:          [%]
Break-even ACoS:     [%]

### Flags
[tier-boundary warnings, estimate warnings, thin-margin warnings]
```

## Worked example

Product at 29.99 USD, large standard, 1.2 lb shipping weight, landed cost 7.50.

Referral 15 percent is 4.50. Fulfillment fee for the tier and weight roughly 5.80.
Storage share roughly 0.20. Unit cost 7.50. Returns reserve roughly 0.45.
Prep and inbound roughly 0.90. Allocated ad cost 3.00.

Net profit per unit roughly 7.64. Net margin roughly 25 percent. Break-even ACoS
before ads roughly 35 percent. The product is healthy, but it sits close to a weight
band. adding heavier packaging could push the fulfillment fee up and cut margin.

## Quality check

- All seven stack layers are included. no missing storage, returns, or prep lines.
- The fulfillment fee is derived from size tier and weight, not from price.
- Any product within 10 percent of a tier boundary is flagged.
- Fee rates the user did not supply are marked as estimates with a warning symbol.
- Net margin and break-even ACoS are both reported, not only net profit.

## Common mistakes

- **Price minus cost equals profit.** Ignoring three Amazon fees and three cost lines.
- **Forgetting storage and returns.** Small per-unit numbers that quietly erase a
  thin margin.
- **Ignoring the size tier.** A product an inch into the next tier can be unprofitable
  while a nearly identical one is fine.
- **No ad cost in the math.** A unit that is profitable before ads can be a loss after.
- **Using off-season storage rates.** Q4 storage is far higher. a Q4 plan needs the
  Q4 rate.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. 50 production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
