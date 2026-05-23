---
name: amz-account-health-triage
description: >-
  Triage an Amazon Account Health Rating (AHR) screenshot or text dump.
  Identifies which violations and metrics are pulling the rating down,
  prioritizes by point weight, and outputs a remediation order. Use when a user
  asks about Account Health, AHR, account health rating dropping, violations
  to address, or stabilizing a yellow or red account. Trigger phrases:
  "account health", "AHR", "violations", "policy strikes", "account at risk".
  Works with zero tools. the user pastes the AHR snapshot.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Account Health Triage

Account Health Rating shifts faster than ever under the 2025 expanded visibility.
Sellers see numbers move green to yellow to red and do not know which violation
matters most. This skill reads the snapshot and tells you what to fix first.

## When to use this

- AHR dropped and the seller does not know why.
- Multiple violations are open and the seller does not know which to address first.
- The account is yellow or red and a suspension is plausible.
- Routine quarterly review.

## The framework. The Triage Order

Not all violations weigh equally. Address in this order:

1. **Suspension-trigger violations.** IP complaints, authenticity, restricted, safety.
   These can suspend a listing or account on a single bad complaint. Fix immediately.
2. **Order-defect rate (ODR).** The headline performance metric. negative feedback,
   A-to-z claims, chargebacks. A single bad week pushes ODR over the threshold.
3. **Late shipment rate and valid tracking rate.** Fulfillment reliability. Fast to
   move with operational changes.
4. **Cancellation rate.** Seller-caused cancellations from stockouts or pricing errors.
5. **Policy violations with point values.** Each carries weight in the AHR score.
   address by point cost.
6. **Listing quality issues.** Lowest urgency, but cumulative weight.

Within each tier, sort by recency. fresh violations weigh more than aging ones.

## Step by step

1. **Collect the snapshot.** Current AHR score, list of open violations, current
   performance metrics, recent listing flags.

2. **Classify each item** into the six tiers above.

3. **Identify the binding tier.** Where the score is dropping from. Often one tier
   accounts for most of the loss.

4. **Build the remediation order.** Tier 1 first, then by point cost within each
   tier. Each action has its expected impact on the score.

5. **Tie to existing skills.** Suspension-trigger items route to
   `amz-suspension-appeal`. Listing-suppression items route to the suppression
   recovery skill. Compliance items route to `amz-product-compliance`.

6. **Set the review cadence.** Weekly check during recovery, monthly when stable.

7. **Run the quality check**, then deliver.

## Output format

```
## Account Health Triage. [account]

Current AHR: [score]   Status: [green/yellow/red]

### Triage list (in order to address)
1. [tier] . [violation] . [point cost or impact] . [route to]
2. ...

### Binding tier
[which tier accounts for most of the drop]

### This week
[top 3 actions, ordered]

### Review cadence
[weekly / monthly]
```

## Worked example

Account AHR at 180, yellow. Open: two IP complaints, an ODR at 1.2 percent, a late
shipment rate at 6 percent, three listing-quality flags.

Triage: IP complaints first (tier 1, suspension trigger), route both to suspension
appeal workflow with evidence. ODR next (tier 2), respond to the negative feedback
and dispute the open A-to-z. Late shipment rate (tier 3), shift to FBA or fix the
handling-time process. Listing-quality flags last. The IP complaints alone are worth
roughly 60 points if cleared. ODR another 30. The triage shows the path back to
green without scattershot action.

## Quality check

- Every violation is classified into one of the six tiers.
- Suspension-trigger items are first, regardless of point value.
- The binding tier is named.
- Each action has an expected score impact.
- Items requiring other skills are routed to those skills, not duplicated.

## Common mistakes

- **Treating all violations equally.** A 2-point listing-quality flag is not the
  same as an IP complaint.
- **Reacting to the score, not the violations.** Trying to "raise the number"
  without identifying which specific items are pulling it.
- **Ignoring fresh violations.** Recent violations weigh more than old ones in the
  formula.
- **No review cadence.** AHR drifts. a weekly check during recovery catches new
  issues before they compound.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
