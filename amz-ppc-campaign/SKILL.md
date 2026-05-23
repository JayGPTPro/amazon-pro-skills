---
name: amz-ppc-campaign
description: >-
  Build or audit Amazon Sponsored Products campaigns. Mode A builds a campaign
  structure from scratch with keyword groups, match types, and starting bids
  from product margins. Mode B audits existing campaigns from a search term
  report and returns bid changes, negatives, and a graduation plan. Use when a
  user asks to build PPC campaigns, structure Sponsored Products, set ad bids,
  audit a campaign, fix ACoS, or plan an auto and exact campaign structure.
  Trigger phrases: "PPC campaign", "sponsored products", "campaign structure",
  "set bids", "audit my ads", "fix my ACoS", "auto and exact campaigns". Works
  with zero tools. the user provides margins, keywords, or a search term report.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# PPC Campaign Builder

Sponsored Products is the engine of most Amazon ad accounts. Built right, it is a
funnel that discovers keywords and then harvests them profitably. Built wrong, it is
one giant auto campaign quietly losing money. This skill builds the funnel or audits
the one you have.

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
2. For each term, decide: raise bid (converts below target ACoS), lower bid (converts
   above target ACoS but still sells), negate (drains with no sales), or wait (too
   few clicks).
3. List the converting Discover and Test terms to graduate to the exact campaign.
4. Apply negative isolation for every graduated term.
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

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. 50 production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
