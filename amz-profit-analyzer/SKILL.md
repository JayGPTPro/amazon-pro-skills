---
name: amz-profit-analyzer
description: >-
  Analyze true Amazon profitability per ASIN and across a portfolio. Goes beyond
  per-unit fees to include advertising, returns, storage, promotions, and hidden
  fees, and finds where the real money is made and lost. Use when a user asks
  about profitability, true net profit, which products make money, why profit is
  lower than expected, portfolio profit analysis, or hidden fees eating margin.
  Trigger phrases: "profit analysis", "true profit", "net margin", "which
  products are profitable", "where is my money going", "hidden fees". Works with
  zero tools. the user pastes revenue, fee, and cost figures.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Profit Analyzer

A product can sell well and still lose money. Per-unit fee math (see amz-fba-calculator)
tells you if a single unit is profitable. This skill goes wider: it analyzes real
profitability per ASIN and across the catalog, including the costs that only show up
at the account level, and finds where the money actually goes.

## When to use this

- Sales are strong but the bank balance is not growing.
- A seller wants to know which products carry the business and which drain it.
- Profit came in far below the per-unit math's promise.
- Deciding which SKUs to scale, fix, or cut.

## The framework. The Profit Waterfall

True profit is revenue minus seven layers. The per-unit calculators stop at layer 3.
the money usually leaks in layers 4 to 7.

```
Gross revenue
  minus  Amazon selling fees   (referral, fulfillment)
  minus  Cost of goods         (landed: factory + freight + duty)
  minus  Storage               (monthly + long-term storage fees)
  minus  Advertising           (the real ad spend attributed to the SKU)
  minus  Returns and refunds   (refunded amount + lost units + return processing)
  minus  Promotions            (coupons, deals, deal fees, discounts)
  minus  Hidden and overhead   (removal fees, reimbursements net, chargebacks, software, VA)
  =      True net profit
```

Run the waterfall per ASIN. The pattern across the catalog tells the story: a few
SKUs usually carry the business, several are break-even, and one or two quietly lose
money while looking busy.

## The leak finder

For each SKU, compute each layer as a percent of that SKU's revenue. The layer that
is abnormally large versus the rest of the catalog is the leak:

- Advertising far above the catalog norm. an ad-dependent SKU, the listing or
  conversion is weak.
- Returns far above the norm. a product, sizing, or expectation problem.
- Storage far above the norm. overstock or a slow mover, possibly facing long-term
  storage fees.
- Promotions far above the norm. discounting that has become a permanent crutch.

## Step by step

1. **Collect inputs.** Per ASIN where possible: units sold, revenue, Amazon fees,
   landed cost, ad spend, returns, storage, promotion costs, and any account-level
   overhead to allocate.

2. **Run the waterfall per ASIN.** Produce true net profit and true net margin for
   each, not just for the catalog total.

3. **Rank the catalog.** Sort SKUs by true net profit. Identify the carriers, the
   break-even SKUs, and any loss-makers.

4. **Run the leak finder** on each SKU. Name the abnormal layer.

5. **Recommend per SKU.** Scale the carriers, fix the named leak on the break-even
   SKUs, and decide cut or fix on the loss-makers.

6. **Surface the hidden layer.** Account-level costs sellers forget. removal fees,
   long-term storage, reimbursement gaps, software, labor. Allocate and show them.

7. **Run the quality check**, then deliver.

## Output format

```
## Profit Analysis. [catalog or ASIN]

### Per-ASIN waterfall
[ASIN] . revenue . fees . COGS . storage . ads . returns . promo . overhead . NET . margin%
...

### Catalog ranking
Carriers: [SKUs and their net]
Break-even: [SKUs]
Loss-makers: [SKUs]

### Leaks
[SKU] . abnormal layer . [the leak and the fix]
...

### Recommendations
Scale: ...   Fix: ...   Cut or rework: ...
```

## Worked example

A 6-SKU catalog looks healthy on revenue. The waterfall shows SKU C, the best seller
by units, runs ad spend at 31 percent of its revenue while the catalog norm is 14.
Its true net margin is 2 percent. SKU C is not a winner, it is a treadmill. the
listing converts poorly and only ad spend keeps it moving.

Recommendation: do not scale SKU C. Fix the conversion leak first (listing and
images). Two other SKUs are the real carriers and deserve the ad budget that SKU C
is burning.

## Quality check

- The full seven-layer waterfall is run, including ads, returns, promo, and overhead.
- Profit is computed per ASIN, not only as a catalog total.
- Each SKU's layers are compared as a percent of revenue to find the abnormal one.
- Loss-making SKUs are identified explicitly, even if they sell well by units.
- Account-level hidden costs are allocated and shown, not ignored.
- Each SKU gets a scale, fix, or cut recommendation.

## Common mistakes

- **Stopping at per-unit fees.** The per-unit math says a SKU is fine while ads,
  returns, and promos make it a loss.
- **Catalog-total thinking.** A healthy total can hide a SKU bleeding money.
- **Confusing units with profit.** The best seller by volume can be the worst by
  margin.
- **Ignoring overhead.** Removal fees, long-term storage, software, and labor are
  real and rarely allocated.
- **Scaling a treadmill.** Pouring budget into a SKU that only moves because of ad
  spend.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
