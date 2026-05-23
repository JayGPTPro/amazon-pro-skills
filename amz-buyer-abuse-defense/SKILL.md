---
name: amz-buyer-abuse-defense
description: >-
  Identify and act on Amazon buyer abuse: serial returners, INR fraud,
  materially-different claim abuse, and refund-without-return patterns. Builds
  the case to Amazon to refund the seller and ban or restrict the buyer. Use
  when a user asks about buyer fraud, serial returners, abusive customers,
  repeat A-to-z claims, return abuse, or how to report a bad buyer. Trigger
  phrases: "buyer abuse", "serial returner", "buyer fraud", "abusive customer",
  "report a buyer", "INR fraud". Works with zero tools. the user pastes the
  order and claim history.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Buyer Abuse Defense

Amazon's buyer-protection bias leaves sellers absorbing fraud and abuse losses
unless they build the case correctly. This skill identifies the abuse pattern and
files the report that gets the seller refunded and the buyer flagged.

## When to use this

- The same buyer has filed multiple A-to-z claims across orders.
- A serial returner pattern (high return rate on one customer).
- An INR claim where delivery proof is clear but the buyer refuses to accept it.
- A "materially different" claim on a product that matches the listing exactly.

## The framework. The Abuse Pattern Rubric

Five abuse patterns Amazon recognizes when documented properly.

1. **Serial returner.** One buyer with an unusually high return rate across orders.
2. **INR refusal.** Buyer claims item not received but delivery proof is clean.
3. **Materially-different abuse.** Buyer claims SNAD on a product that matches the
   listing exactly, often after using it.
4. **Refund-without-return.** Buyer gets a refund issued but never returns the
   item, then orders again with the same pattern.
5. **Coordinated fraud.** Multiple accounts at the same address or IP, returning or
   claiming on the same SKU.

Each has a specific evidence packet Amazon's buyer abuse team responds to.

## Step by step

1. **Collect inputs.** The buyer order history visible, claim or return history,
   any messages, delivery proofs, and the SKU pattern.

2. **Classify the pattern.** Match to one of the five from the rubric.

3. **Assemble evidence.** Per pattern. dates, order IDs, delivery scans, returns
   condition photos if FBM, listing-vs-claim comparison for SNAD claims.

4. **File the case.** Through Seller Support, Account Health, or the dedicated
   Buyer Abuse form (where available). Use the words "buyer abuse" or "fraudulent
   buyer behavior" so it routes to the right team.

5. **Request specific remedies.** Refund of the loss, restriction or ban of the
   buyer, and protection from future ODR hits from the same buyer.

6. **Track the pattern outcome.** Amazon may not always confirm action, but the
   same buyer often stops appearing on the seller's orders.

7. **Run the quality check**, then deliver.

## Output format

```
## Buyer Abuse Case. [order or buyer]

Pattern: [serial returner / INR refusal / SNAD abuse / refund-no-return / coordinated]

### Evidence
1. [exhibit] . [source] . [what it shows]
...

### Case narrative
[short, factual, dated, references each exhibit]

### Requested remedies
- Refund the seller's loss on these orders: [list]
- Restrict or ban the buyer
- Protect ODR from the named buyer's claims

### Where to file
[exact path. Seller Support / Account Health / Buyer Abuse form]
```

## Worked example

The same buyer filed 3 A-to-z claims in the past 60 days, all INR on FBA orders
with clean delivery scans. Pattern: INR refusal. Evidence: order IDs, dates,
delivery scans with GPS, the buyer's claim text in each. Case filed under Buyer
Abuse with a request to refund the seller, restrict the buyer, and remove the ODR
hits. Amazon refunded two of three within 14 days and the buyer stopped appearing
on the seller's orders.

## Quality check

- The abuse pattern is named, not described vaguely.
- Evidence is per-exhibit and dated, not summarized.
- The case explicitly uses the words 'buyer abuse' or 'fraudulent buyer behavior'
  to route correctly.
- Specific remedies are requested, including ODR protection.
- The pattern is tracked across multiple orders, not filed as a one-off.

## Common mistakes

- **Filing per-order.** Amazon dismisses single-order claims that look isolated.
  pattern across multiple orders is what triggers action.
- **No delivery proof.** INR refusal cases need clean delivery evidence.
- **Emotional case.** "This buyer is a liar" reads as opinion. dates and exhibits
  read as fact.
- **Forgetting ODR.** Requesting refund but not ODR protection. the A-to-z claim
  may stay on the metric even when refunded.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
