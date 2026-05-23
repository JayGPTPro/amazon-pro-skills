---
name: amz-cash-flow-forecaster-dd7
description: >-
  Forecast cash flow under Amazon's DD+7 (Delivery-Date-Based Reserve) payout
  policy. Models when funds clear, sizes the working-capital buffer the seller
  needs, and stress-tests scenarios for slow shipping or refund spikes. Use when
  a user asks about DD+7, Delivery-Date-Based Reserve, payout delays, working
  capital, cash flow under the new reserve policy, or how much cash they need
  to keep on hand. Trigger phrases: "DD+7", "payout reserve", "delivery date
  reserve", "working capital", "cash flow", "Amazon holds my money". Works with
  zero tools. the user provides sales velocity, fulfillment mix, and seasonality.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Cash Flow Forecaster (DD+7)

Amazon's DD+7 policy holds funds until 7 days after the estimated delivery date.
For sellers used to weekly biweekly payouts, this is a working-capital shock that
can leave a healthy business out of cash. This skill models the gap and sizes the
buffer.

## When to use this

- DD+7 just kicked in for the seller's account.
- Planning Q4 and worried about cash held through the peak.
- Sales are growing fast and the seller does not know if cash can keep up.
- Considering FBM or 3PL to shorten the payout cycle.

## The framework. The DD+7 Cash Cycle

Cash held by Amazon at any moment = sales of the trailing window held through
estimated delivery + 7 days. Three factors determine how much:

1. **Daily sales rate.** Higher sales = more cash in the pipeline at once.
2. **Transit time.** Faster delivery (Prime, regional FBA) clears cash sooner. Slow
   delivery (FBM, oversize, international) extends the hold.
3. **Refund and return rate.** Refunds reduce the released amount and stretch the
   effective cycle.

The buffer formula: working capital buffer roughly equals daily sales rate x
average days in the cash cycle. For an FBA seller with average 4-day transit and a
trailing 30-day window of attention, that is around 11 days of sales held at any
time. Plus seasonality. peak weeks pile up cash that releases slowly into a slower
period.

## Step by step

1. **Collect inputs.** Average daily sales (USD), fulfillment mix (FBA % vs FBM %),
   average transit time per channel, refund rate, and any known seasonal pattern.

2. **Compute the steady-state hold.** Daily sales x (transit days + 7) for each
   channel, weighted by mix.

3. **Model the peak.** Multiply daily rate by the seasonal multiplier for the peak
   weeks, recompute the hold. This is the maximum cash held mid-peak.

4. **Stress-test.** Add a refund spike scenario (+50 percent of normal rate for a
   week). Add a slow-shipping scenario (+3 transit days). Both happen in Q4.

5. **Size the buffer.** Recommend a working-capital buffer equal to the maximum
   stress-tested hold, with a small margin. This is the minimum cash on hand to
   survive the policy without short-term debt.

6. **Recommend mitigations.** Faster fulfillment, Seller-Fulfilled Prime, 3PL with
   own merchant of record, or financing facilities matched to the cycle.

7. **Run the quality check**, then deliver.

## Output format

```
## DD+7 Cash Flow Forecast. [account]

Inputs: daily sales [$], FBA [%]/FBM [%], avg transit [d], refund rate [%]

### Steady-state hold
[$ held in the pipeline at any moment]

### Peak scenario
Seasonal multiplier: [Nx]
Peak hold: [$]

### Stress-tests
Refund spike: [$ hold]
Slow shipping: [$ hold]

### Recommended buffer
Working capital buffer: [$]   Why: [the binding scenario]

### Mitigations
[faster fulfillment, SFP, 3PL, financing options]
```

## Worked example

A seller at 8,000 USD daily sales, all FBA, average 4-day transit, refund rate 8%.

Steady state: 8,000 x 11 = 88,000 USD held at any moment. Peak (Q4 at 3x): 264,000
held. Stress test with a refund spike and slow shipping: roughly 310,000. The
recommended buffer is roughly 320,000 USD of working capital, or a credit facility
matched to that ceiling. The seller had been operating on 80k of cash and was about
to be squeezed through Q4 without knowing it.

## Quality check

- Hold is computed per fulfillment channel, weighted by mix.
- The peak scenario uses a real seasonal multiplier, not a flat assumption.
- Both refund-spike and slow-shipping stress tests are run.
- The recommended buffer is the worst-case stress-tested hold, not the steady state.
- Mitigations are practical, not just "get a loan".

## Common mistakes

- **Confusing payout speed with cash speed.** Payouts may arrive on schedule and the
  business still runs out of cash, because the trailing window keeps growing.
- **Modeling steady state only.** Peak and stress are when the policy bites hardest.
- **Ignoring refunds.** A refund spike during peak compounds with the hold.
- **No mitigation plan.** Telling a seller to "have more cash" is not a plan.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
