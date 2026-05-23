---
name: amz-3pl-vs-fba-decision
description: >-
  Compare FBA, 3PL with FBM, and Seller-Fulfilled Prime (SFP) economics per SKU.
  Factors fees, the Prime badge, Buy Box impact, DD+7 cash flow effect, and
  flexibility. Returns the right fulfillment choice. Use when a user asks about
  FBA vs FBM, 3PL, SFP, switching fulfillment, reshoring, or dual-channel
  fulfillment. Trigger phrases: "FBA vs FBM", "3PL", "SFP", "seller fulfilled
  prime", "switch fulfillment", "dual channel". Works with zero tools.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# 3PL vs FBA Decision

Sellers are reshoring to 3PL+SFP to dodge FBA fees and DD+7 cash holds. The decision
is not cost alone. The Prime badge, Buy Box share, and operational complexity all
move with the choice. This skill compares per SKU.

## When to use this

- A SKU's FBA fees feel high enough to question the channel.
- DD+7 cash hold is straining working capital.
- Considering SFP and want a clear-eyed comparison.
- A subset of SKUs (heavy, slow, oversized) may belong elsewhere.

## The framework. The Three Channels

Per SKU, model three options.

### FBA

- Fulfillment fee + storage + inbound. Default channel.
- Prime badge automatic. Buy Box advantage. fastest delivery promise.
- Cash holds 11+ days under DD+7.

### 3PL + FBM (no Prime)

- Pick/pack/labor + carrier outbound + warehousing.
- No Prime badge unless SFP. Buy Box disadvantage on shared listings.
- Cash payouts faster (Amazon transfers, not DD+7 reserve).

### Seller-Fulfilled Prime (SFP)

SFP is gated. sellers must qualify through a 30-day trial with tight performance
bars (on-time delivery 93%+, valid tracking 99%+, cancellation rate under 0.5%),
and Amazon periodically closes new enrollment. Confirm eligibility before treating
SFP as a real option.

- Pick/pack/labor + carrier outbound (paid, premium speed) + warehousing.
- Prime badge. Buy Box parity with FBA.
- Strict SFP performance bar (on-time delivery, cancellation rate).
- Cash payouts faster than FBA.

The right choice usually splits the catalog: FBA for fast small movers, 3PL for
oversize/heavy/slow, SFP for premium movers worth the operational rigor.

## Step by step

1. **Collect inputs.** Per SKU: price, unit cost, dimensions and weight, current
   FBA fee stack, expected 3PL or self-fulfillment cost (pick/pack/labor + carrier
   + warehousing), velocity, current Buy Box share.

2. **Compute net per channel.** Profit per unit through FBA, through 3PL+FBM, and
   through SFP (with the carrier cost premium for fast delivery).

3. **Layer the badge effect.** 3PL+FBM (no Prime) on a shared listing typically
   loses 30-60 percent of Buy Box. Multiply effective sales accordingly.

4. **Factor cash.** DD+7 hold under FBA is a real working-capital cost (see
   amz-cash-flow-forecaster-dd7).

5. **Check SFP eligibility.** SFP has a performance bar. if the seller cannot meet
   it, it is not on the table.

6. **Pick per SKU.** Often: FBA for the bulk, 3PL for oversized or slow-moving,
   SFP for select premium SKUs.

7. **Run the quality check**, then deliver.

## Output format

```
## Fulfillment Choice. [SKU]

### Per-unit profit by channel
FBA:           [$]
3PL + FBM:     [$]   (with [%] Buy Box share factor)
SFP:           [$]   (eligibility: [yes/no])

### Cash impact
FBA cash held per unit: [$ days held]
3PL/SFP cash velocity: [days faster]

### Recommendation: [channel]
[reasoning, including badge and cash factors]
```

## Worked example

A 4-pound product, $40 price, $9 cost. FBA total fees: $14, profit $17. 3PL+FBM:
total ops $7, but on a shared listing Buy Box share drops to ~40%, so effective
profit per ordered unit is higher but units fall, net annualized: lower. SFP:
ops $9 (carrier + labor), Prime badge holds, Buy Box stays at FBA-equivalent,
profit per unit $22 vs FBA's $17, and DD+7 hold is avoided saving working capital.
Recommendation: SFP for this SKU if the seller can meet the SFP performance bar.
FBA stays as a fallback.

## Quality check

- Per-channel profit is computed from real numbers, including 3PL ops cost.
- The Buy Box-share haircut for non-Prime FBM is factored, not assumed equal.
- SFP eligibility and the performance bar are checked, not assumed.
- DD+7 cash hold is treated as a real cost.
- The decision is per SKU, not a flat catalog policy.

## Common mistakes

- **Comparing on fees alone.** A "cheaper" 3PL+FBM channel can deliver less profit
  if Buy Box share drops.
- **Assuming SFP eligibility.** Many sellers cannot consistently meet the SFP
  performance bar and shouldn't choose it.
- **Switching the whole catalog.** The right answer is usually a split, not a flag.
- **Ignoring the operational tax.** 3PL and SFP are work. the financial savings
  must beat the operational cost.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
