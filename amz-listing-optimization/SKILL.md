---
name: amz-listing-optimization
description: >-
  Optimize a full Amazon listing for both ranking and conversion. Rewrites the
  title, bullets, and description, places keywords correctly, sharpens the
  benefit argument, and checks policy and mobile compliance. Use when a user
  asks to optimize a listing, improve a title, rewrite bullets, fix a listing
  that does not convert, improve listing copy, or do a listing makeover. Trigger
  phrases: "optimize my listing", "listing optimization", "rewrite my bullets",
  "improve my title", "listing not converting", "listing makeover". Works with
  zero tools. the user pastes the current listing.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Listing Optimizer

A listing has two jobs and they pull against each other. it must rank, which wants
keywords, and it must convert, which wants persuasion. Sellers usually do one and
lose the other. This skill rewrites the title, bullets, and description to do both.

## When to use this

- A listing gets impressions but a weak conversion rate.
- A listing converts when found but barely ranks.
- The copy is a keyword dump or a feature list with no argument.
- A product is launching and the listing must be right from day one.

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
   and whether A+ Content exists.

2. **Diagnose the failing axis.** Rank, convert, or both.

3. **Rewrite the title** per the playbook. front-loaded keyword, readable, compliant.

4. **Rewrite the 5 bullets**, each with its job, benefit-first, keywords woven in.

5. **Rewrite the description** to match whether A+ exists.

6. **Place keywords.** Confirm the priority keywords appear in title or bullets.
   anything not placed goes to backend, not crammed into visible copy.

7. **Compliance and mobile check.** No prohibited claims, within character limits,
   readable on a phone with the title front-loaded.

8. **Run the quality check**, then deliver.

## Output format

```
## Listing Optimization. [product]

Diagnosis: [rank problem / convert problem / both]

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

## Quality check

- The failing axis was diagnosed before rewriting.
- The title front-loads the core keyword and stays readable and compliant.
- Each of the 5 bullets has one job and is written benefit-first.
- Priority keywords are placed. unplaced keywords go to backend, not crammed in.
- No prohibited or subjective claims anywhere.
- The title reads correctly truncated at about 80 characters on mobile.

## Common mistakes

- **Keyword-stuffing the title.** It indexes and then converts badly. humans buy.
- **Feature-list bullets.** "Stainless steel construction" is a feature. the buyer
  wants the benefit.
- **Rewriting what works.** Touching a title that already ranks can cost the rank.
  diagnose first.
- **Ignoring mobile truncation.** A title whose key phrase sits past character 80 is
  invisible to most shoppers.
- **Crammed keywords.** Forcing every keyword into visible copy. that is what the
  backend field is for.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. 50 production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
