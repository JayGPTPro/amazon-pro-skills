---
name: amz-dayparting-strategy
description: >-
  Build an Amazon PPC dayparting strategy. schedules bids and budgets by hour of
  day and day of week so spend concentrates when shoppers convert and pulls back
  when they do not. Reads the user's hour-and-day performance data and outputs a
  bid-adjustment schedule. Use when a user asks about dayparting, bid scheduling,
  ad scheduling by time of day, peak shopping hours, or wasted ad spend at low
  hours. Trigger phrases: "dayparting", "bid scheduling", "ad schedule", "time
  of day bidding", "peak hours", "budget by hour". Works with zero tools. the
  user pastes hourly or daily performance data.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Dayparting Strategy

Not every hour converts the same. A click at 2 AM from a half-asleep browser is not
worth a click at 8 PM from a buyer with a cart open. Dayparting moves ad budget
toward the hours that convert and away from the hours that drain. This skill builds
the schedule from the seller's own data.

## When to use this

- An account spends evenly around the clock but conversion clearly is not even.
- A daily budget runs out by mid-afternoon and misses the evening peak.
- ACoS is acceptable on average but the seller suspects bad hours hide inside it.
- A seller wants to scale spend without raising ACoS.

## The framework. The Hour Value Map

Dayparting is not "advertise in the evening". It is built from the account's own
hour-by-day conversion. Three steps.

1. **Score every time block.** For each hour, or each hour-and-weekday block if data
   allows, compute conversion rate and ACoS. Rank blocks into three tiers:
   - **Prime.** Conversion above the daily average and ACoS at or below target.
   - **Standard.** Around the daily average.
   - **Drain.** Conversion well below average or ACoS far above target.

2. **Assign a bid posture per tier.**
   - Prime: bid up, plus 15 to 30 percent. this is where budget should land.
   - Standard: baseline bid.
   - Drain: bid down 30 to 50 percent, or pause entirely.

3. **Protect the budget for Prime.** The point of cutting Drain hours is so the daily
   budget survives until the Prime hours arrive. A budget that empties at noon never
   reaches the evening peak.

## Step by step

1. **Collect inputs.** Hourly or day-of-week performance: spend, clicks, orders, sales
   per block. The longer the data window, the more reliable. Ask for at least 2 to 4
   weeks. If only day-of-week data exists, daypart by day, not hour.

2. **Check the data is enough.** A block with very few clicks is noise. Group thin
   hours into wider windows (for example morning, afternoon, evening, overnight)
   until each window has enough clicks to trust.

3. **Score every block** into Prime, Standard, or Drain.

4. **Build the schedule.** Map each block to a bid adjustment. Produce a clear
   hour-by-hour or window-by-window table.

5. **Reallocate, do not just cut.** The budget freed from Drain hours funds higher
   bids in Prime hours. Net spend can stay flat while results improve.

6. **Set a review cadence.** Dayparting drifts. shopping patterns shift with seasons
   and promotions. Recommend a monthly re-score.

7. **Run the quality check**, then deliver.

## Output format

```
## Dayparting Schedule. [account or campaign]

Data window: [dates]   Granularity: [hourly / window / day-of-week]

### Time block scores
[block] . conv rate . ACoS . tier . bid adjustment
...

### Schedule
Prime blocks: [list] . +[%]
Standard blocks: [list] . baseline
Drain blocks: [list] . -[%] or pause

### Net effect
[expected change in spend, ACoS, and orders]
Re-score: [cadence]
```

## Worked example

A storefront product. Overnight 0 to 6 AM converts at one third the daily average
with ACoS double the target. Evening 6 to 10 PM converts well above average at
target ACoS.

Schedule: pause or cut overnight 40 percent. raise evening bids 25 percent. The daily
budget no longer drains before the evening peak, so the account captures the hours
that actually convert. Net spend roughly flat, orders up, ACoS down.

## Quality check

- Time blocks are scored from the account's own conversion and ACoS, not assumptions.
- Thin-data hours are grouped into wider windows until each is statistically usable.
- The schedule reallocates budget from Drain to Prime, it does not only cut.
- The budget logic ensures Prime hours are reached before the daily budget empties.
- A re-score cadence is set, because dayparting drifts.

## Common mistakes

- **Dayparting on a hunch.** "Everyone shops at night" is not this account's data.
- **Acting on noise.** Calling a 3-click hour a Drain hour. group thin hours first.
- **Cutting without reallocating.** Cutting Drain hours and pocketing the budget,
  instead of moving it to Prime where it earns more.
- **Set and forget.** A schedule built in Q1 is wrong by Q4. re-score monthly.
- **Ignoring day of week.** Weekends and weekdays often convert differently. a
  day-of-week layer matters as much as the hour layer.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. 50 production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
