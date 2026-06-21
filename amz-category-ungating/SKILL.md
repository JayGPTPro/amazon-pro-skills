---
name: amz-category-ungating
description: >-
  Guide a seller through getting ungated in a restricted Amazon category or
  brand. Identifies what is gated, what documents Amazon wants, how to source a
  compliant invoice, and how to submit an approval request that passes the first
  time. Use when a user asks about ungating, restricted categories, getting
  approved to sell a category or brand, gated products, or an approval request
  that was denied. Trigger phrases: "ungating", "restricted category", "get
  approved to sell", "gated", "category approval", "brand approval", "invoice
  for ungating". Works with zero tools.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Category Ungating Guide

Amazon gates categories and brands to keep out low-quality and counterfeit sellers.
The gate is not a wall, it is a document check. Most ungating denials happen because
the seller submitted the wrong kind of invoice. This skill gets the request right
the first time.

## When to use this

- A seller wants to list a product and Amazon shows "Approval required".
- A category like Grocery, Beauty, Health, Watches, or Automotive is blocking a listing.
- A specific brand is gated and the seller needs brand approval.
- A previous ungating request was denied and the seller does not know why.

## The framework. The Ungating Document Test

Amazon almost always wants one thing: proof you have a real, compliant supply source.
The approval request passes when the invoice survives all five tests. A denial is
nearly always one failed test.

1. **Real supplier.** The invoice is from a genuine wholesaler or the brand or
   manufacturer, not a retail receipt. A Costco or retail receipt fails.
2. **Quantity.** The invoice shows a real wholesale quantity, commonly 10 units or
   more of the gated item.
3. **Recency.** The invoice is dated within the last 90 days, usually.
4. **Match.** The business name and address on the invoice match the Seller Central
   legal entity exactly.
5. **Legible and complete.** Supplier name, supplier address, supplier phone or
   website, your details, item description, quantity, and date. all visible, nothing
   redacted.

If any test fails, fix the invoice before submitting. resubmitting the same flawed
invoice wastes an attempt.

## Step by step

1. **Confirm what is gated.** A category, a sub-category, or a specific brand. The
   path differs. Check in Seller Central under the listing or via Add a Product.

2. **Read Amazon's exact request.** Amazon states what it wants: invoices, letters of
   authorization, compliance documents, or images. Build to that list, not a generic one.

3. **Source a compliant invoice.** If the seller only has retail receipts, the gate
   will not open. Route them to a genuine wholesale account or a brand-authorized
   distributor first.

4. **Run the five-test check** on the invoice. Fix every failure.

5. **Prepare any extra documents.** Some gates also want a letter of authorization
   from the brand, safety or compliance certificates, or product and packaging photos.

6. **Submit and track.** Submit through the approval request flow. If denied, read the
   denial reason, map it to the failed test, fix that specific item, and resubmit.

7. **Run the quality check**, then deliver.

## Output format

```
## Ungating Plan. [category or brand]

Gate type: [category / sub-category / brand]
Amazon is asking for: [exact list]

### Invoice check
[test] . [pass/fail] . [fix if fail]
...

### Documents to prepare
1. ...

### Submission steps
1. ...

### If denied
[how to read the reason and what to fix]
```

## Worked example

A seller wants to sell a gated grocery brand. Amazon asks for invoices.

The seller has a receipt from a wholesale club. Tests: real supplier fails, a club
receipt is retail. Quantity passes. Recency passes. Match fails, the receipt has no
business name. Action: open a true wholesale account with a grocery distributor,
order 10-plus units of the item, and use that invoice. The club receipt would have
been an automatic denial.

## Quality check

- The exact gate type is confirmed before any document advice.
- The advice is built to Amazon's stated request, not a generic checklist.
- The invoice passes all five tests before submission is recommended.
- Retail receipts are explicitly rejected as a source.
- A denial path is included. read the reason, fix that test, resubmit.

## Common mistakes

- **Retail receipts.** A Costco, Walmart, or Sam's Club receipt is not a wholesale
  invoice and fails instantly.
- **Name mismatch.** The invoice business name does not match Seller Central.
- **Redacting the invoice.** Blacking out the supplier to hide the source. Amazon
  needs the supplier visible. redaction fails the request.
- **Resubmitting the same document.** Denied, then resubmitting unchanged. Read the
  reason and fix the specific failure.
- **Old invoices.** Outside the recency window.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
