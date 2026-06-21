---
name: amz-fee-audit
description: >-
  Audit Amazon Payments report for fee errors. Finds incorrect FBA fulfillment
  fees (wrong size tier), missing referral fee credits on refunds, duplicate
  charges, and FBA storage discrepancies, and produces an FBA fee-discrepancy
  case packet per finding. Use when a user asks about Amazon fee errors,
  overcharged fees, wrong size tier, missing referral refunds, fee audit, or
  Payments report analysis. Trigger phrases: "fee audit", "overcharged", "wrong
  fee", "size tier error", "referral fee refund", "payments report", "FBA fee
  dispute". Works with zero tools. the user pastes Payments report rows.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Fee Audit

After the 2024 size-tier reshuffle, dimensional-tier misclassification became the
single most common hidden fee leak. Sellers also miss referral fee credits on
refunded orders. This skill audits the Payments report for these specific anomalies
and writes the FBA fee-discrepancy case per finding. Fee overcharges are disputed
through Seller Support FBA Fee Discrepancies, not SAFE-T. SAFE-T reimburses sellers on
certain refund and return claims, it is not the channel for FBA fee errors.

## When to use this

- FBA fees feel high and the seller does not know which line is wrong.
- A product is near a size-tier boundary.
- High refund rate and not sure the referral fee was credited back.
- Routine quarterly audit to catch silent fee creep.

## The framework. The Five Fee Anomalies

Every Payments report contains one or more of these five patterns:

1. **Size-tier misclassification.** The unit is billed at a higher size tier than its
   measurements warrant. Cross-check listed dimensions vs the FBA tier table.
2. **Missing referral refund.** A refund was processed but the referral fee was not
   returned proportionally. Cross-check refund row vs the original sale.
3. **Duplicate fulfillment fee.** Two FBA fees for the same order. usually a system
   error.
4. **Storage discrepancy.** Monthly storage billed for units already removed or units
   in transit.
5. **Reimbursement gap.** A reimbursement issued at the old (lower) policy rate that
   should have been higher under 2025 cost-basis policy.

## Step by step

1. **Collect inputs.** A Payments report (date range, transactions) plus product
   dimensions for the SKUs in scope.

2. **Build the expected fees.** For each SKU and order, what the fees should be by
   the current FBA fee tables.

3. **Compare row by row.** Flag every transaction where actual exceeds expected, or
   where a refund did not produce a matching referral credit.

4. **Compute the recovery.** Total dollars across all flagged transactions.

5. **Open the fee reimbursement case** under Seller Support > Fulfillment by Amazon
   > FBA Fee Discrepancies, one case per anomaly type, with the report rows as
   evidence and the calculated delta. (SAFE-T is a separate process for FBM/SFP
   A-to-z refunds, do not file fee disputes through it.)

6. **Plan the structural fix.** A size-tier issue is recurring. The fix is updating
   the listed dimensions, not just claiming back.

7. **Run the quality check**, then deliver.

## Output format

```
## Fee Audit. [account / period]

### Anomalies found
1. Size-tier misclassification . [SKU] . [units affected] . [$ delta]
2. Missing referral refunds . [orders] . [$ delta]
...

### Total recovery available: [$]

### Cases to open (Seller Support > FBA > Fees)
Case 1. [anomaly] . [evidence rows] . [case narrative]
...

### Structural fixes
[dimensions to update, processes to add]
```

## Worked example

A seller's product is billed at large-standard but actually measures small-standard.
20 days of orders sit at the wrong tier, costing ~1.20 USD per unit. 800 units sold
in period = 960 USD overcharge. An FBA fee-discrepancy case opens under Seller Support
FBA Fee Discrepancies with the report rows, the correctly-measured dimensions, and the
tier-table reference. Recovery typically within two weeks. Structural fix: update the
dimensions in the listing so the issue does not recur. The seller had been paying the
wrong fee for months.

## Quality check

- Every anomaly is one of the five named types.
- Expected fees are computed from the current FBA tables, not assumed.
- Each finding has report rows as evidence, not just a calculation.
- The structural fix is included so the leak does not recur after the recovery.

## Common mistakes

- **Auditing only when it feels expensive.** Most fee leaks creep quietly.
- **Claiming the dollars without fixing the source.** Same anomaly returns next month.
- **No expected-fee baseline.** Without 'what should it have been', there is nothing
  to detect.
- **Ignoring referral refunds.** Easy to miss on high-refund SKUs and small per-item.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
