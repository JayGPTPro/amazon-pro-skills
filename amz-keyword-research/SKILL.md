---
name: amz-keyword-research
description: >-
  Build a complete Amazon keyword set for a product and sort it into a usable
  map. generates seed keywords, expands by intent, classifies by funnel stage
  and relevance, and assigns each keyword a placement (title, bullets, backend,
  PPC). Use when a user asks for keyword research, keyword ideas, what keywords
  to target, long-tail keywords, search terms to rank for, or how to map
  keywords to a listing. Trigger phrases: "keyword research", "keyword ideas",
  "what keywords", "long tail keywords", "keywords for my listing", "keyword
  map". Works with zero tools. the user describes the product and audience.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Keyword Research

A keyword list is not keyword research. A pile of 300 keywords with no structure is
as useless as no keywords at all. Real research ends with a map: which keyword goes
where, and which keyword to fight for first. This skill builds that map.

## When to use this

- A new product needs its keyword foundation before the listing is written.
- An existing listing was built on guesses and never had real keyword work.
- A seller has a keyword list but no idea which to prioritize.
- Planning a PPC campaign and needing the keyword groups it will run on.

## The framework. The Keyword Map

Every keyword has two properties that decide what to do with it: **intent stage** and
**relevance**. Plot both and the placement becomes obvious.

### Intent stage

- **Head terms.** Broad, high volume, high competition ("water bottle"). Hard to rank,
  worth pursuing only as the product matures.
- **Mid-tail.** Two to three words, real intent, winnable ("insulated water bottle").
  The core ranking target.
- **Long-tail.** Specific, lower volume, high conversion ("32 oz insulated water
  bottle for hiking"). Cheap to win, converts well, the launch focus.

### Relevance

- **Core.** The product is exactly this. must rank.
- **Adjacent.** Related use case or audience. worth targeting.
- **Loose.** Tangential. backend or skip. never the title.

## AI search keywords

Rufus, Alexa+, and the COSMO layer surface listings on a wider range of queries
than literal A9 search. Three keyword types specifically earn AI-surface citations
and should be included in the map even when their direct search volume looks low.

- **Question-form keywords.** "what is the best [X]", "how to choose [X]", "how to
  use [X] for [Y]". These match the way buyers prompt Rufus and how Alexa+ parses
  spoken queries. Place answers in bullets and in the Customer Questions tab.
- **Comparison keywords.** "[brand or product] vs [alternative]", "[X] alternative
  to [Y]", "difference between [X] and [Y]". COSMO uses these to position the
  listing against the comparison set. Place in A+ comparison-chart copy and in a
  bullet that names the comparison without naming a competitor brand.
- **Audience-specific keywords.** "[product] for [audience]", e.g. "running shoes
  for runners over 50", "stroller for tall parents", "yoga mat for hot yoga". COSMO
  reads these as explicit audience intent and re-ranks listings that clearly serve
  the named audience. Place in the title's qualifier slot, in a bullet, and in
  backend keywords.

These are not separate from the map below. they slot into Bullet/A+, Backend, and
PPC placements as normal, with the launch priority weighted toward the audience-
specific ones because they convert best and face the least competition.

## The placement rule

| Keyword type | Placement |
|--------------|-----------|
| Highest-volume core mid-tail | Title |
| Core and adjacent mid-tail and long-tail | Bullets and A+ |
| Loose, synonyms, misspellings, not yet placed | Backend search terms |
| Everything winnable | PPC, grouped by match type |

## Step by step

1. **Collect inputs.** The product, what problem it solves, the target audiences, the
   category, and any keywords or competitor listings the user already has.

2. **Generate seeds.** From the product itself, its use cases, its audiences, its
   materials and attributes, the problems it solves, and the occasions it fits.

3. **Expand each seed.** Synonyms, alternate phrasings, modifiers (size, color,
   material, audience, use case), question forms, and common misspellings.

4. **Classify every keyword** by intent stage and relevance, per the framework.

5. **Cut the noise.** Drop Loose keywords with no real intent. an irrelevant keyword
   that brings the wrong shopper hurts conversion-based ranking.

6. **Build the map.** Assign every surviving keyword a placement. Mark the launch
   priority set: core long-tail and winnable mid-tail.

7. **Run the quality check**, then deliver.

## Output format

```
## Keyword Map. [product]

### Title keywords (highest-volume core mid-tail)
[keywords]

### Bullet and A+ keywords (core and adjacent)
[keywords grouped by theme]

### Backend keywords (loose, synonyms, misspellings)
[keywords]

### PPC groups
Exact (proven intent): [keywords]
Broad and phrase (discovery): [keywords]

### Launch priority
[the 10 to 15 winnable keywords to rank for first]
```

## Worked example

Product: a 32 oz insulated water bottle for hiking.

- Title: "insulated water bottle", "32 oz water bottle". core mid-tail, real volume,
  winnable.
- Bullets and A+: "leakproof water bottle", "water bottle for hiking", "wide mouth
  bottle". core and adjacent.
- Backend: "thermos", "canteen", "hydro flask alternative", "watter bottle"
  (misspelling). loose and synonyms.
- Launch priority: the long-tail set, "32 oz insulated bottle for hiking",
  "leakproof hiking water bottle". low competition, high conversion, rankable in weeks.

## Quality check

- Every keyword is classified by both intent stage and relevance.
- Loose, low-intent keywords are cut, not stuffed into the title.
- Every surviving keyword has a placement.
- The launch priority set is winnable long-tail and mid-tail, not head terms.
- PPC keywords are split into proven-intent exact and discovery broad.

## Common mistakes

- **A list with no map.** 300 keywords and no decision about any of them.
- **Chasing head terms at launch.** Spending the launch fighting "water bottle"
  against entrenched sellers instead of winning long-tail fast.
- **Stuffing irrelevant keywords.** An off-target keyword that brings non-buyers
  lowers conversion and hurts rank.
- **Translating keywords by logic.** Real shoppers use words you would not guess.
  expand from how people actually search, not from a thesaurus.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
