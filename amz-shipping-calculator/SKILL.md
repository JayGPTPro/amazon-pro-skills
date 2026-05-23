---
name: amz-shipping-calculator
description: >-
  Calculate Amazon shipping and fulfillment costs and compare FBA versus FBM.
  Covers FBA fulfillment fees by size tier, dimensional weight, monthly and
  long-term storage, inbound shipping to Amazon, and removal fees. Use when a
  user asks to calculate shipping or fulfillment costs, compare FBA and FBM,
  understand dimensional weight, estimate storage fees, or figure inbound
  shipping. Trigger phrases: "shipping calculator", "fulfillment cost", "FBA vs
  FBM", "dimensional weight", "storage fees", "inbound shipping", "removal
  fees". Works with zero tools. the user provides dimensions, weight, and rates.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Shipping Calculator

Fulfillment cost is the line that decides whether a product is worth selling, and the
one sellers estimate worst. This skill builds the full fulfillment picture and
settles the FBA versus FBM question with numbers.

## When to use this

- Working out the true fulfillment cost of a product.
- Deciding between FBA and FBM for a product.
- A product's fees feel high and the seller does not know which line to blame.
- Comparing two package designs or two product sizes by fulfillment cost.

## The framework. The Fulfillment Cost Stack

Fulfillment is not one fee. It is a stack, and FBA and FBM split it differently.

### The FBA stack

1. **Fulfillment fee.** Set by size tier and shipping weight. The fee jumps in steps
   as weight bands and size tiers are crossed.
2. **Dimensional weight.** Amazon charges on the greater of actual weight and
   dimensional weight. Dimensional weight equals length times width times height,
   divided by the dim divisor (currently 139 for most US FBA size tiers). A light but bulky product is billed on its volume, not
   its scale weight. this surprises sellers constantly.
3. **Monthly storage.** Cubic feet times the monthly rate, higher in Q4.
4. **Long-term storage.** An extra fee on units that have aged in the warehouse past
   the threshold.
5. **Inbound shipping.** The cost to ship inventory from the supplier or the seller
   to Amazon's warehouses. real, and often forgotten.
6. **Removal or disposal.** If units must be pulled back or destroyed.

### The FBM stack

1. **Pick, pack, and your own labor.**
2. **Outbound carrier cost** to the customer, on dimensional weight too.
3. **Packaging materials.**
4. **Storage** in your own space.
5. No FBA fee, but also no Prime badge unless on Seller-Fulfilled Prime, and a lower
   Buy Box score.

## FBA versus FBM

Compute the per-unit total for each stack and compare, but the decision is not cost
alone:

- **FBA usually wins** on small, light, fast-moving products. the Prime badge and the
  Buy Box advantage lift conversion enough to outweigh the fee.
- **FBM can win** on large, heavy, slow-moving, or low-margin products where the FBA
  fee and storage would dominate, and on oversize items.
- A product can also be **split**: FBA for the velocity and badge, FBM as overflow or
  for oversize variants.

## Step by step

1. **Collect inputs.** Product dimensions and weight, the dim divisor, units per
   inbound shipment, inbound shipping cost, expected monthly turnover, the category,
   and the seller's own FBM handling cost if relevant.

2. **Determine the size tier and the billable weight.** Billable weight is the
   greater of actual and dimensional weight. Flag if dimensional weight is the driver.

3. **Build the FBA stack.** All six lines, per unit.

4. **Build the FBM stack** if a comparison is wanted.

5. **Compare and recommend.** Per-unit total each way, plus the conversion and badge
   factor, not cost alone.

6. **Flag the levers.** If dimensional weight or a size-tier boundary is inflating
   the cost, note that a smaller or lighter package could move the product into a
   cheaper tier.

7. **Run the quality check**, then deliver.

## Output format

```
## Fulfillment Cost. [product]

Dimensions: [LxWxH]   Actual weight: [x]   Dimensional weight: [y]
Billable weight: [the greater]   Size tier: [tier]

### FBA stack (per unit)
Fulfillment fee, storage, long-term risk, inbound share, removal risk . total [$]

### FBM stack (per unit, if compared)
Pick/pack/labor, carrier, packaging, storage . total [$]

### Recommendation
[FBA / FBM / split] . [reasoning including badge and conversion]

### Cost levers
[dimensional-weight or tier-boundary flags]
```

## Worked example

A light but bulky product, a foam cushion. Actual weight 1 lb, but the box volume
gives a dimensional weight of 4 lb.

Billable weight is 4 lb, not 1. The FBA fulfillment fee is charged on the volume. The
seller had budgeted on the 1 lb scale weight and the real fee is far higher.
Recommendation: still FBA, the product is small-standard-ish and benefits from the
badge, but the cost lever is real. compressing the packaging to reduce the box volume
would lower the dimensional weight and the fee on every single unit sold.

## Quality check

- Billable weight is the greater of actual and dimensional weight, and it is stated.
- A product driven by dimensional weight is explicitly flagged.
- The full six-line FBA stack is built, including inbound shipping and storage.
- An FBA versus FBM comparison weighs the Prime badge and conversion, not just cost.
- Size-tier-boundary and dimensional-weight cost levers are surfaced.

## Common mistakes

- **Budgeting on scale weight.** A bulky light product is billed on volume. the real
  fee can be several times the guess.
- **Forgetting inbound shipping.** The cost to get inventory to Amazon is part of
  fulfillment and is routinely omitted.
- **FBA versus FBM on cost alone.** FBM can look cheaper while quietly costing the
  Prime badge, the Buy Box, and conversion.
- **Ignoring storage.** Especially Q4 storage and long-term storage on slow movers.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. 50 production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
