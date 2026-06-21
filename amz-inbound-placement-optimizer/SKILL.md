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

Amazon's Inbound Placement Service Fee, in effect since March 1, 2024, charges
sellers a per-unit fee that depends on how many inbound locations they ship to. send
to more locations and the fee drops, often to zero. send to one and it is highest.
The wrong choice on a single shipment can cost roughly $0.30 or more per unit on
standard-size items, and well over a dollar per unit on larger ones. This skill
compares the split options and picks the lowest landed cost.

## When to use this

- Preparing an inbound shipment and not sure which placement to choose.
- A past shipment cost more than expected and the seller suspects placement.
- Comparing Amazon-optimized routing vs minimal splits across recurring shipments.
- High-volume SKU where pennies per unit add up.

## The framework. The Three Splits

Amazon's Send-to-Amazon flow offers three shipment-split options. they trade the
seller's own freight and labor against Amazon's placement fee, and they are named by
how many inbound locations the inventory goes to. More splits, lower placement fee.
Fewer splits, Amazon does the spreading and charges for it. The three splits, in
Amazon's own terminology:

1. **Amazon-Optimized Shipment Splits (four or more locations).** Amazon picks the
   destinations and the inventory goes to four+ locations. lowest placement fee, and
   for qualifying shipments it is free. the trade is that the seller ships to the
   most destinations.
2. **Partial Shipment Splits (two or three locations).** Inventory goes to two or
   three locations. a reduced per-unit placement fee, fewer destinations to ship to.
3. **Minimal Shipment Splits (single location).** The seller sends to one location
   and Amazon spreads the inventory across the network on the seller's behalf for the
   highest per-unit placement fee.

(Eligible sellers in some categories may also see managed or unified inventory
options. when offered, treat the same way. weigh Amazon's fee against the freight and
labor it removes.)

The right split depends on three numbers: the per-unit placement fee Amazon quotes
for each option, the seller's outbound freight cost difference across the destination
counts, and the speed-to-sellable implication (fewer-location splits can mean more
days out of stock at the locations Amazon would have spread into).

## Step by step

1. **Collect inputs.** SKU(s), units per shipment, current shipping cost per unit
   to each option Amazon offers, and the seller's own freight rate.

2. **Pull the placement quotes.** Amazon's Send-to-Amazon flow shows the per-unit
   placement fee for each of the three splits for this specific shipment. Use those
   numbers, not estimates. they vary by size tier, weight, and region.

3. **Compute total landed.** For each split: (Amazon placement fee + seller's own
   outbound freight to that number of destinations) x units. The tradeoff runs the
   two costs against each other. more destinations (Amazon-Optimized) means a lower
   or zero placement fee but higher outbound freight, since the seller's carrier
   ships to more places with less consolidation. one destination (Minimal) means the
   cheapest outbound freight but the highest placement fee. Compare total dollars per
   shipment, not per unit, because outbound freight per unit changes with the
   destination count.

4. **Factor speed.** With Minimal, Amazon receives at one location and then
   redistributes across the network, so full in-stock can lag. shipping the inventory
   directly to more locations can get it sellable across the network sooner. For a
   fast-moving SKU, days out of stock at the locations you did not seed has a sales
   cost.

5. **Pick the lowest landed.** Amazon-Optimized often wins because the placement fee
   it removes (frequently down to zero) outweighs the extra outbound freight,
   especially for light, low-cube units. Minimal can win when the seller's outbound
   freight to multiple destinations is expensive relative to the placement fee, for
   example heavy or bulky SKUs. Partial is the middle ground. run the numbers, do not
   assume.

6. **Repeat across the shipment plan.** Decision per shipment, not a fixed policy.

7. **Run the quality check**, then deliver.

## Output format

```
## Inbound Placement Decision. [shipment ID]

Units: [N]   SKU(s): [list]

### Splits compared
1. Amazon-Optimized (4+ locations). Placement fee/unit: [$]. Outbound freight/unit: [$]. Total: [$]
2. Partial (2-3 locations). ...
3. Minimal (single location). ...

### Winner: [option]
[reasoning + dollar comparison]

### Speed implication
[days to in-stock per option, sales-cost estimate if relevant]
```

## Worked example

A 1,000-unit shipment of a small standard SKU, all numbers pulled from the seller's
own Send-to-Amazon quote and carrier rates. Amazon-Optimized (4+ locations): $0.00
placement (qualifies for free), but $0.22 outbound freight because the carrier ships
to four destinations = $0.22 total = $220. Partial (2-3 locations): $0.16 placement,
$0.13 outbound = $0.29 total = $290. Minimal (single location): $0.30 placement,
$0.08 outbound (one cheap destination) = $0.38 total = $380. The placement fee Amazon
removes on the Optimized split more than covers the extra outbound freight, so
Amazon-Optimized wins by $70 over partial and $160 over minimal. Speed: shipping
directly to four locations seeds the network, roughly 4 days to broad in-stock,
versus partial 6 days and minimal 9 days while Amazon redistributes from the one
location. for a 20-units-a-day SKU, the 5-day gap between optimized and minimal also
costs roughly 100 units of lost sales. optimized wins on both axes here. for a heavy
or bulky SKU where shipping to four destinations is expensive, the outbound freight
can flip the result toward partial or minimal. always run the SKU's real numbers.

## Quality check

- All three splits are quoted from Amazon's Send-to-Amazon flow, not estimated.
- Total landed is computed per split, adding the seller's outbound freight to the
  placement fee, with the tradeoff (lower placement vs higher outbound at more
  destinations) made explicit.
- Speed to in-stock is factored, especially for fast-moving SKUs.
- The decision is per shipment, not a fixed policy.
- The math is dollars per shipment, not per unit (because outbound freight scales
  with the destination count).

## Common mistakes

- **Defaulting to Minimal Shipment Splits.** Sellers pick the single-location option
  for convenience and pay the highest placement fee per unit, often more than the
  outbound freight they saved.
- **Ignoring outbound freight.** Amazon-Optimized cuts or zeroes the placement fee
  but adds outbound freight, because the carrier now ships to four+ destinations.
  netting the two is the whole exercise. comparing placement fees alone is wrong.
- **One-off thinking.** Picking once and applying to every shipment. each shipment
  gets its own quote, and the quote varies by size, weight, and region.
- **Forgetting speed.** Minimal can stockout a fast SKU while Amazon redistributes
  from one location, costing more in lost sales than the freight it saved.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
