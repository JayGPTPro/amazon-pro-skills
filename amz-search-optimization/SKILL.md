---
name: amz-search-optimization
description: >-
  Optimize a product's visibility in Amazon search. Explains how the A9 and
  COSMO ranking systems weigh relevance, conversion, and sales velocity, audits
  a listing against the ranking factors, and builds a plan to climb. Use when a
  user asks about Amazon SEO, ranking higher in search, the A9 or COSMO
  algorithm, search visibility, why a listing does not rank, or how Amazon
  decides ranking. Trigger phrases: "amazon SEO", "rank higher", "A9", "COSMO",
  "search ranking", "search visibility", "why doesn't my listing rank". Works
  with zero tools.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Search Optimization

Amazon search is not Google. It does not rank the most relevant result, it ranks the
result most likely to sell. This skill explains how Amazon's ranking actually works
and audits a listing against the factors that move it.

## When to use this

- A listing is indexed but buried and the seller wants to climb.
- A seller is confused about what Amazon's algorithm rewards.
- A new product needs a ranking plan, not just a listing.
- Rankings are flat despite a good-looking listing.

## The framework. The Three Pillars of Amazon Rank

Amazon's ranking (A9, and the newer COSMO layer that adds shopper context and intent)
weighs three pillars. A listing must clear all three. a weak pillar caps the rank
regardless of the other two.

### Pillar 1. Relevance

Can Amazon match the listing to the query at all? A keyword the listing does not
contain anywhere, in the title, bullets, or backend, cannot rank. Relevance is the
entry ticket. it gets you considered, not ranked.

COSMO extends this: Amazon increasingly infers intent and context, so a listing that
clearly serves a specific use case and audience is matched to more of the right
queries, even ones it does not literally contain.

### Pillar 2. Conversion

Of the shoppers who see the listing, how many buy? This is the heaviest pillar.
Amazon ranks what sells. Conversion is driven by the main image, price, rating and
review count, and the listing's persuasive quality. A listing that is relevant but
converts poorly will not climb, because ranking it would cost Amazon sales.

### Pillar 3. Sales velocity

How many units, and how fast, for a given keyword? Recent sales velocity for a query
pushes rank for that query. This is why launches use ads and deals. they manufacture
velocity to earn organic rank, which then sustains itself.

## The diagnosis

- Not indexed for a keyword. a Relevance failure. the keyword is missing from the
  listing. fix placement.
- Indexed but page 5 and not moving. usually a Conversion failure. traffic arrives,
  does not buy, Amazon will not promote it.
- Good conversion but slow climb. a Velocity problem. needs an ads-and-deals push to
  build momentum.

## Step by step

1. **Collect inputs.** The product, the target keywords, the listing (title, bullets,
   backend), the main image, price, rating, review count, conversion rate if known,
   and current rough rankings.

2. **Audit Pillar 1.** For each target keyword, is it placed somewhere indexable? Is
   the listing clearly serving a specific use case and audience for COSMO?

3. **Audit Pillar 2.** Score the conversion drivers: main image, price position,
   rating, review count, listing persuasion. Name the weakest.

4. **Audit Pillar 3.** Is there enough recent sales velocity on the target keywords,
   or does the listing need a manufactured push?

5. **Diagnose the capping pillar.** Identify the one pillar holding the rank down.

6. **Build the climb plan.** Fix the capping pillar first. relevance fixes are
   cheap, conversion fixes are highest leverage, velocity is the launch lever.

7. **Run the quality check**, then deliver.

## Output format

```
## Search Optimization. [product]

### Pillar audit
Relevance: [pass / gaps] . [missing keywords, COSMO intent clarity]
Conversion: [score] . [weakest driver]
Velocity: [adequate / needs a push]

### Capping pillar: [which]

### Climb plan
1. [fix the capping pillar] ...
2. ...

### Watch
[the metric that confirms the climb]
```

## Worked example

A listing is indexed for its main keyword but stuck on page 4. Traffic is decent,
conversion rate is well below the category norm.

Diagnosis: Relevance passes, the keyword is placed. Velocity is adequate, traffic
arrives. The capping pillar is Conversion. the main image is flat and the bullets are
a feature list. Amazon will not promote a listing that does not convert the traffic
it already gets. Climb plan: fix the main image and rewrite the bullets benefit-first,
then the existing traffic starts converting, and rank follows. Spending on ads before
fixing conversion would just buy expensive proof that the listing does not close.

## Quality check

- All three pillars are audited. relevance, conversion, velocity.
- The single capping pillar is identified before any plan is written.
- The plan fixes the capping pillar first, not the easiest pillar.
- Conversion is treated as the heaviest pillar, because Amazon ranks what sells.
- A velocity push is recommended only once conversion is sound.

## Common mistakes

- **Treating Amazon like Google.** Optimizing for relevance alone. relevance only
  gets you considered.
- **Buying velocity into a weak listing.** Ads and deals on a listing that does not
  convert just burn money.
- **Ignoring conversion.** The heaviest ranking pillar, and the one sellers most
  often skip.
- **Keyword stuffing for relevance.** Cramming keywords hurts conversion, which hurts
  rank more than the extra relevance helps.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. 50 production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
