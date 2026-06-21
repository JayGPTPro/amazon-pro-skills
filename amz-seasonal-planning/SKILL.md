---
name: amz-seasonal-planning
description: >-
  Build an Amazon seasonal and Q4 plan. Works backward from peak demand dates to
  set inventory order timing, ad budget ramps, deal calendar, listing refresh,
  and the post-peak wind-down. Use when a user asks about seasonal planning, Q4
  preparation, Prime Day prep, holiday selling, peak season inventory, or timing
  a seasonal product. Trigger phrases: "seasonal planning", "Q4 plan", "holiday
  prep", "prime day prep", "peak season", "seasonal product", "black friday".
  Works with zero tools.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Seasonal Planner

Seasonal selling is won or lost months before the peak. The inventory order, the
listing refresh, the ad ramp. all of it has a deadline that sits well before the
demand. This skill builds the plan by working backward from the peak date.

## When to use this

- Preparing for Q4, Prime Day, Prime Big Deal Days, or a category-specific season.
- A seller has a seasonal product and needs a timing plan.
- A past peak was missed because inventory or ads were not ready.
- Planning the wind-down so the season does not end in long-term storage fees.

## The framework. The Backward Timeline

Never plan a season forward from today. Plan it backward from the peak. Fix the peak
date, then place every milestone at its required lead time before it.

```
                                              <-- PEAK DEMAND
                                  T-2 to 4 weeks   Ad budget ramps to maximum
                          T-3 to 6 weeks           Deal and coupon submissions
                  T-4 to 8 weeks                   Listing refresh live, indexed
          T-6 to 10 weeks                          Inventory checked in at FBA
  T-3 to 5 months                                  Inventory purchase order placed
```

The single hardest deadline is the inventory order. It carries the full lead time:
production, freight, customs, and FBA check-in. Miss it and nothing else matters,
because there is nothing to sell at the peak.

## The two Prime events. handle them separately

Amazon now runs two major Prime events each year, and sellers conflate them all
the time. They have different prep windows, different inventory leads, and
different ad warmup curves. The exact dates move every year, and Amazon has
shifted them before (the summer event has landed in June in some years, July in
others). Never hard-code a date. confirm the exact dates for the current year
in Seller Central, then apply the lead times below relative to that date.

### The summer Prime event

The flagship event, historically mid-year (it has fallen in June or July
depending on the year). Treat its date as a moving target and confirm it each
year. Working backward from the confirmed date: deal submissions close roughly
8 to 10 weeks ahead, inventory should be checked in by about 2 to 3 weeks
before, the listing refresh should be live and indexed by about 2 to 3 weeks
before, and the ad budget ramps through the two weeks into the event. The event
runs hot. expect peak CPCs and a sharp demand spike on enrolled deals.

### The fall Prime event (Prime Big Deal Days)

The fall counterpart, positioned as the kickoff to Q4. Historically lands in
early to mid October, but Amazon confirms it closer to the event, so verify the
date each year rather than assuming. Working backward from the confirmed date:
deal submissions close roughly 8 to 10 weeks ahead, inventory checked in by
about 3 weeks before, the listing refresh live and indexed by about 2 to 3
weeks before, and the ad budget ramping through the week into the event.

Critical differences from the summer event. The fall event sits inside the
broader Q4 ramp, so the ad warmup is longer (the demand curve begins building
weeks ahead) and the wind-down is shorter (it bleeds straight into Black Friday
and Cyber Monday prep, not into a quiet month). Inventory lead time is also
tighter for sellers with overseas freight, because the fall event lands during
the same window when Q4 holiday inventory is moving on the same routes.
Order earlier.

A seller running both events does not run the same plan twice. Different prep
windows, different inventory PO dates, different ad warmup, and the fall event
must hand off cleanly to the November and December peaks without leaving
the listing depleted.

This skill is the broad annual timeline. For the deep Q4 work, the week-by-week
reorder calendar, per-SKU peak velocity multipliers, inbound delay buffers, and
FBM fallback triggers, hand off to amz-q4-restock-war-room.

## The five workstreams

1. **Inventory.** Order quantity from a seasonal demand forecast, not the flat
   monthly rate. Peak demand can be several times the baseline. Order against the
   peak, with the lead time backward from check-in. Plan the post-peak quantity down
   so the season does not end in excess stock and long-term storage fees.

2. **Listing.** A seasonal refresh: gift-angle copy, seasonal main or gallery images,
   seasonal keywords added to the backend. It must be live and indexed weeks before
   the peak, because indexing and ranking take time.

3. **Ads.** Ramp the budget up as demand builds, peak it through the event, and do
   not cut it the instant the event ends. there is a tail. Expect higher CPCs in peak
   season and budget for them.

4. **Deals.** Lightning Deals, Best Deals, and coupons for peak events have
   submission deadlines weeks ahead. Miss the submission window and the deal cannot
   run. see amz-deal-finder.

5. **Wind-down.** After the peak, plan the price and ad taper and the inventory
   position so leftover stock does not sit into the long-term storage fee window.

## Step by step

1. **Collect inputs.** The product, the peak date or event, the baseline sales rate,
   the expected seasonal multiplier, the full inventory lead time, and current stock.

2. **Fix the peak date** and build the backward timeline.

3. **Forecast peak demand.** Baseline rate times the seasonal multiplier across the
   peak window. This drives the inventory order quantity.

4. **Place every milestone** on the timeline at its lead time before the peak. Flag
   any milestone whose deadline has already passed or is close.

5. **Plan the wind-down.** Post-peak taper and a stock position that avoids long-term
   storage fees.

6. **Run the quality check**, then deliver.

## Output format

```
## Seasonal Plan. [product] . peak: [date or event]

### Demand forecast
Baseline: [units/period]   Multiplier: [Nx]   Peak window need: [units]

### Backward timeline
[date] . inventory PO placed
[date] . inventory checked in at FBA
[date] . listing refresh live and indexed
[date] . deal and coupon submissions
[date] . ad budget at peak
PEAK: [date]
[date] . wind-down begins

### Deadline flags
[any milestone already passed or imminent]

### Wind-down
[price and ad taper, stock target to avoid long-term storage fees]
```

## Worked example

A gift product, peak December, baseline 300 units a month, expected 4x in the peak
window. Inventory lead time 12 weeks total.

Backward from a mid-December peak: the inventory purchase order must be placed by
about September to check in by late October or early November. The listing's gift
refresh should be live by late October so it indexes. Deal submissions for the
November and December events close weeks earlier than sellers expect. the ad budget
ramps through November and holds into late December. Wind-down begins after the peak
with a price taper and a stock target low enough to avoid the long-term storage fee
window. The seller had been planning to order in October. that would have missed
the entire season.

## Quality check

- The plan is built backward from the peak date, not forward from today.
- The inventory order quantity uses a seasonal multiplier, not the flat monthly rate.
- The inventory order deadline accounts for the full lead time including FBA check-in.
- The listing refresh is scheduled early enough to index before the peak.
- Deal submission deadlines are placed weeks ahead of the events.
- A wind-down plan avoids ending the season in long-term storage fees.
- Any already-passed or imminent deadline is flagged.

## Common mistakes

- **Planning forward.** Working from today instead of backward from the peak, and
  discovering the inventory deadline has passed.
- **Ordering against the baseline.** Stocking for the normal month and selling out
  on day two of the peak.
- **Late listing refresh.** A seasonal listing that goes live too late to index and
  rank before the peak.
- **Missing deal deadlines.** Deal submissions close far earlier than the events.
- **No wind-down.** Over-ordering for the peak and paying long-term storage fees on
  the leftovers all year.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
