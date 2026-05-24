---
name: amz-listing-optimization
description: >-
  Optimize a full Amazon listing for both ranking and conversion, and diagnose
  why a listing is not ranking against the A9 + COSMO pillars. Rewrites the
  title, bullets, and description, places keywords correctly, sharpens the
  benefit argument, and checks policy and mobile compliance. Use when a user
  asks to optimize a listing, improve a title, rewrite bullets, fix a listing
  that does not convert, improve listing copy, do a listing makeover, rank
  higher in search, audit search visibility, or asks about the A9 or COSMO
  algorithm. Trigger phrases: "optimize my listing", "listing optimization",
  "rewrite my bullets", "improve my title", "listing not converting", "listing
  makeover", "amazon SEO", "rank higher", "A9", "COSMO", "search ranking",
  "search visibility", "why doesn't my listing rank". Works with zero tools.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Listing Optimizer

A listing has two jobs and they pull against each other. it must rank, which wants
keywords, and it must convert, which wants persuasion. Sellers usually do one and
lose the other. This skill rewrites the title, bullets, and description to do both,
and diagnoses which side is holding the listing back.

## When to use this

- A listing gets impressions but a weak conversion rate.
- A listing converts when found but barely ranks.
- The copy is a keyword dump or a feature list with no argument.
- A product is launching and the listing must be right from day one.
- A seller is confused about what Amazon's algorithm rewards.
- Rankings are flat despite a good-looking listing.

## The framework. Rank and Convert

Every element of a listing is scored on two axes. The fix depends on which axis is
failing.

- **Rank axis.** Does the right keyword appear in the right place so Amazon indexes
  and ranks it? Title and bullets carry the most weight.
- **Convert axis.** Does the copy turn a reader into a buyer by leading with benefits
  and killing objections?

Diagnose first. impressions but no sales is a convert problem. sales when found but
no impressions is a rank problem. Then rewrite the failing axis without breaking the
other.

## Ranking diagnosis. A9 + COSMO pillars

When the failure is on the Rank axis, dig one level deeper. Amazon's ranking (A9, and
the newer COSMO layer that adds shopper context and intent) weighs three pillars. A
listing must clear all three. a weak pillar caps the rank regardless of the other
two.

### Pillar 1. Relevance

Can Amazon match the listing to the query at all? A keyword the listing does not
contain anywhere (title, bullets, or backend) cannot rank. Relevance is the entry
ticket. it gets you considered, not ranked.

COSMO extends this. Amazon now infers intent and context, so a listing that clearly
serves a specific use case and audience is matched to more of the right queries,
even ones it does not literally contain. Concrete 2026-era example. a shopper
searches "gift for new mom who is breastfeeding". The literal-keyword listing that
crams "breastfeeding gift" into the title used to win. Under COSMO, Amazon infers
the intent (postpartum recovery, practical, comfort-focused, sub-$50) and re-ranks
to surface listings whose copy clearly establishes that use case, audience, and
price band, even without the exact phrase. A listing that says "for the first six
weeks postpartum" and "machine-washable in cold" can outrank one stuffed with the
literal query. Specificity of use case and audience now functions as a ranking
signal, not just a conversion signal.

### Pillar 2. Conversion

Of the shoppers who see the listing, how many buy? This is the heaviest pillar.
Amazon ranks what sells. Conversion is driven by the main image, price, rating and
review count, and the listing's persuasive quality. A listing that is relevant but
converts poorly will not climb, because ranking it would cost Amazon sales.

### Pillar 3. Sales velocity

How many units, and how fast, for a given keyword? Recent sales velocity for a query
pushes rank for that query. This is why launches use ads and deals. they manufacture
velocity to earn organic rank, which then sustains itself.

### Reading the pillars

- Not indexed for a keyword. a Relevance failure. the keyword is missing from the
  listing. fix placement.
- Indexed but page 5 and not moving. usually a Conversion failure. traffic arrives,
  does not buy, Amazon will not promote it.
- Good conversion but slow climb. a Velocity problem. needs an ads-and-deals push to
  build momentum.

## The element playbook

### Title

- Lead with the highest-volume core keyword phrase, then brand, then the key
  qualifiers (size, count, material, use).
- Readable, not a keyword pile. A title a human cannot parse converts worse even if
  it indexes.
- Respect the category character limit. front-load. mobile truncates around 80 chars.
- No promotional or subjective claims ("best", "sale", "top rated").

### Bullets

Five bullets, each one job:

1. The single biggest benefit, the reason to buy.
2 to 4. The features that matter, each written benefit-first: the feature, then what
it does for the buyer.
5. The objection killer or the guarantee.

Open each bullet with 2 to 4 capitalized words as a label, then the sentence. Weave
keywords in naturally. never at the cost of readability.

### Description

When A+ Content is present, the description is light. a short brand-and-benefit
paragraph. When there is no A+, the description must carry more of the argument.

## Step by step

1. **Collect inputs.** The current title, bullets, description, the product, the
   target buyer, the top 3 objections, the keyword set (or run keyword logic first),
   whether A+ Content exists, and current rough rankings.

2. **Diagnose the failing axis.** Rank, convert, or both. If Rank is failing, audit
   the three pillars and name the capping pillar before rewriting.

3. **Rewrite the title** per the playbook. front-loaded keyword, readable, compliant.

4. **Rewrite the 5 bullets**, each with its job, benefit-first, keywords woven in.

5. **Rewrite the description** to match whether A+ exists.

6. **Place keywords.** Confirm the priority keywords appear in title or bullets.
   anything not placed goes to backend, not crammed into visible copy.

7. **Sharpen the COSMO signal.** Make the use case, audience, and context
   unambiguous in the copy so intent-based ranking can pick it up.

8. **Compliance and mobile check.** No prohibited claims, within character limits,
   readable on a phone with the title front-loaded.

9. **Run the quality check**, then deliver.

## Output format

```
## Listing Optimization. [product]

Diagnosis: [rank problem / convert problem / both]
If rank, capping pillar: [relevance / conversion / velocity]

### Title
Before: [old]
After: [new]
Why: [what changed and the axis it fixes]

### Bullets
1. [new bullet] . job: biggest benefit
...

### Description
[new copy]

### Keyword placement
Placed in title/bullets: [keywords]
Sent to backend: [keywords]

### COSMO signal
Use case made explicit: [what]
Audience made explicit: [who]

### Compliance and mobile
[confirmation]
```

## Worked example

A garlic press, good impressions, weak conversion. Diagnosis: convert problem. The
old bullets were a feature list, "stainless steel construction, ergonomic handle,
dishwasher safe".

Rewritten bullet 1: "NO MORE GARLIC SMELL ON YOUR HANDS. Press a whole clove, skin
on, and never touch it. the mince drops straight into the pan." Same product, but the
copy now leads with the benefit and kills the real objection. The title was already
fine, so it was left alone. fixing what is not broken risks the rank axis.

Second case. A listing is indexed for its main keyword but stuck on page 4. Traffic
is decent, conversion rate is well below the category norm. Diagnosis: rank problem,
capping pillar is Conversion. the main image is flat and the bullets are a feature
list. Amazon will not promote a listing that does not convert the traffic it already
gets. Climb plan: fix the main image and rewrite the bullets benefit-first, then the
existing traffic starts converting, and rank follows. Spending on ads before fixing
conversion would just buy expensive proof that the listing does not close.

## Quality check

- The failing axis was diagnosed before rewriting.
- If Rank is failing, the three pillars were audited and the capping pillar was
  named before any plan was written.
- The title front-loads the core keyword and stays readable and compliant.
- Each of the 5 bullets has one job and is written benefit-first.
- Priority keywords are placed. unplaced keywords go to backend, not crammed in.
- The use case and audience are explicit so COSMO can match intent-based queries.
- No prohibited or subjective claims anywhere.
- The title reads correctly truncated at about 80 characters on mobile.

## Common mistakes

- **Treating Amazon like Google.** Optimizing for relevance alone. relevance only
  gets you considered.
- **Keyword-stuffing the title.** It indexes and then converts badly. humans buy.
- **Feature-list bullets.** "Stainless steel construction" is a feature. the buyer
  wants the benefit.
- **Rewriting what works.** Touching a title that already ranks can cost the rank.
  diagnose first.
- **Buying velocity into a weak listing.** Ads and deals on a listing that does not
  convert just burn money.
- **Ignoring mobile truncation.** A title whose key phrase sits past character 80 is
  invisible to most shoppers.
- **Crammed keywords.** Forcing every keyword into visible copy. that is what the
  backend field is for.
- **Vague use case.** A listing that could be anything to anyone leaves COSMO no
  intent to match.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
