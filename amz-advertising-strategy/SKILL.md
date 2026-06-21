---
name: amz-advertising-strategy
description: >-
  Design a portfolio-level Amazon advertising strategy across Sponsored Products,
  Sponsored Brands, and Sponsored Display. Sets the TACoS target, splits budget by
  funnel stage, defines the role of each campaign type, and builds a scaling plan.
  Use when a user asks how to structure their ad account, allocate ad budget,
  set ACoS or TACoS targets, decide between SP, SB, and SD, plan a launch vs a
  scale phase, or fix an ad account that grew without a plan. Trigger phrases:
  "advertising strategy", "ad budget", "TACoS", "ad portfolio", "SP SB SD",
  "scale my ads", "ad account structure". Works with zero tools. the user pastes
  their own ad and sales numbers.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Advertising Strategy Director

Most Amazon ad accounts are not strategies. They are a pile of campaigns that grew
one launch at a time. This skill steps back to the portfolio level and builds the
actual plan: what each campaign type is for, how much budget it gets, and what
number you are steering toward.

## When to use this

- The ad account has many campaigns and no governing logic.
- Deciding how to split budget across Sponsored Products, Brands, and Display.
- Setting a realistic ACoS or TACoS target for a product or the whole catalog.
- Moving a product from launch phase to profit phase and the strategy must change.
- Spend is rising faster than sales and nobody can say why.

## The framework. The Three-Layer Ad Portfolio

Stop thinking in campaigns. Think in three layers, each with a different job, a
different budget share, and a different success metric.

| Layer | Job | Campaign types | Success metric |
|-------|-----|----------------|----------------|
| **Defend** | Own your brand and your own listings | SP and SB on brand terms, SD on your own detail pages | Impression share near 100%, low ACoS |
| **Harvest** | Convert high-intent shoppers profitably | SP exact match on proven converting keywords | ACoS at or below break-even |
| **Hunt** | Discover new keywords and audiences | SP auto and broad, SB, SD audiences | Cost per new converting keyword |

Defend is cheap and non-negotiable. Harvest is your profit engine. Hunt is your
growth budget and the only layer allowed to run above break-even ACoS, because you
are paying for discovery, not for the sale.

## The number that governs everything. TACoS

ACoS measures a campaign. TACoS measures the business: total ad spend divided by
total sales, ad-driven and organic. Steer by TACoS.

- **Launch phase:** TACoS 20 to 40 percent is acceptable. You are buying rank.
- **Growth phase:** TACoS 12 to 20 percent. Ads still pull organic up.
- **Mature phase:** TACoS 6 to 12 percent. Organic carries the product. ads defend.

If TACoS is flat while spend rises, ads are replacing organic sales, not adding to
them. That is the single most expensive mistake in the account.

## Step by step

1. **Collect inputs.** Catalog size, price and margin per key product, current total
   ad spend and total sales, current ACoS and TACoS, and the phase of each main
   product (launch, growth, mature). Ask one compact follow-up if data is missing.

2. **Compute break-even ACoS.** Break-even ACoS equals contribution margin divided by
   price, as a percent. This is the line between Harvest and Hunt. Every product needs
   its own number.

3. **Assign each product a phase and a TACoS target** from the table above.

4. **Build the three-layer split.** A typical mature product: Defend 10 to 15 percent
   of budget, Harvest 55 to 65 percent, Hunt 25 to 30 percent. A launch flips it.
   Hunt and rank-buying dominate.

5. **Set rules per layer.** Define the bid posture, match types, and the ACoS ceiling
   for each layer of each product. Hunt may exceed break-even. Harvest may not.

6. **Build the scaling plan.** Define the trigger that moves budget from Hunt to
   Harvest: a keyword converts profitably for 2 weeks, it graduates. Define the
   trigger that cuts spend: a Hunt keyword spends 1.5x the target CPA with no sale.

7. **Run the quality check**, then deliver.

## Output format

```
## Advertising Strategy. [Brand or product]

Phase: [launch / growth / mature]
Break-even ACoS: [X]%   Target TACoS: [Y]%

### Budget split
Defend: [%] . [what runs here]
Harvest: [%] . [what runs here]
Hunt: [%] . [what runs here]

### Rules
[layer]: bid posture, match types, ACoS ceiling
...

### Scaling plan
Graduate when: [trigger]
Cut when: [trigger]

### This week
[top 3 prioritized actions]
```

## Worked example

Product at 30 USD, 12 USD contribution margin. Break-even ACoS is 40 percent. Mature
phase, target TACoS 10 percent.

- Defend: 12 percent of budget, brand SP and SB, ACoS ceiling 15 percent.
- Harvest: 60 percent, SP exact on 25 proven keywords, ACoS ceiling 40 percent.
- Hunt: 28 percent, SP auto plus one broad campaign, ACoS allowed up to 60 percent
  because it buys keyword discovery.
- Graduation rule: any Hunt keyword with 2 weeks of sub-40 percent ACoS moves to
  Harvest as an exact-match keyword.

## Quality check

- Every product has its own break-even ACoS, not one shared number.
- The strategy steers by TACoS, not only by campaign ACoS.
- Only the Hunt layer is allowed to run above break-even ACoS.
- The budget split matches the product phase. a launch is not split like a mature SKU.
- There is a written rule for both scaling up and cutting.
- No campaign exists without a layer and a job.

## Common mistakes

- **Steering by ACoS alone.** A 15 percent ACoS account can still be unprofitable if
  TACoS is climbing and organic is shrinking.
- **One ACoS target for the whole catalog.** Margins differ. break-even differs.
- **No discovery budget.** An account with only Harvest stops finding new keywords
  and slowly decays.
- **Discovery with no graduation.** Hunt campaigns that never promote their winners
  burn money on terms that should have moved to exact long ago.
- **Treating a launch like a mature product.** Launch needs aggressive rank-buying.
  judging it on mature TACoS kills it early.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
