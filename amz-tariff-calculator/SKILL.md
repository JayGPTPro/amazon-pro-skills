---
name: amz-tariff-calculator
description: >-
  Calculate import tariffs, duties, and landed cost for products imported to
  sell on Amazon. Covers HS code classification, duty rates, additional tariffs,
  freight and customs fees, and the true per-unit landed cost. Use when a user
  asks about import tariffs, customs duty, landed cost, HS codes, import taxes,
  duty rates, or the cost of importing a product. Trigger phrases: "tariff",
  "import duty", "customs", "landed cost", "HS code", "import tax", "duty
  rate", "cost to import". Works with zero tools. the user provides the product,
  the route, and the costs.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Tariff and Landed Cost Calculator

The factory price is not the cost of the product. By the time a unit reaches an
Amazon warehouse it has carried freight, duty, additional tariffs, and customs fees.
Sellers who plan on the factory price discover the real margin too late. This skill
builds the true landed cost.

## When to use this

- Sourcing an imported product and needing the real per-unit cost.
- A product's margin came in lower than planned and import costs are suspected.
- Comparing two sourcing countries or two routes.
- Quoting a landed cost before committing to a supplier.

## The framework. The Landed Cost Stack

Landed cost per unit is the factory price plus six layers. Walk all of them.

```
Factory price per unit (EXW or FOB)
  plus  Freight           (ocean or air, per unit = shipment freight / units)
  plus  Import duty       (HS code duty rate x customs value)
  plus  Additional tariffs (trade-remedy or country-specific tariffs, if any)
  plus  Customs fees      (entry / processing / harbor or handling fees)
  plus  Insurance         (cargo insurance, small but real)
  plus  Inland and broker (port-to-warehouse trucking, customs broker fee)
  =     Landed cost per unit
```

This landed cost is the number that feeds every margin calculation. amz-fba-calculator
and amz-profit-analyzer both need it. A profit analysis built on the factory price is
wrong from the first line.

## The HS code. the line that decides the duty

The duty rate is set by the product's HS code (Harmonized System classification).
Get the code wrong and the duty is wrong, and a customs misclassification can mean
penalties.

- The HS code is determined by what the product is and what it is made of.
- A small difference in materials or function can move the product to a different
  code with a very different duty rate.
- When the code is uncertain, treat the duty as an estimate, mark it, and recommend
  confirming the classification with a customs broker before relying on the number.

## Additional tariffs

Beyond the base duty, some products from some countries carry extra trade-remedy or
country-specific tariffs that can be larger than the base duty itself. These change
with trade policy. Always check whether the specific product and origin country
carry an additional tariff on top of the base rate, and treat policy-dependent rates
as estimates.

Note on low-value shipments: the Section 321 / $800 de minimis exemption that once
let low-value parcels enter duty-free has been suspended (for China-origin goods
first, then broadened across origins), so small shipments that used to clear free
can now owe the full duty stack. Confirm the current status and scope before
relying on it, this area is policy-dependent and has been in flux.

## Step by step

1. **Collect inputs.** The product and its materials, the origin country, the
   destination marketplace, the factory price and Incoterm (EXW or FOB), the freight
   cost and units per shipment, and the HS code if the seller has it.

2. **Classify.** Confirm or estimate the HS code from the product and materials. If
   estimated, flag it and recommend a broker confirmation.

3. **Find the base duty rate** for that HS code and route.

4. **Check for additional tariffs** specific to the product and origin country. Mark
   any policy-dependent rate as an estimate.

5. **Build the stack.** Factory price, freight per unit, duty, additional tariffs,
   customs fees, insurance, inland and broker. Compute landed cost per unit.

6. **Hand off the number.** State clearly that this landed cost is the input to
   amz-fba-calculator and amz-profit-analyzer.

7. **Run the quality check**, then deliver.

## Output format

```
## Landed Cost. [product]

Route: [origin] to [destination]   HS code: [code, confirmed or estimated]

### Landed cost stack (per unit)
Factory price:        [$]
Freight per unit:     [+$]
Import duty:          [+$]   (rate [%] on customs value)
Additional tariffs:   [+$]   (if any. mark as estimate if policy-dependent)
Customs fees:         [+$]
Insurance:            [+$]
Inland + broker:      [+$]

### Landed cost per unit: [$]

### Flags
[HS-code-estimate warnings, policy-dependent-rate warnings]

Use this landed cost as the cost input for amz-fba-calculator and amz-profit-analyzer.
```

## Worked example

A seller imports a stainless kitchen tool. Factory price 4.00 USD FOB, ocean freight
working out to 0.55 per unit.

HS code estimated from the product and material, flagged for broker confirmation.
Base duty rate applied to the customs value adds about 0.50. The seller checks and
the product and origin country also carry an additional tariff, which is policy-
dependent and adds a further amount, marked as an estimate. Customs fees, insurance,
and inland trucking plus the broker fee add roughly another 0.45 per unit.

Landed cost per unit lands well above the 4.00 factory price. The seller had been
modeling margin on 4.00. the real cost input is the landed figure, and that is what
goes into the FBA and profit calculations.

## Quality check

- All six layers added to the factory price are included.
- The duty rate is tied to an HS code, and an uncertain code is flagged with a
  recommendation to confirm with a broker.
- Additional or trade-remedy tariffs are checked, not just the base duty.
- Policy-dependent rates are marked as estimates with a warning symbol.
- The output states that the landed cost is the input for the FBA and profit skills.

## Common mistakes

- **Planning on the factory price.** The single most common import-cost mistake.
- **Guessing the HS code.** A wrong classification means a wrong duty and possible
  customs penalties.
- **Missing additional tariffs.** Trade-remedy tariffs can exceed the base duty and
  are easy to overlook.
- **Forgetting the small lines.** Customs fees, insurance, broker, and inland
  trucking are individually small and collectively significant.
- **Stale rates.** Tariff policy changes. a rate from last year may no longer hold.

This skill is general guidance, not customs advice. confirm classifications and
rates with a licensed customs broker before committing.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
