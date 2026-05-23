---
name: amz-global-selling
description: >-
  Evaluate and plan Amazon international expansion. Sizes the opportunity in a
  target marketplace, checks the regulatory and tax requirements, plans logistics
  and fulfillment, and sequences which marketplace to enter first. Use when a
  user asks about selling internationally, expanding to the EU, UK, Japan,
  Canada, Australia, or other Amazon marketplaces, global selling, or which
  country to expand to next. Trigger phrases: "global selling", "expand
  internationally", "sell in the EU", "sell in the UK", "international
  marketplace", "which country next". Works with zero tools.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Global Selling Planner

International expansion is where sellers either double the business or quietly bleed
money on a marketplace they did not understand. The difference is sequencing and
homework. This skill scores a target marketplace and builds the entry plan before a
single unit ships.

## When to use this

- A product is doing well in the home marketplace and the seller wants the next one.
- A seller is unsure whether the UK, the EU, Japan, Canada, or Australia comes first.
- A seller jumped into a marketplace and is now stuck on tax or compliance.
- Planning inventory and fulfillment for a multi-country footprint.

## The framework. The Market Entry Score

Score each candidate marketplace on five gates. A low score on a hard gate, tax or
compliance, is a stop, not a deduction.

| Gate | The question | Stop condition |
|------|--------------|----------------|
| Demand | Is there real search demand for this product there? | No demand, no entry |
| Competition | Can the listing win against local incumbents? | Saturated with entrenched locals |
| Tax | VAT, GST, or sales-tax registration and filing burden | Cannot or will not meet it |
| Compliance | Product safety marks, labeling, language, certifications | Product cannot be made compliant |
| Logistics | Can inventory be delivered there at a workable cost? | No viable freight or fulfillment path |

A marketplace clears entry only when Demand and Competition are favorable and Tax,
Compliance, and Logistics are all genuinely solvable.

## The marketplace shortlist

- **Canada.** Usually the gentlest first step for a North American seller. shared
  language, close logistics, North American Unified Account.
- **UK.** A strong standalone English-language market. its own VAT regime.
- **EU (Germany, France, Italy, Spain, Netherlands).** Large, but VAT across
  countries and EU product compliance make it the heaviest lift.
- **Japan.** High-value, lower competition for the right product, but language and
  local compliance are real work.
- **Australia.** Smaller, English-language, GST rules, long freight.

## Step by step

1. **Collect inputs.** The product and category, the home marketplace and current
   performance, the candidate countries, and the seller's appetite for tax and
   compliance admin.

2. **Score each candidate** on the five gates. Mark any hard-gate failure as a stop.

3. **Sequence the entry.** Recommend one marketplace first, the one with the highest
   score and the lowest operational lift. Expansion is sequential, not simultaneous.

4. **Plan tax and compliance** for the chosen marketplace: which registrations,
   which product marks and labels, which language requirements.

5. **Plan logistics.** Decide between shipping into local FBA, using Amazon's
   cross-border programs, or a remote-fulfillment option, and price each.

6. **Plan the listing.** Translation and localization, not machine translation.
   localized keywords, localized pricing, localized images where needed.

7. **Run the quality check**, then deliver.

## Output format

```
## Global Selling Plan. [product]

### Market Entry Scores
[country] . demand . competition . tax . compliance . logistics . verdict
...

### Recommended first marketplace
[country] . why first

### Entry plan for [country]
Tax: [registrations and filing]
Compliance: [marks, labels, language]
Logistics: [fulfillment route and cost]
Listing: [localization plan]

### Next marketplace after this one
[country and trigger to expand]
```

## Worked example

A US seller of a kitchen gadget, strong at home, considering UK and Germany.

Scores: UK clears all five gates, one VAT registration, English listing, manageable
freight. Germany has demand but EU-wide VAT and product compliance make it a heavier
lift. Recommendation: UK first. it banks an international revenue stream with one tax
registration. Germany and the wider EU come second, once UK operations are steady and
the VAT and compliance work can be done properly.

## Quality check

- Every candidate is scored on all five gates.
- Tax, compliance, and logistics are treated as hard gates, not minor deductions.
- Exactly one marketplace is recommended first. expansion is sequenced, not parallel.
- The entry plan names specific tax registrations and compliance marks, not "check
  local rules".
- Listing localization is real translation, not machine translation.

## Common mistakes

- **Entering everywhere at once.** Spreading inventory and attention thin across
  five new marketplaces.
- **Ignoring VAT and GST.** Tax registration and filing are the most underestimated
  cost of international selling.
- **Machine-translated listings.** A literal translation reads as foreign and
  converts poorly. localize.
- **Skipping product compliance.** A product that is legal at home may need new
  safety marks, labels, or certifications abroad.
- **Underpricing freight.** International logistics can erase the margin that made
  the product worth expanding.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. 50 production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
