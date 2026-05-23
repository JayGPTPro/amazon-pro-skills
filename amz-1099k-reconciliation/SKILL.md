---
name: amz-1099k-reconciliation
description: >-
  Reconcile Amazon's 1099-K against actual deposits, fees, and refunds for tax
  filing. Explains the gap between gross sales on the 1099-K and what hit the
  bank, maps the numbers to Schedule C lines, and produces the worksheet the
  seller or their CPA needs. Use when a user asks about 1099-K, Amazon tax
  documents, reconciling gross vs net sales, year-end tax prep, or why the
  1099-K is higher than their deposits. Trigger phrases: "1099-K", "tax forms",
  "Amazon tax document", "gross vs net", "Schedule C", "year end". Works with
  zero tools. the user pastes the 1099-K and Payments summary.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# 1099-K Reconciliation

Amazon's 1099-K reports gross sales, including refunds and before fees. Most sellers
look at their bank deposits, see a much smaller number, and either overpay tax or
underreport. This skill reconciles the two and produces the worksheet that maps to
Schedule C lines.

## When to use this

- Year-end tax prep and the 1099-K does not match the deposits.
- Working with a CPA who needs the breakdown.
- A first 1099-K and the seller is confused by the gross number.
- Quarterly estimated taxes and the seller wants to know the real revenue.

## The framework. The Gross-to-Net Bridge

The 1099-K shows one number: gross sales. The bank shows another: net deposits. The
bridge between them is:

```
Gross sales (1099-K Box 1)
  minus  Refunds and returns           → Schedule C: Returns and allowances
  minus  Amazon selling fees (referral + FBA + storage) → Schedule C: Commissions/fees
  minus  Advertising spend             → Schedule C: Advertising
  minus  Other deductions (reimbursements net, removals, etc.)
  =      Net cash to bank
```

Each line on the bridge maps to a different Schedule C field. The gross number stays
on the return. the deductions appear on their own lines.

## Step by step

1. **Collect inputs.** The 1099-K (Box 1 total), Amazon's Payments Date Range
   summary for the same year, refund total, and ad spend total. If the seller exports
   the year-end summary report, it contains most of these.

2. **Build the bridge.** Each line from gross to net, with the dollar value.

3. **Reconcile.** Total bridge should match the bank deposits to within a small
   timing variance. Investigate any large gap.

4. **Map to Schedule C.** Per-line Schedule C field name, ready to hand to a CPA.

5. **Flag the common surprises.** Sales tax collected and remitted by Amazon usually
   passes through but is shown gross. Some categories or marketplaces have different
   treatments. Note them.

6. **Quarterly extension.** For estimated tax planning, run the same bridge on the
   trailing quarter.

7. **Run the quality check**, then deliver.

## Output format

```
## 1099-K Reconciliation. [year]

1099-K Box 1 gross: [$]

### Gross-to-net bridge
Refunds and returns:        [-$]   Schedule C line: Returns and allowances
Amazon selling fees:        [-$]   Schedule C line: Commissions and fees
Advertising:                [-$]   Schedule C line: Advertising
Other deductions:           [-$]   Schedule C line: Other expenses
Net to bank:                [$]

Bank deposits reported:     [$]   Variance: [$]

### Notes for CPA
[sales tax pass-through, marketplace facilitator status, etc.]
```

## Worked example

1099-K Box 1: 1,200,000 USD. Bank deposits for the year: 480,000. The seller thought
he made 480k. The bridge: refunds 90k, Amazon fees (referral plus FBA plus storage)
360k, advertising 180k, removal and storage adjustments 12k, leaves about 558k.
Bank shows 480k. About 30k of the variance is timing (December sales paid in January). A gap of
roughly 14 percent like this one warrants investigation. retained reserves,
uncategorized fees, or a chargeback wave can each open a real gap behind the
timing bucket.
The Schedule C return reports the 1,200,000 gross and the deductions on their own
lines, not a flat 480k of revenue. Under-reporting the 1,200,000 is the mistake the
IRS catches.

## Quality check

- Every line on the bridge is sourced from Amazon's own reports, not estimated.
- Each line is mapped to a specific Schedule C field.
- The reconciliation explains any variance against bank deposits.
- Marketplace facilitator and sales tax pass-through are noted, not ignored.

## Common mistakes

- **Reporting net only.** Showing 480k of revenue when the 1099-K to the IRS says
  1.2M. instant red flag for an audit.
- **Missing the fee deduction.** Paying tax on the gross because the deductions were
  never separated out.
- **Confusing timing variance with an error.** December sales paid in January cause a
  small gap. it is timing, not a bookkeeping error.
- **Treating sales tax as income.** Amazon often collects and remits the tax. it is
  not the seller's income, but it shows up in the gross.

This skill is general guidance, not tax advice. work with a CPA for your specific
situation.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
