---
name: amz-ppc-campaign
description: >-
  Build or audit Amazon Sponsored Products campaigns, and layer dayparting on
  mature accounts. Mode A builds a campaign structure from scratch with keyword
  groups, match types, and starting bids from product margins. Mode B audits
  existing campaigns from a search term report and returns bid changes,
  negatives, and a graduation plan. An advanced dayparting appendix schedules
  bids and budgets by hour and day for accounts with enough data. Use when a
  user asks to build PPC campaigns, structure Sponsored Products, set ad bids,
  audit a campaign, fix ACoS, plan an auto and exact campaign structure, or
  dayparting, bid scheduling, ad scheduling by time of day, peak shopping
  hours, or wasted ad spend at low hours. Trigger phrases. "PPC campaign",
  "sponsored products", "campaign structure", "set bids", "audit my ads", "fix
  my ACoS", "auto and exact campaigns", "dayparting", "bid scheduling", "ad
  schedule", "time of day bidding", "peak hours", "budget by hour". Works with
  zero tools. the user provides margins, keywords, or a search term report.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# PPC Campaign Builder

Sponsored Products is the engine of most Amazon ad accounts. Built right, it is a
funnel that discovers keywords and then harvests them profitably. Built wrong, it is
one giant auto campaign quietly losing money. This skill builds the funnel or audits
the one you have, and adds dayparting as an advanced layer once the structure is
sound and the data is thick enough to justify it.

## When to use this

- A new product is launching and needs a Sponsored Products structure from scratch.
- An existing PPC account has no funnel, just one auto campaign that never scales.
- ACoS is high and a search term report is sitting unread.
- Bids were set by guess and the seller wants them tied to margin.
- A seller wants a repeatable structure across multiple SKUs.

## Two modes

- **Mode A. Build.** A new product, no campaigns yet. Output: a campaign structure.
- **Mode B. Audit.** Campaigns exist. Output: bid changes, negatives, graduations.

## The framework. The Discovery to Harvest Funnel

Sponsored Products works as a three-campaign funnel. keywords flow left to right as
they prove themselves.

```
DISCOVER            TEST               HARVEST
Auto campaign  -->  Broad/phrase   -->  Exact-match
finds terms         campaign            campaign
                    confirms intent     scales the winners
```

- **Discover.** An auto campaign. Amazon matches your product to search terms you
  did not think of. The search term report is the gold.
- **Test.** Promising terms from Discover go into a broad or phrase campaign to
  confirm they convert with real intent.
- **Harvest.** Terms that convert in Test graduate to an exact-match campaign with
  higher bids. this is the profit engine. As a term graduates, it is added as a
  negative in the campaign it came from, so the funnel does not bid against itself.

## The bid math

Every bid traces back to margin.

- **Break-even ACoS** equals contribution margin divided by price. the most an ad can
  cost before the unit loses money.
- **Target ACoS** is set below break-even for Harvest (you want profit) and may be at
  or above break-even for Discover (you are buying keyword data).
- **Max CPC** roughly equals price, times target ACoS, times expected conversion rate.
  starting bids come from this, not from a guess.

## Step by step. Mode A, Build

1. Collect price, contribution margin, the keyword set (or run keyword logic), and
   the product phase.
2. Compute break-even ACoS, target ACoS per funnel stage, and starting Max CPC.
3. Build the three campaigns: one auto for Discover, one broad or phrase for Test,
   one exact for Harvest, seeded with the strongest known keywords.
4. Group keywords and set match types and starting bids from the bid math.
5. Define the negative-keyword isolation so the three campaigns do not compete.

## Step by step. Mode B, Audit

1. Collect the search term report and campaign data: spend, clicks, orders, sales,
   ACoS per term, plus target ACoS.
2. Set the bid action for each term that sells: raise bid (converts below target
   ACoS), or lower bid (converts above target ACoS but still sells).
3. Sort the rest into negate, keep-and-graduate, or wait. For the full negate/keep/
   graduate decision tree (the drain threshold, exact versus phrase negatives, and
   protecting converting terms from a careless phrase negative), see
   amz-negative-keywords.
4. Apply negative isolation for every graduated term, so the funnel does not bid
   against itself.
5. Produce a week-by-week action plan.

## Output format

```
## PPC Plan. [product] . Mode [A/B]

Break-even ACoS: [%]   Target ACoS: Harvest [%] / Discover [%]

### Mode A. Structure
Discover (auto): [budget, starting bid]
Test (broad/phrase): [keyword groups, bids]
Harvest (exact): [seed keywords, bids]
Negative isolation: [rules]

### Mode B. Actions
Raise bid: [terms, new bids]
Lower bid: [terms, new bids]
Negate: [terms]
Graduate to exact: [terms]
Week-by-week plan: ...
```

## Worked example

Product 30 USD, contribution margin 12. Break-even ACoS 40 percent.

Mode A: target ACoS 25 percent for Harvest, 50 percent allowed for Discover. Three
campaigns. auto for discovery, broad for testing, exact for the 8 strongest known
keywords with bids set from a Max CPC of roughly 30 x 0.25 x conversion rate. Each
exact keyword is negated in the auto and broad campaigns so the funnel does not
bid against itself.

## Quality check

- Break-even ACoS is computed from margin, and target ACoS differs by funnel stage.
- The structure is a Discover, Test, Harvest funnel, not one campaign.
- Every graduated keyword is negated in its source campaign. no internal competition.
- Bids trace to the Max CPC math, not a flat guess.
- Mode B decisions distinguish raise, lower, negate, and wait. low-click terms wait.

## Common mistakes

- **One giant auto campaign.** Discovery with no harvest. it never scales the winners.
- **No negative isolation.** The auto, broad, and exact campaigns bid against each
  other for the same term and inflate the cost.
- **Flat bids.** One bid across all keywords ignores that they convert differently.
- **Never graduating.** Winners left in the broad campaign forever instead of moving
  to a higher-bid exact campaign.
- **Judging Discover by Harvest ACoS.** Discovery buys keyword data. it is allowed to
  run hotter.

---

## Advanced. Dayparting

Once the funnel is built and a healthy data stream exists, the next lever is
dayparting. shifting bids and budgets toward the hours that convert and away from
the hours that drain. This is an optimization on top of the funnel, not a
substitute for it.

### Data-quality gate

Before doing any of this, the account must clear two bars. **At least 4 weeks of
hour-and-day performance data** and **enough daily spend that hour-level slices have
meaningful click volume** (rule of thumb. if a typical hour has under 5 clicks across
the data window, treat it as noise). Below that, dayparting is acting on noise.
skip it, fix structure and bids first, come back when the data is thick enough.

If only day-of-week data is reliable, daypart by day, not hour. group thin hours
into wider windows (morning, afternoon, evening, overnight) until each window has
enough clicks to trust.

### The Hour Value Map

Dayparting is built from the account's own hour-by-day conversion, not from
intuition.

1. **Score every time block.** For each hour, or each hour-and-weekday block,
   compute conversion rate and ACoS. Rank blocks into three tiers:
   - **Prime.** Conversion above the daily average and ACoS at or below target.
   - **Standard.** Around the daily average.
   - **Drain.** Conversion well below average or ACoS far above target.

2. **Assign a bid posture per tier.**
   - Prime: bid up, plus 15 to 30 percent. this is where budget should land.
   - Standard: baseline bid.
   - Drain: bid down 30 to 50 percent, or pause entirely.

3. **Protect the budget for Prime.** The point of cutting Drain hours is so the
   daily budget survives until the Prime hours arrive. A budget that empties at noon
   never reaches the evening peak. reallocate, do not just cut.

### Dayparting step by step

1. Confirm the data-quality gate (4+ weeks, sufficient hourly clicks).
2. Score every block (or window) into Prime, Standard, Drain.
3. Build the bid-adjustment schedule.
4. Reallocate the freed budget into Prime. net spend can stay flat while results
   improve.
5. Set a monthly re-score cadence. dayparting drifts with seasons and promotions.

### Dayparting worked example

A storefront product with 6 weeks of data. Overnight 0 to 6 AM converts at one
third the daily average with ACoS double the target. Evening 6 to 10 PM converts
well above average at target ACoS. Schedule: pause or cut overnight 40 percent.
raise evening bids 25 percent. The daily budget no longer drains before the
evening peak. net spend roughly flat, orders up, ACoS down.

### Dayparting common mistakes

- **Dayparting too early.** Acting on a few days of data, or on hour buckets with
  3 clicks each. that is hunch-driven, not data-driven.
- **Dayparting on a hunch.** "Everyone shops at night" is not this account's data.
- **Cutting without reallocating.** Cutting Drain hours and pocketing the budget,
  instead of moving it to Prime where it earns more.
- **Set and forget.** A schedule built in Q1 is wrong by Q4. re-score monthly.
- **Ignoring day of week.** Weekends and weekdays often convert differently. a
  day-of-week layer matters as much as the hour layer.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
