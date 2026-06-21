---
name: amz-buy-box
description: >-
  Diagnose why a listing is losing the Amazon Buy Box (Featured Offer) and build a
  plan to win it back. Covers seller-health signals, pricing relative to the
  competing offer, fulfillment method, stock, and account metrics. Use when a
  user asks why they lost the Buy Box, how to win the Featured Offer, why a
  reseller is beating them, or why their own listing shows another seller's
  offer. Trigger phrases: "buy box", "featured offer", "lost the buy box",
  "win the buy box", "buy box percentage", "another seller has my listing".
  Works with zero tools. the user describes the offer and account state.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Buy Box Recovery

The Buy Box, now called the Featured Offer, is the Add to Cart button. Lose it and
your sales on that listing fall by most of their volume even though the listing looks
fine. This skill finds the exact reason you lost it and builds the recovery plan.

## When to use this

- Sales on a listing dropped sharply but traffic did not.
- The detail page shows another seller's offer as the Featured Offer.
- Buy Box percentage in Business Reports has dropped meaningfully, especially below
  what it normally holds for this listing.
- A reseller appeared on your listing and is taking the sale.

## The framework. The Five Buy Box Gates

Amazon picks the Featured Offer by scoring offers on a set of signals Amazon does
not fully publish. A practical simplification is five gates. Diagnose in this order.
the first failed gate is usually the cause.

1. **Eligibility.** Is the account in good standing and the offer Buy Box eligible?
   A suppressed account or an ineligible category wins zero Buy Boxes regardless of
   price. Check first.
2. **Fulfillment.** FBA and Seller-Fulfilled Prime score far higher than standard
   merchant fulfillment. A standard FBM offer loses to an FBA offer at the same price.
3. **Price to customer.** Amazon scores the landed price, item plus shipping. An offer
   priced above the lowest reasonable offer can lose the box even with great metrics.
   This includes losing the box to yourself by being priced above Amazon's fair-price
   threshold.
4. **Account health.** Late shipment rate, order defect rate, cancellation rate, and
   valid tracking rate. Weak metrics push your offer down even when price is good.
5. **Stock and reliability.** Low or zero stock, slow handling time, and inconsistent
   delivery speed all reduce the score.

## Step by step

1. **Collect inputs.** Is this your own branded listing or a shared one. your
   fulfillment method and the competing offer's method. your price and the competing
   price including shipping. your account health metrics. your stock level and
   handling time. Ask one compact follow-up for whatever is missing.

2. **Walk the five gates in order.** Stop at the first gate you fail. that is the
   primary cause. Note any secondary failures.

3. **Brand-owner check.** If this is your own brand and a reseller is on the listing,
   the issue is usually unauthorized resale. The fix is Brand Registry, a pricing and
   distribution policy, and removing unauthorized sellers, not a price war.

4. **Price-suppression check.** If you are the only seller and still have no Buy Box,
   your price is above Amazon's fair-price threshold. The fix is lowering to a
   reasonable price or correcting a reference-price issue, not adding sellers.

5. **Build the recovery plan.** One primary action for the failed gate, plus the
   secondary fixes, each with the expected time to recover.

6. **Run the quality check**, then deliver.

## Output format

```
## Buy Box Diagnosis. [ASIN or product]

Listing type: [own brand / shared]
Primary cause: [failed gate]
Secondary issues: [list]

### Recovery plan
1. [primary action] . expected recovery: [time]
2. [secondary action] ...

### If this is your brand
[reseller / brand-protection guidance, if relevant]

### Watch
[the metric to monitor to confirm recovery]
```

## Worked example

Own-brand listing, sales down 70 percent, traffic flat. Seller is FBA, price
unchanged, account health green. Gate 1 to 4 all pass. The detail page shows no
Featured Offer at all.

Diagnosis: Gate 3, price suppression. The listing price was raised above Amazon's
fair-price threshold after a competitor on a similar product dropped. Fix: lower to a
reasonable price or fix the reference-price flag in the listing. Buy Box typically
returns within 24 hours of the price correction.

## Quality check

- The five gates were walked in order and the first failure is named as primary.
- Own-brand reseller cases are handled with brand protection, not a price war.
- Single-seller no-Buy-Box cases are correctly diagnosed as price suppression.
- Every action has an expected recovery time.
- The plan names the metric to watch to confirm the box is back.

## Common mistakes

- **Dropping price blindly.** If the failed gate is account health or fulfillment, a
  lower price does not bring the box back. it just cuts margin.
- **Ignoring price suppression.** Sellers assume they need a competitor to lose the
  box. you can lose it to nobody by pricing too high.
- **Fighting resellers on price.** A race to the bottom on your own brand. the real
  fix is Brand Registry and a distribution policy.
- **Missing handling time.** A slow handling time quietly lowers the score even when
  price and health look fine.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
