---
name: amz-niche-finder
description: >-
  Evaluate whether an Amazon niche is worth entering. Scores a niche on demand,
  competition, margin headroom, review barrier, differentiation room, and
  seasonality, and returns an enter, watch, or avoid verdict. Use when a user
  asks to evaluate a niche, find a profitable niche, judge whether a category is
  worth entering, assess competition in a niche, or compare two niches. Trigger
  phrases: "niche finder", "evaluate this niche", "is this niche worth it",
  "good niche", "low competition niche", "should I enter". Works with zero
  tools. the user describes the niche and what they can observe.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Niche Finder

Most product failures are decided before launch, in the choice of niche. A great
listing in a brutal niche loses. A mediocre listing in an open niche wins. This skill
scores a niche honestly and returns enter, watch, or avoid.

## When to use this

- A seller has a product idea and wants to know if the niche is winnable.
- Choosing between two or three niches to commit to.
- A seller keeps picking niches that look good and turn out saturated.
- Sizing a niche before sourcing or sampling anything.

## The framework. The Niche Scorecard

Score the niche on six gates. Two of them are pass-or-fail. fail either and the niche
is avoid, regardless of the rest.

| Gate | What to look for | Weight |
|------|------------------|--------|
| Demand | Steady search volume and sales across the top listings | Pass/fail |
| Margin headroom | Selling price leaves real margin after fees and ads | Pass/fail |
| Competition depth | How many entrenched sellers, and how strong | Scored |
| Review barrier | Review counts of the top listings. the wall a new entrant climbs | Scored |
| Differentiation room | Are the top listings beatable, or already excellent | Scored |
| Seasonality and risk | Year-round demand, no patent, brand, or compliance trap | Scored |

**Demand** and **margin headroom** are the pass-or-fail gates. No demand, nothing to
win. No margin, winning does not pay. Only score the rest if both pass.

## Reading the scored gates

- **Competition depth.** A page-one of 10 strong brands is a hard niche. a page-one
  with weak listings and tired images is an opening.
- **Review barrier.** If the top listings have 200 to 800 reviews, a new entrant can
  climb in. If they have 5,000-plus, the review wall alone can take a year.
- **Differentiation room.** Read the top listings' reviews. recurring complaints are
  the room to differentiate. If buyers are already happy, there is no opening.
- **Seasonality and risk.** A niche that sells only in December is a different
  business. a niche full of patented designs or one dominant brand is a trap.

## Step by step

1. **Collect inputs.** The niche, the typical selling price, what the user can
   observe about the top listings (review counts, image quality, ratings, recurring
   complaints), and any seasonality or known patent or brand concentration.

2. **Run the pass-or-fail gates.** Demand and margin headroom. If either fails, the
   verdict is avoid. stop and say why.

3. **Score the four scored gates** from the observations.

4. **Find the opening.** State the specific way a new entrant could win: a weak
   incumbent, an unmet complaint, an outdated image set. If there is no opening, say so.

5. **Verdict.** Enter (clear opening, climbable barrier, real margin), Watch (mixed,
   revisit with more data), or Avoid (failed gate or no opening).

6. **Run the quality check**, then deliver.

## Output format

```
## Niche Evaluation. [niche]

### Pass-or-fail gates
Demand: [pass/fail] . [evidence]
Margin headroom: [pass/fail] . [evidence]

### Scored gates
Competition depth: [score] . [notes]
Review barrier: [score] . [notes]
Differentiation room: [score] . [notes]
Seasonality and risk: [score] . [notes]

### The opening
[the specific way to win, or "no clear opening"]

### Verdict: [ENTER / WATCH / AVOID]
[one paragraph of reasoning]
```

## Worked example

Niche: bamboo cutlery sets, around 18 USD.

Demand passes, steady volume. Margin headroom: at 18 USD after fees and ads the
margin is thin. borderline. Competition: page-one is crowded but the listings are
generic. Review barrier: top listings at 1,500 to 4,000 reviews, a real wall.
Differentiation room: reviews complain the cutlery splinters, a genuine opening.

Verdict: Watch. The opening is real (a non-splintering version) but the thin margin
and the high review wall mean it is not a clean Enter. Revisit if a higher-priced,
clearly better version can be sourced that lifts the margin gate to a clear pass.

## Quality check

- Demand and margin headroom were checked first as pass-or-fail gates.
- A niche that fails either gate is Avoid, and the reason is stated.
- The four scored gates are each backed by an observation, not a guess.
- The verdict names a specific opening, or states there is none.
- The verdict is one of Enter, Watch, or Avoid, with reasoning.

## Common mistakes

- **Falling for demand alone.** High search volume in a niche with no margin or a
  10,000-review wall is a trap, not an opportunity.
- **Ignoring the review barrier.** Underestimating how long it takes to climb past
  entrenched listings.
- **No opening.** Entering a niche where the top listings are genuinely excellent and
  buyers are happy. there is nothing to take.
- **Skipping the risk scan.** Walking into a patented design or a single-brand-locked
  category.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. 50 production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
