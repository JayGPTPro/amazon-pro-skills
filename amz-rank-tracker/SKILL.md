---
name: amz-rank-tracker
description: >-
  Set up Amazon keyword rank tracking and interpret the movements. Defines which
  keywords to track, how to read a rank change, separates organic rank from ad
  placement, and turns ranking shifts into actions. Use when a user asks about
  rank tracking, keyword rankings, why a ranking dropped, organic position,
  tracking search position, or how to improve a keyword rank. Trigger phrases:
  "rank tracker", "keyword ranking", "rank dropped", "organic rank", "search
  position", "improve my ranking", "track rankings". Works with zero tools. the
  user provides their rank observations.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Rank Tracker

Rank is the score that decides how much free traffic a listing gets. But a raw rank
number means nothing without context. a drop can be a disaster or noise. This skill
sets up tracking that matters and reads the movements correctly.

## When to use this

- A seller wants to start tracking keyword rank properly.
- A ranking dropped and the seller does not know if it is serious.
- A seller is tracking 200 keywords and drowning in noise.
- A launch is underway and rank progress needs monitoring.

## The framework. The Three-Tier Rank Ladder

Tracking every keyword is noise. Track the keywords that decide revenue. The
Three-Tier Rank Ladder sorts the keyword set into three tiers, each with its own
tracking cadence.

| Tier | Which keywords | Track how |
|------|----------------|-----------|
| Money keywords | The 5 to 15 terms that drive most of the sales | Daily, watched closely |
| Growth keywords | Terms being actively pushed toward page one | Daily during the push |
| Watch keywords | Long-tail and secondary terms | Weekly, scanned for surprises |

Tracking the 10 keywords that make the money beats tracking 200 that do not.

## Watching the AI shopping surfaces (emerging, not yet a rank metric)

Standard search rank is no longer the whole picture. A growing share of buyer
attention is moving into Amazon's AI shopping surfaces: the in-app AI assistant
answers and the recommendation modules it generates. These surfaces are new and
still shifting fast. Amazon's AI assistant launched as Rufus and, as of mid-2026,
is being folded into a unified "Alexa for Shopping" experience, so the exact
names, panels, and behaviors keep changing. A listing can hold a solid organic
position and still lose share if the assistant does not surface it, and a listing
can sit deeper in literal search and still pick up traffic if the assistant
recommends it.

Important: there is no public, precise rank metric for these surfaces today. Do
not track them like organic rank, because there is no stable position number to
track and the surfaces themselves are in flux. Monitor them qualitatively
instead. for a handful of money keywords, occasionally:

- **Ask the assistant a question version of the keyword** and note whether your
  ASIN comes up at all. This is a yes/no/sometimes observation, not a position.
- **Glance at the AI-generated recommendation modules** for the keyword's intent
  and note whether the listing tends to appear. Look for a directional trend over
  weeks, not a daily number.
- **For voice-relevant categories**, occasionally test a spoken query and note
  whether the assistant returns the ASIN.

Treat all of this as a soft, directional signal, not a precise rank. If the
listing stops surfacing in the AI modules while holding organic rank, the likely
issue is an intent-match gap under COSMO. the use case or audience signal in the
copy has gone vague (see amz-ai-search-optimization). Act on a clear sustained
pattern, not a single observation, and never let these noisy surfaces override
what your real organic rank and sales data are telling you.

## Reading a rank movement

A rank number alone is meaningless. Three rules for reading a movement.

1. **Organic versus sponsored.** A listing can show high because of an ad placement
   while its organic rank is low. Always read organic rank separately. an "improvement"
   that is just ad spend is not real rank.

2. **Noise versus signal.** Rank wobbles a few positions every day. A move of a few
   spots is noise. A sustained move over several days, or a large sudden jump, is
   signal. Do not react to noise.

3. **The cause map.** When a real move happens, map it to a cause before acting:
   - Sudden organic drop. a stockout, a listing suppression, a policy flag, a lost
     Buy Box, or a competitor surge. Check those first.
   - Slow organic decline. conversion rate slipping, reviews souring, price drift,
     or a category-wide shift.
   - Organic rise. a recent listing or image change, a deal, ad spend pulling organic
     up, or fresh reviews.

## Step by step

1. **Collect inputs.** The product, the keyword set, current rank observations
   (organic and overall if known), and any recent changes: listing edits, stock
   events, deals, ad changes.

2. **Tier the keywords.** Assign each to money, growth, or watch. Define the tracking
   cadence per tier.

3. **Separate organic from sponsored** in every observation. flag where the seller is
   only seeing the ad-placed position.

4. **Classify each movement** as noise or signal using the rules.

5. **For every signal, map the cause.** Use the cause map. Do not recommend an action
   until the cause is identified.

6. **Recommend actions** only for real signals, ordered by revenue impact.

7. **Run the quality check**, then deliver.

## Output format

```
## Rank Report. [product]

### Tracking setup
Money keywords: [list] . daily
Growth keywords: [list] . daily
Watch keywords: [list] . weekly

### Movements
[keyword] . organic rank: [from -> to] . [noise / signal] . likely cause
...

### Actions (signals only)
1. [keyword] . [cause] . [action] . [revenue priority]
```

## Worked example

A money keyword fell from organic position 8 to 31 in two days.

Read: a 23-spot sustained drop is signal, not noise. Cause map for a sudden organic
drop: the seller checks and finds the product went out of stock for 36 hours.
Out-of-stock crushes organic rank fast. Action: get back in stock, then run a short
ad push and, if eligible, a deal to rebuild velocity and recover the position.
panicking and rewriting the listing would have been the wrong move. the listing was
never the problem.

## Quality check

- Keywords are tiered. money, growth, watch. not all tracked the same.
- Organic rank is read separately from ad-placed position in every observation.
- Each movement is classified noise or signal. small wobbles are not acted on.
- Every signal is mapped to a cause before any action is recommended.
- Actions are given only for real signals, ordered by revenue impact.

## Common mistakes

- **Reacting to noise.** Rewriting a listing because rank wobbled three spots.
- **Confusing ad placement with rank.** Celebrating a "rank gain" that is only paid
  placement, while organic rank is flat or falling.
- **Tracking everything.** 200 tracked keywords, no idea which 10 matter.
- **Acting before diagnosing.** Recommending a fix before mapping the cause. the
  fix for a stockout drop is not the fix for a conversion-decline drop.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
