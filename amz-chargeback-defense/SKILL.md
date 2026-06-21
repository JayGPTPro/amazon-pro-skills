---
name: amz-chargeback-defense
description: >-
  Defend Amazon chargebacks and A-to-z claims within the 3-day A-to-z response window.
  Identifies the claim type, builds the evidence packet (tracking, signature,
  messaging history, fulfillment proof), and writes the response narrative
  Amazon's case reviewers read for. Use when a user asks about chargebacks,
  A-to-z claims, INR (item not received), SNAD (significantly not as described),
  payment disputes, or defending an order claim. Trigger phrases: "chargeback",
  "A-to-z claim", "INR", "SNAD", "dispute", "buyer claim", "order defense".
  Works with zero tools. the user pastes the claim text and order data.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Chargeback and A-to-z Defense

A chargeback (credit-card network dispute) and an A-to-z claim (Amazon-mediated)
are two different processes with different deadlines. Both punish the seller who
ignores them and reward the seller who responds with the right evidence. This skill
builds the response for either path.

## When to use this

- A chargeback notification arrived from Amazon.
- An A-to-z claim is open and the response window is counting down.
- The seller has been auto-losing claims and wants a real process.
- A pattern of claims on a specific SKU or carrier suggests a fix.

## The framework. The Claim Type Decision Tree

Three claim types. Each has a different burden of proof. Identify first.

| Claim type | Buyer says | Burden of proof |
|------------|-----------|-----------------|
| INR (item not received) | Did not arrive | Carrier delivery proof, tracking with delivery scan, signature if signed |
| SNAD (not as described) | Wrong item or condition | Listing text and images at time of sale, fulfillment records, return offered |
| Fraud / unauthorized | I didn't make this purchase | IP/device data, order pattern, communication trail |

Amazon's case reviewers read for the burden of proof for the specific claim type.
Send the wrong evidence and the case is lost even if the seller is right.

## Step by step

1. **Collect inputs.** The claim text Amazon sent, the order ID, fulfillment method
   (FBA or FBM), tracking number, any messaging with the buyer, and the listing
   details at time of sale.

2. **Identify the claim type** from the buyer's stated reason.

3. **Assemble the evidence per type.**
   - INR: carrier delivery scan with timestamp, GPS if available, signature
     confirmation, address validation, second-attempt notes.
   - SNAD: title, bullets, main image, and dimensions as listed at sale time. Offer
     return or partial refund if appropriate.
   - Fraud: pattern, IP/device, message thread, order velocity, payment-method
     mismatch.

4. **Write the response narrative.** Factual, dated, points to the evidence by
   exhibit. No emotion, no excuses, no buyer-blame. 3 to 5 short paragraphs.

5. **Submit before the deadline.** An A-to-z claim gives the seller about 3 calendar
   days (roughly 72 hours) to respond to Amazon's request for information. confirm the
   exact countdown on the case, since Amazon has shown some variation here. A card-network
   chargeback is a separate process on the issuer's representment timeline, often a week
   or more after notification. Submit well before either deadline. extensions are not granted.

6. **Note the ODR impact.** An A-to-z lost without response counts against the
   seller's Order Defect Rate, even after refund. Defending matters for the metric,
   not just the dollars.

7. **Track the pattern.** If multiple claims fit one root cause (a carrier issue, a
   listing mismatch, a buyer behavior), fix that root cause.

8. **Run the quality check**, then deliver.

## Output format

```
## Claim Defense. [order ID]

Claim type: [INR / SNAD / Fraud]
Deadline: [date and time]

### Evidence packet
1. [exhibit] . source . what it proves
...

### Response narrative
[3 to 5 short paragraphs Amazon will read]

### Pattern check
[any recurring root cause across recent claims]
```

## Worked example

An INR claim on an FBA order. Tracking shows delivered with a GPS scan to the buyer's
address, 7 days ago. The seller's instinct was to refund and move on. Defense plan:
file the response with the delivery scan, GPS coordinates if available, and
Amazon's own delivery record (FBA orders are usually defensible because Amazon
fulfilled). Amazon's reviewers should grant the claim back to the seller because the
proof of delivery is in their own system. Total seller cost: zero, not the refund
plus a fee.

## Quality check

- The claim type is identified before any evidence is assembled.
- Evidence matches the burden of proof for that specific type.
- The response is factual and dated. no emotion, no buyer-blame.
- Submitted with time to spare before the deadline.
- Recurring patterns are flagged for a root-cause fix.

## Common mistakes

- **Auto-refunding.** Paying the chargeback plus a fee instead of defending a
  defensible claim.
- **Wrong evidence type.** Sending listing screenshots on an INR claim, or carrier
  tracking on a SNAD claim.
- **Emotional response.** A pleading or accusatory narrative gets dismissed.
- **Missing the deadline.** The A-to-z window is about 3 calendar days, no extensions. confirm the exact countdown shown on the case.
- **No pattern review.** Fighting each claim in isolation while the same root cause
  keeps producing more.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
