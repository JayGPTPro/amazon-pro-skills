---
name: amz-inbound-placement-optimizer
description: >-
  Compare Amazon inbound shipment placement options (minimal-split vs Amazon-
  optimized split, partial-split, optional unified inventory) given SKU
  dimensions, units, and destination forecast. Returns the lowest landed cost
  per unit. Use when a user asks about STA (Send to Amazon), inbound placement
  fees, shipment splits, fulfillment center routing, or inbound shipping
  optimization. Trigger phrases: "STA", "inbound placement", "shipment split",
  "placement fee", "fulfillment center routing". Works with zero tools.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Inbound Placement Optimizer

Amazon's Send-to-Amazon inbound options charge different placement fees and produce
different in-stock speeds. The wrong choice on a single shipment can cost
$0.30 to $1.10 per unit. This skill compares the options and picks the lowest
landed cost.

## When to use this

- Preparing an inbound shipment and not sure which placement to choose.
- A past shipment cost more than expected and the seller suspects placement.
- Comparing Amazon-optimized routing vs minimal splits across recurring shipments.
- High-volume SKU where pennies per unit add up.

## The framework. The Placement Options

Amazon offers placement modes that trade off the seller's labor against placement
fees. Key options:

1. **Amazon-optimized split.** Amazon decides the destinations. lowest placement fee
   per unit, but the seller ships to multiple FCs.
2. **Partial-split.** Fewer destinations, moderate fee per unit.
3. **Minimal-split (single destination, where eligible).** One destination, but the
   highest per-unit placement fee, and not always available.
4. **Optional unified inventory (eligible categories).** Amazon distributes for the
   seller across regions.

The right option depends on three numbers: the per-unit placement fee Amazon
quotes, the seller's outbound shipping cost difference, and the speed-to-sellable
implication (slow placement = more days out of stock).

## Step by step

1. **Collect inputs.** SKU(s), units per shipment, current shipping cost per unit
   to each option Amazon offers, and the seller's own freight rate.

2. **Pull the placement quotes.** Amazon's STA flow shows the per-unit placement
   fee for each option for this specific shipment. Use those numbers.

3. **Compute total landed.** For each option: (Amazon placement fee + seller's
   freight to those destinations) x units. Compare total dollars per shipment, not
   per unit, because freight per unit varies by destination count.

4. **Factor speed.** Slower placement = days out of stock on the FCs Amazon would
   not have picked. For a fast-moving SKU, days-out-of-stock has a sales cost.

5. **Pick the lowest landed.** Often Amazon-optimized wins because Amazon's
   placement fees are designed to be cheaper than the seller's marginal freight.
   sometimes a partial split wins for SKUs with very low outbound cost.

6. **Repeat across the shipment plan.** Decision per shipment, not a fixed policy.

7. **Run the quality check**, then deliver.

## Output format

```
## Inbound Placement Decision. [shipment ID]

Units: [N]   SKU(s): [list]

### Options compared
1. Amazon-optimized split. Placement fee per unit: [$]. Outbound freight: [$]. Total: [$]
2. Partial-split. ...
3. Minimal-split. ...

### Winner: [option]
[reasoning + dollar comparison]

### Speed implication
[days to in-stock per option, sales-cost estimate if relevant]
```

## Worked example

A 1,000-unit shipment of a small standard SKU. Amazon-optimized split: $0.21 per
unit placement, $0.18 outbound = $0.39 total = $390. Partial-split: $0.48 placement,
$0.10 outbound = $0.58 total = $580. Minimal-split: $1.05 placement, $0.05 outbound
= $1.10 total = $1,100. Amazon-optimized wins by $190 over partial and $710 over
minimal. Speed: optimized 4 days in stock, partial 6 days, minimal 9 days. for a
20-units-a-day SKU, the 5-day difference between optimized and minimal also costs
roughly 100 units of lost sales. optimized wins on both axes.

## Quality check

- All available placement options are quoted from Amazon's STA flow, not estimated.
- Total landed is computed per option, including outbound freight.
- Speed to in-stock is factored, especially for fast-moving SKUs.
- The decision is per shipment, not a fixed policy.
- The math is dollars per shipment, not per unit (because freight scales by destinations).

## Common mistakes

- **Defaulting to minimal-split.** Sellers pick the single-destination option for
  convenience and pay $0.50-$0.90 more per unit.
- **Ignoring outbound freight.** Amazon-optimized has a placement fee but lower
  outbound freight per unit (the seller's carrier consolidates).
- **One-off thinking.** Picking once and applying to every shipment. each shipment
  gets its own quote.
- **Forgetting speed.** A slower placement can stockout a fast SKU and cost more in
  lost sales than the placement fee difference.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
