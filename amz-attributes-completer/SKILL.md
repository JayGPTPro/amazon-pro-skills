---
name: amz-attributes-completer
description: >-
  Audit and complete the Amazon Seller Central Attributes section for a listing.
  Diffs the category template against the filled fields, ranks the missing
  fields by impact on AI-driven search (Rufus, Alexa+) and traditional ranking,
  and proposes the optimal values. Use when a user asks about the Attributes
  section, missing attributes, product attributes, category fields, or "how
  to fill the back end of my listing". Trigger phrases: "attributes",
  "attributes section", "category fields", "back end fields", "missing
  attributes". Works with zero tools.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Attributes Completer

The Seller Central Attributes section is the most important SEO field most sellers
ignore. Amazon's AI ranking (Rufus, Alexa+, COSMO) reads attributes before bullets
or A+. Most listings fill under 40 percent of available fields. This skill closes
that gap with the right values.

## When to use this

- A new listing being set up and attributes are mostly empty.
- An old listing where attributes were never revisited.
- AI search visibility is weak (long-tail queries return competitors).
- A category template was updated and new fields appeared.

## The framework. The Three-Tier Field Priority

Not all attribute fields weigh equally. Fill in this order.

| Tier | Fields | Why |
|------|--------|-----|
| Tier 1. Identity | Material, dimensions, weight, color, size, count | Hard filters. shoppers narrow by these. AI uses them as facts |
| Tier 2. Use case | Compatibility, audience, age range, use, occasion | Drives long-tail and AI question matching |
| Tier 3. Compliance and brand | Country of origin, batteries, warnings, brand, manufacturer | Required for some categories. avoids suppression |

Within each tier, fill every field the category template offers, even if a value
seems obvious from the title. The AI does not read inference. it reads the field.

## Step by step

1. **Collect inputs.** The category, current Attributes section snapshot (what's
   filled vs empty), the product, any spec sheet.

2. **Pull the category template.** Identify every available field. categories vary,
   and the template adds fields over time.

3. **Diff filled vs available.** Build the list of empty fields.

4. **Classify each empty field** into Tier 1, 2, or 3.

5. **Propose the optimal value** for each empty field. Be specific. "Material:
   Stainless Steel 304", not "Metal".

6. **Prioritize.** Tier 1 first, then 2, then 3. Within a tier, by AI search impact.

7. **Flag any field that requires evidence** (compliance, certifications). these
   need source documents before filling.

8. **Run the quality check**, then deliver.

## Output format

```
## Attributes Audit. [ASIN]

Category: [category]
Filled: [%]   Empty fields: [count]

### Fill order
Tier 1 (Identity)
- [field] . current: [empty/value] . proposed: [value]
...
Tier 2 (Use case)
...
Tier 3 (Compliance and brand)
...

### Evidence required
[fields that need source documents before filling]

### Estimated lift
[expected AI-search lift from filling Tier 1 + 2]
```

## Worked example

A kitchen knife listing in Home and Kitchen. Audit shows 9 of 24 category fields
filled. Empty Tier 1: blade material, handle material, exact dimensions, weight.
Empty Tier 2: handedness, cut type, intended use, knife type, dishwasher safe.
Empty Tier 3: country of origin, warranty type.

Plan: fill all Tier 1 fields with specific values (Blade material: VG-10 Damascus
steel, not "stainless"). Tier 2 fields with the exact use case wording (Intended
use: home cooking, professional chef). Tier 3 last, with documentation where
needed. Lift: long-tail queries like "8-inch chef knife Damascus stainless" now
match this listing strongly through the AI ranking layer.

## Quality check

- Every field is classified into a tier.
- Tier 1 is filled first, with specific values not generic placeholders.
- Compliance fields are flagged for evidence before filling.
- Empty fields are prioritized by AI-search impact, not alphabetical.
- The estimated lift is realistic, not vague.

## Common mistakes

- **Generic values.** "Material: Metal" instead of "Material: Stainless Steel 304".
  the AI reads specifics.
- **Skipping fields that "feel obvious".** The AI does not infer from the title. it
  reads the field directly.
- **Filling Tier 3 first.** Compliance and brand fields are important but lower
  impact on search than the Tier 1 identity fields.
- **Set and forget.** Categories add fields over time. attributes need a quarterly
  re-audit.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
