---
name: amz-subscribe-save
description: >-
  Plan an Amazon Subscribe and Save strategy for consumable and replenishable
  products. Decides if a product fits, sets the discount tier, and builds a plan
  to convert one-time buyers into subscribers and keep them. Use when a user
  asks about Subscribe and Save, SnS, recurring revenue on Amazon, subscription
  discounts, converting buyers into subscribers, or retention. Trigger phrases:
  "subscribe and save", "SnS", "subscription", "recurring revenue", "repeat
  buyers", "retention", "replenishment". Works with zero tools.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Subscribe and Save Strategist

Subscribe and Save turns a one-time buyer into a recurring revenue stream. For the
right product it is the most valuable program on Amazon, because a subscriber's
lifetime value dwarfs a single sale. This skill decides if a product fits and builds
the plan to grow and hold subscribers.

## When to use this

- A seller has a consumable product and is not using Subscribe and Save.
- A product has a real repeat-purchase rate (see amz-brand-analytics).
- A seller wants recurring revenue and predictable demand.
- Subscribe and Save is on but the subscriber base is not growing.

## The framework. The Subscriber Flywheel

Three turns that compound: Fit, Fund, Flywheel. Qualify the product, set the discount
that pays back over a subscriber lifetime, then convert and hold so the base grows on
its own momentum.

### Turn one. The fit test

Subscribe and Save only works for products people genuinely re-buy on a schedule. Run
the fit test:

- **Consumable or replenishable.** It runs out: coffee, supplements, pet food, razor
  blades, filters, cleaning supplies, skincare. A one-time durable purchase fails.
- **Predictable cadence.** A buyer can guess how often they need it.
- **Margin headroom.** It can absorb the subscription discount and still profit.
- **Stable demand and supply.** The seller can keep it in stock. a subscriber who
  hits an out-of-stock cancels and rarely returns.

Fail the fit test and Subscribe and Save is the wrong tool. do not force it.

### Turn two. Fund the discount

The lever you control is the seller-funded discount, set in the dashboard, commonly in
steps from 0 percent up to around 10 to 15 percent. On top of whatever you fund, Amazon
adds its own funded amount on qualifying multi-item subscription deliveries, so the
customer can see more off than you pay for. Set your seller-funded SnS discount in the
dashboard and confirm the current Amazon-funded base, since the exact split and
qualifying conditions change. The discount is the price of recurring revenue. Set it
against the math: a subscriber's lifetime value is many orders, so a slightly deeper
discount that meaningfully lifts subscriber conversion usually pays. Confirm the
discounted price still clears contribution margin on every order.

### Turn three. The flywheel. Convert and hold

- **Convert.** Make the subscribe option visible and attractive. Mention the
  replenishment angle in the listing copy and A+. A buyer does not subscribe to a
  product they do not realize they will need again.
- **Hold.** The subscriber base leaks if the product goes out of stock or quality
  slips. Protect in-stock rate above all. Plan inventory around the predictable
  subscriber baseline plus the one-time demand on top.

## Step by step

1. **Collect inputs.** The product, whether it is consumable, the price and margin,
   the repeat-purchase signal if known, and current Subscribe and Save status.

2. **Run the fit test.** If it fails, say so and stop. recommend the right tool
   instead (a bundle, a multipack).

3. **Set the discount tier.** Against the lifetime-value math, confirming every
   subscription order still clears contribution margin.

4. **Plan the convert side.** Listing and A+ copy that names the replenishment need
   and makes the subscribe option obvious.

5. **Plan the hold side.** Inventory planning around the subscriber baseline so the
   base never hits an out-of-stock.

6. **Set the metric.** Track active subscribers and the subscriber growth rate, not
   just total sales.

7. **Run the quality check**, then deliver.

## Output format

```
## Subscribe and Save Plan. [product]

### Fit test
Consumable: [y/n]   Predictable cadence: [y/n]
Margin headroom: [y/n]   Stable supply: [y/n]
Verdict: [fits / does not fit]

### Discount tier (if it fits)
Discount: [%]   Discounted price: [$]   Margin per order after: [$]

### Convert
[listing and A+ copy direction]

### Hold
[inventory plan around the subscriber baseline]

### Metric
Track: active subscribers and growth rate
```

## Worked example

A coffee brand, whole-bean bags at 18 USD.

Fit test: consumable yes, predictable cadence yes, margin headroom yes, supply stable
yes. It fits well. Discount tier: a meaningful subscription discount, since a coffee
subscriber re-orders many times a year and the lifetime value dwarfs the per-order
discount, confirmed that each subscription order still clears contribution margin.
Convert: the listing and A+ name the "never run out of coffee" angle and make the
subscribe option prominent. Hold: inventory is planned around the subscriber baseline
first, because a coffee subscriber who hits an out-of-stock cancels and switches brand.

## Quality check

- The fit test is run first. a non-consumable product is told Subscribe and Save does
  not fit.
- The discount tier is set against lifetime value, and every order still clears
  contribution margin.
- The convert plan makes the replenishment need explicit in the listing.
- The hold plan protects in-stock rate around the subscriber baseline.
- The tracked metric is active subscribers and growth, not total sales.

## Common mistakes

- **Forcing it on a durable product.** Subscribe and Save on a one-time purchase that
  nobody re-buys.
- **Discounting blindly.** Setting the discount without checking it still clears
  margin, or setting it too thin to move conversion.
- **Out-of-stock.** The fastest way to lose subscribers. an out-of-stock cancels the
  subscription and the customer rarely returns.
- **Not promoting it.** Buyers do not subscribe to a product whose listing never
  mentions they will need it again.
- **Watching total sales.** The metric is the subscriber base. it is the recurring
  revenue, and it is what predicts next month.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
