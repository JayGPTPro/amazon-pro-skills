---
name: amz-fba-prep
description: >-
  Prepare an FBA shipment correctly so it is not rejected, delayed, or charged
  prep fees at the warehouse. Covers labeling, polybagging, suffocation warnings,
  bundle and set prep, expiration dating, box weight and dimension limits, and
  the shipment plan itself. Use when a user asks about FBA prep, shipping
  inventory to Amazon, labeling units, polybag requirements, prep requirements,
  a shipment that was rejected, or unplanned prep fees. Trigger phrases: "FBA
  prep", "ship to Amazon", "FBA labeling", "polybag", "shipment plan", "prep
  requirements", "shipment rejected". Works with zero tools.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# FBA Prep Compliance

A rejected or mis-prepped FBA shipment costs money twice: the prep fee Amazon charges
to fix it, and the days the inventory sits unsellable. Almost every prep failure is
one of a short list of known mistakes. This skill walks the prep so the shipment
arrives clean.

## When to use this

- Preparing the first FBA shipment of a new product.
- A past shipment was rejected or hit with unplanned prep fees.
- Shipping a fragile, liquid, sharp, adult, or expiration-dated product.
- Sending bundles, multipacks, or sets and unsure how to prep them.

## The framework. The Prep Gate Checklist

A shipment passes the warehouse when it clears six gates. Walk them in order before
anything is boxed.

1. **Unit labeling.** Every unit needs a scannable FNSKU label, or the product must
   be enrolled in stickerless commingled inventory. The label must cover any existing
   barcode so only one scans. A double-scannable unit is a prep failure.

2. **Packaging integrity.** Each unit must survive a 3-foot drop and handling. Loose,
   open, or fragile units need a polybag, bubble wrap, or a box.

3. **Polybag rules.** A polybag must be transparent, sealed, and at least 1.5 mil
   thick. If the bag is 5 inches or larger on any side, it must carry a printed
   suffocation warning at the required font size. The barcode must be scannable
   through or on the bag.

4. **Special handling.** Liquids, glass, sharp items, and adult products have extra
   requirements. expiration-dated and consumable goods must show a legible date and
   meet the remaining-shelf-life rule.

5. **Sets and bundles.** A multipack or set must be marked "sold as set" or "do not
   separate" so the warehouse keeps it as one sellable unit.

6. **Box and shipment limits.** Standard cartons stay within the 50 lb (22.6 kg)
   limit. heavier cartons need a "team lift" or oversize marking, and the absolute
   ceiling is around 150 lb. Apply markings where required. The
   shipment plan, box content, and carton labels must match what is inside.

## Step by step

1. **Collect inputs.** The product, its fragility and category, whether it is a
   bundle or set, whether it has an expiration date, the units per box, and the box
   weight and dimensions.

2. **Walk the six gates.** For each gate, state the requirement for this specific
   product and whether it is met or what to fix.

3. **Flag the fee risk.** Name where Amazon would charge a prep fee or reject the
   shipment if a gate fails, so the seller fixes it before shipping, not after.

4. **Build the shipment plan checklist.** FNSKU labels printed and applied, box
   content information accurate, carton labels on every box, weight and dimension
   markings correct.

5. **Decide self-prep or Amazon prep.** If the seller cannot meet a gate, Amazon prep
   or a third-party prep center is the route. price it against doing it right at the
   source.

6. **Run the quality check**, then deliver.

## Output format

```
## FBA Prep Plan. [product]

### Six-gate check
1. Unit labeling: [requirement] . [met / fix]
2. Packaging integrity: ...
3. Polybag rules: ...
4. Special handling: ...
5. Sets and bundles: ...
6. Box and shipment limits: ...

### Fee and rejection risks
[where a fee or rejection would hit if unfixed]

### Shipment checklist
[ ] FNSKU labels applied, old barcodes covered
[ ] Box content information matches
[ ] Carton labels on every box
[ ] Weight and oversize markings applied
```

## Worked example

A glass candle, sold as a 2-pack.

Gate 1: each 2-pack gets one FNSKU label, not one per candle. Gate 2 and 3: glass,
so each pack is bubble-wrapped and bagged. Gate 5: the pack is marked "sold as set,
do not separate" or the warehouse may split it. Gate 6: the master carton stays
under the weight limit and carries a glass and this-way-up marking. Miss Gate 5 and
Amazon sells the candles as singles and the listing breaks.

## Quality check

- All six gates are walked for this specific product, not a generic list.
- Unit labeling explicitly covers the old barcode so only one scans.
- Polybag suffocation-warning rule is applied when the opening is 5 inches or larger.
- Bundles and sets are marked so the warehouse keeps them as one unit.
- Fee and rejection risks are named before shipping.

## Common mistakes

- **Double barcodes.** Leaving the manufacturer barcode visible next to the FNSKU.
  two scannable codes are a prep failure.
- **Missing suffocation warnings.** The most common polybag rejection.
- **Unmarked sets.** The warehouse separates a bundle into singles and the listing
  becomes unsellable.
- **Overweight boxes.** A carton over the limit gets refused or surcharged.
- **Mismatched box content.** The plan says one thing, the box holds another. delays
  and reconciliation problems.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
