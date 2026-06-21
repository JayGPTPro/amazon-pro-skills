---
name: amz-reimbursement-audit
description: >-
  Build Amazon FBA reimbursement claims under the 2025 manufacturing-cost policy.
  Identifies eligible cases (lost units, warehouse-damaged units, customer-return
  losses, fee errors), assembles the cost-basis evidence Amazon now requires, and
  produces a claim packet per case within the 60-day window. Use when a user
  asks about FBA reimbursements, lost inventory claims, warehouse damage, the
  new reimbursement policy, manufacturing cost evidence, or unrecovered refunds.
  Trigger phrases: "reimbursement", "FBA claim", "lost inventory", "warehouse
  damage", "manufacturing cost", "60 day window", "SAFE-T". Works with zero
  tools. the user pastes the relevant Amazon report rows and supplier invoices.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Reimbursement Audit

Amazon changed how it values reimbursements: for inventory lost or damaged in a
fulfillment center, it now pays on your product manufacturing (sourcing) cost rather
than selling price, and you set that cost in Seller Central. Amazon still runs
automated reconciliation and proactively reimburses many warehouse lost and damaged
cases on its own. manual claims are for the cases its system did not catch, or closed
without paying, and for getting the cost basis right. This skill builds the claim
packet that actually gets paid for the cases that fall through.

## When to use this

- Units lost or damaged in the warehouse that automated reconciliation never
  reimbursed, or reimbursed for less than expected.
- A refund processed for a customer but the unit was not returned, or returned damaged.
- Old reimbursement habits that no longer match the current policy.
- Multiple claim-eligible events sitting past the filing-window risk.

## The framework. The Four Claim Cases

Every Amazon reimbursement case is one of four types. Each has a different evidence
requirement, but all four now require cost-basis proof if the seller wants the
higher payout.

| Case | What happened | Trigger report | Evidence required |
|------|---------------|----------------|-------------------|
| Lost | Inbound or warehouse loss | Reconciliation, Inventory Adjustments | shipment IDs, units lost, manufacturing cost |
| Warehouse damaged | Amazon-caused damage | Inventory Adjustments code reasons | adjustment IDs, unit cost |
| Customer return | Refund issued, no return or damaged return | Returns report, Reimbursements report | order ID, refund date, return status, cost |
| Fee error | Wrong fulfillment fee or referral fee | Payments report | the wrong charge, the right charge, the delta |

For every case, build cost basis once: the manufacturing (sourcing) cost per unit from
the supplier invoice. Amazon defines manufacturing cost as your cost to source the
product and excludes shipping, handling, and customs duties. so use the per-unit
invoice price, not the fully landed cost. Same number for every future claim on that
SKU, set on the Manage Your Sourcing Cost page in Seller Central.

## The 60-day window

Claims must be filed within 60 days of the triggering event. Anything older is
unrecoverable. The first job of any audit is to scan for events near the window edge
and file those first.

## Step by step

1. **Collect inputs.** The Reconciliation, Inventory Adjustments, Returns, and
   Payments reports the user can paste. Plus a supplier invoice to read the
   manufacturing (sourcing) cost per unit for the SKUs involved.

2. **Compute cost basis per SKU.** Per-unit manufacturing (sourcing) cost from the
   supplier invoice. exclude freight, duty, and handling, since Amazon's manufacturing-
   cost definition leaves them out. This is the number Amazon now wants, set on the
   Manage Your Sourcing Cost page.

3. **Classify every reimbursable event** into one of the four claim cases.

4. **Run the window check.** Sort by days since the event. Anything inside 60 days is
   recoverable. Anything beyond is lost. file the at-risk cases first.

5. **Build the packet per case.** Claim narrative, evidence list, cost basis
   calculation, and the exact case form to open in Seller Central.

6. **Track and follow up.** Amazon often denies on a technicality. Plan a follow-up
   round with the cost-basis evidence attached again.

7. **Run the quality check**, then deliver.

## Output format

```
## Reimbursement Audit. [SKU or catalog]

Cost basis per SKU: [SKU] . [$ per unit] . source: [supplier invoice, sourcing cost]

### Claim packet
Case 1. [type] . event date . days remaining . units . $ at stake
  Narrative: [one-paragraph factual story]
  Evidence: [list]
  Cost basis: [$]
  Where to file: [exact Seller Central path]

...

### Priority order
1. [Cases inside 14 days of window edge]
2. [Cases by dollar size]
```

## Worked example

A seller has 24 units of a 22 USD product lost in an inbound shipment 53 days ago,
plus 8 refunds where the units never returned, average 31 days ago.

Cost basis: 6.40 per unit, the manufacturing (sourcing) cost read straight off the
supplier invoice, freight and duty excluded. Lost case: 24 units x 6.40 = 154 USD owed,
filed inside the 60-day window with the cost evidence and the shipment ID, on day 53.
Customer-return cases: 8 separate cases, filed in priority order, average 29 days
remaining. Amazon's automated reconciliation may have already reimbursed some of these.
the audit is for the cases it missed or closed without paying, and to make sure the
sourcing cost is set so the payout is on cost basis rather than a lower default.

## Quality check

- Cost basis per SKU is computed before any claim narrative is written.
- Every event is classified into one of the four cases.
- The 60-day window is checked first. at-risk cases are filed before larger ones.
- Each packet has narrative, evidence list, and cost basis attached.
- A follow-up plan exists for the common Amazon initial denial.

## Common mistakes

- **Assuming automation catches everything.** Amazon proactively reimburses many
  warehouse lost and damaged cases, but not all. the ones it misses or closes without
  paying still need a manual claim inside the window.
- **Filing without cost evidence.** The default payout dropped sharply. cost basis is
  the difference between recovering 40 cents and 100 cents on the dollar.
- **Missing the window.** Events past 60 days are lost.
- **Submitting and giving up after one denial.** Amazon often denies first, accepts
  on resubmission with the same evidence.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
