---
name: amz-trending-products
description: >-
  Spot and evaluate trending product opportunities on Amazon, and tell a real
  trend from a fad. Reads trend signals, judges where a trend is in its curve,
  and decides whether a seller can enter in time to profit. Use when a user asks
  about trending products, hot products, viral products, jumping on a trend,
  trend spotting, or whether a product is a fad. Trigger phrases: "trending
  products", "hot products", "viral product", "is this a trend or a fad", "trend
  spotting", "should I jump on this trend". Works with zero tools.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Trending Products

A trend can build a business or bury one. Catch it early and ride it. catch it late
and you receive your inventory the week demand collapses. This skill judges where a
trend sits in its curve and whether a seller can still enter and profit.

## When to use this

- A seller sees a product taking off and wonders whether to jump in.
- Deciding if something is a durable trend or a short fad.
- Timing an entry into a rising category.
- A seller keeps arriving late to trends and getting stuck with stock.

## The framework. The Trend Curve

Every trend moves through four phases. The only question that matters is which phase
it is in now, because the seller's lead time, sourcing plus freight plus FBA check-in,
decides when their inventory actually arrives.

| Phase | Signals | Should you enter? |
|-------|---------|-------------------|
| Emerging | Early search growth, few listings, low competition | Yes, if you can verify it is real. the best entry |
| Rising | Fast search and sales growth, listings multiplying | Yes, if your lead time lands you before the peak |
| Peak | Saturated, many sellers, prices competing down | No. you arrive as it turns |
| Declining | Search falling, sellers exiting, stock dumping | No |

The trap: a product that looks irresistible is usually at Peak. By the time a trend
is obvious enough to feel safe, the window has closed. The money is in Emerging and
early Rising.

## Trend versus fad

The hardest call. A trend has a reason to last. a fad does not.

- **A trend** has an underlying driver: a lasting behavior change, a technology
  shift, a demographic change. it settles into a smaller but durable steady state.
- **A fad** is driven by novelty or a viral moment alone. it spikes and collapses to
  near zero, fast.

The test: ask why people want this. If the answer is a durable reason, it can settle
into real demand. If the answer is "it is going around right now", it is a fad, and
a fad only pays the sellers who were already in before it spiked.

## The lead-time reality check

This decides everything. Compute: today's date, plus the full lead time (sourcing,
production, freight, customs, FBA check-in). That is when the seller's inventory is
actually live. Now ask: at that future date, what phase will the trend be in?

- If the inventory lands in Emerging or Rising, the entry can work.
- If it lands in Peak or Declining, do not enter, however good it looks today.

## Step by step

1. **Collect inputs.** The product or trend, the observable signals (search growth,
   listing count, price behavior, social or news driver), and the seller's full lead
   time.

2. **Place the trend on the curve.** Emerging, Rising, Peak, or Declining, from the
   signals.

3. **Run the trend-versus-fad test.** Name the underlying driver, or name that there
   is none.

4. **Run the lead-time reality check.** Project the phase the trend will be in when
   the seller's inventory actually lands.

5. **Verdict.** Enter (Emerging or early Rising, durable driver, inventory lands in
   time), Watch (unclear, name what would confirm it), or Skip (Peak, Declining, or
   a fad, or inventory lands too late).

6. **If Enter, plan the exit too.** A trend ends. Plan the wind-down so the seller is
   not the one holding stock when demand turns.

7. **Run the quality check**, then deliver.

## Output format

```
## Trend Evaluation. [product]

### Curve position: [Emerging / Rising / Peak / Declining]
[signals]

### Trend or fad
Underlying driver: [the durable reason, or "none, this is a fad"]

### Lead-time reality check
Lead time: [weeks]   Inventory lands: [date]
Projected phase at that date: [phase]

### Verdict: [ENTER / WATCH / SKIP]
[reasoning]

### If ENTER, the exit plan
[wind-down trigger and stock target]
```

## Worked example

A product is going viral on social, search is climbing fast, and a dozen new listings
appeared this month.

Curve: Rising, possibly nearing Peak given how fast listings are multiplying. Trend
or fad: the only reason people want it is the viral moment, no durable driver. it is
a fad. Lead-time check: the seller's lead time is 10 weeks, so inventory lands in
about two and a half months. A fad rising this fast will very likely be at Peak or
Declining by then. Verdict: Skip. It feels like a sure thing today, which is exactly
the signal that the window has already closed for a new entrant with a 10-week lead
time.

## Quality check

- The trend is placed on the four-phase curve from real signals.
- The trend-versus-fad test names the underlying driver, or names its absence.
- The lead-time reality check projects the phase at the date inventory actually lands.
- The verdict is based on that future phase, not on how the trend looks today.
- An Enter verdict includes an exit and wind-down plan.

## Common mistakes

- **Entering at Peak.** A trend that looks safe and obvious is usually already
  saturated.
- **Ignoring lead time.** Judging the trend by today's phase, not the phase it will
  be in when the inventory lands.
- **Mistaking a fad for a trend.** Sourcing a viral novelty that collapses before the
  units arrive.
- **No exit plan.** Riding a trend up with no plan for the turn, and holding the
  stock when demand falls.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
