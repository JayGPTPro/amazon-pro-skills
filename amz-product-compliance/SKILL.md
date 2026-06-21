---
name: amz-product-compliance
description: >-
  Check an Amazon product for compliance and safety requirements before and
  after listing. Covers required certifications, labeling and warning
  requirements, restricted-substance rules, documentation Amazon may demand, and
  category-specific safety rules. Use when a user asks about product compliance,
  safety requirements, certifications, required labels or warnings, a compliance
  document request from Amazon, or whether a product is allowed. Trigger
  phrases: "product compliance", "safety requirements", "certifications",
  "compliance documents", "required labels", "is this product allowed". Works
  with zero tools.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Product Compliance Check

Compliance is the risk that does not show up until it is a crisis: a listing pulled,
an account flagged, a recall. Most of it is preventable with a check before sourcing.
This skill runs that check and tells a seller what to secure before money is committed.

## When to use this

- Before sourcing a product, to know what compliance it will require.
- Amazon has requested compliance or safety documents for a live listing.
- A product is in a sensitive category: children's items, electronics, supplements,
  cosmetics, food contact, batteries.
- A seller is unsure whether a product can be sold at all.

## The framework. The Compliance Stack

Run the product through five layers. A gap in any layer is a risk to close before
the product goes live, ideally before it is even ordered.

1. **Category gate.** Is the category restricted or gated, and does selling it need
   approval? See amz-category-ungating. Some products are simply prohibited.

2. **Certifications and testing.** Does the product need third-party testing or a
   certification mark? Children's products, electronics, and items with electrical or
   wireless parts commonly do. Identify which tests and marks apply.

3. **Labeling and warnings.** Does the product or packaging need specific warnings,
   age grading, content labels, country of origin, or a safety mark printed on it?
   A missing required warning is a common takedown trigger.

4. **Restricted substances and materials.** Do the materials trigger any restricted-
   substance rule, food-contact rule, or hazardous-material handling rule? This
   affects both legality and how the product can be shipped and stored.

5. **Documentation readiness.** Amazon can request a compliance document at any time.
   Test reports, certificates, safety data sheets, supplier declarations. Have them
   on file before the request comes, not after the listing is already down.

## Step by step

1. **Collect inputs.** The product, its category, its materials, who uses it
   (especially whether children), whether it has electrical, battery, or wireless
   parts, and the destination marketplace.

2. **Walk the five layers.** For each, state what applies to this specific product
   and whether the seller has it or must obtain it.

3. **Rank the gaps by risk.** A missing required certification or warning is a high
   risk. it can pull the listing and flag the account. Order the gaps accordingly.

4. **Name the fix per gap.** Which test, which lab type, which label change, which
   document to request from the supplier. Be specific.

5. **Set the timing.** Mark which items must be secured before sourcing, before
   listing, and which can be held ready for an Amazon request.

6. **Add a marketplace note.** Compliance differs by country. flag that the same
   product needs a fresh check for any other marketplace.

7. **Run the quality check**, then deliver.

## Output format

```
## Compliance Check. [product]

Category: [category]   Users: [incl. children?]   Marketplace: [country]

### Compliance Stack
1. Category gate: [applies?] . [status / action]
2. Certifications and testing: ...
3. Labeling and warnings: ...
4. Restricted substances and materials: ...
5. Documentation readiness: ...

### Gaps by risk
[gap] . [risk level] . [specific fix] . [secure by: sourcing / listing / on-file]

### Marketplace note
[reminder that other countries need a fresh check]
```

## Worked example

A seller is sourcing a child's nightlight.

Category gate: toys and children's products, allowed but sensitive. Certifications:
a children's product, so it needs children's product safety testing, and as an
electrical item it needs electrical safety testing. Labeling: needs age grading, a
tracking label, and any required electrical safety marking. Restricted substances:
children's product, so lead and phthalate limits apply, secure a test report.
Documentation: keep the test reports and the children's product certificate on file.

Gaps by risk: the safety testing and the children's product certificate are high
risk and must be secured before sourcing in bulk. A nightlight ordered without them
can be pulled on day one and flag the account.

## Quality check

- All five layers of the stack are walked for this specific product.
- Children's products, electronics, and consumables are recognized and trigger their
  specific testing requirements.
- Every gap names a specific fix, not "check the rules".
- Gaps are ranked by risk, with takedown-and-flag risks marked high.
- Timing is set. what to secure before sourcing versus before listing versus on-file.
- A reminder is included that other marketplaces need a separate check.

## Common mistakes

- **Sourcing first, compliance later.** Discovering after a bulk order that the
  product needed testing it does not have.
- **Missing required warnings.** A label or warning omitted from the packaging,
  triggering a takedown.
- **No documents on file.** Amazon requests a certificate, the seller has none, the
  listing goes down while they scramble.
- **Assuming compliance travels.** A product compliant at home failing the rules of
  another marketplace.
- **Trusting the supplier blindly.** A supplier saying "it is certified" without the
  actual report in hand.

This skill is general guidance, not legal advice. for a specific product, confirm
requirements with a qualified compliance professional.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
