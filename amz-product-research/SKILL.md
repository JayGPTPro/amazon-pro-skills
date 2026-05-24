---
name: amz-product-research
description: >-
  Research and validate an Amazon product opportunity end to end, and evaluate
  whether the niche around it is winnable. Assesses demand, competition, profit
  potential, entry barriers, review wall, differentiation room, and seasonality,
  and returns a go/no-go with the reasoning. Use when a user asks to research a
  product, find a product to sell, validate a product idea, assess an
  opportunity, evaluate a niche, find a profitable niche, judge whether a
  category is worth entering, or compare niches. Trigger phrases: "product
  research", "find a product to sell", "validate this product", "is this a good
  product", "product opportunity", "should I sell this", "niche finder",
  "evaluate this niche", "is this niche worth it", "good niche", "low
  competition niche", "should I enter". Works with zero tools. the user
  describes the product and what they can observe.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Product Research

Product research is the highest-stakes decision a seller makes. everything after it
is execution on a choice already made. This skill validates a product opportunity
across the four things that decide it, and pressure-tests the niche around it,
returning a clear go or no-go.

Two layers run here. The Opportunity Square is the single-product test. The Niche
Scorecard is the niche-level test that frames the product. Run the Square when you
have one product in mind. Add the Scorecard when the question is "is this whole
category winnable" or when comparing several niches before picking the product.

## When to use this

- A seller has a product idea and wants it pressure-tested before committing.
- A seller is comparing several product ideas or several niches.
- A seller keeps picking products that look promising and then disappoint.
- Validating a product before sourcing or sampling.
- Sizing a niche before committing time to specific products inside it.

## The framework. The Opportunity Square

A product opportunity stands on four corners. A weak corner is not fatal alone, but
two weak corners are a no-go, and the verdict must say which corners carry it.

### Corner 1. Demand

Is there real, steady demand? Look for consistent search volume and consistent sales
across the top listings, not one spike. Check the trend. demand fading is a trap, even
if today's number looks fine.

### Corner 2. Competition

Can a new entrant win? Read the top listings. Strong brands with thousands of reviews
and excellent listings make a hard square. Weak listings, tired images, and a wall of
complaints in the reviews are an open one. Count the review barrier honestly.

### Corner 3. Profit

Does the money work? Selling price minus the full FBA fee stack, the landed cost,
returns, storage, and a realistic launch ad budget must leave a real net margin. Use
amz-fba-calculator. A product that sells well at a 4 percent net margin is a job, not
a business.

### Corner 4. Barrier to entry

What stands in the way? Patents, brand-locked categories, gating, heavy compliance,
high minimum order quantities, oversize fee tiers, fragile or hazardous shipping. A
high barrier is sometimes good, it keeps competitors out, but only if the seller can
clear it themselves.

## Sub-framework. The Niche Scorecard

When the question is whether to enter a whole niche (not just a single ASIN), score
the niche on six gates. Two of them are pass-or-fail. fail either and the niche is
avoid, regardless of the rest.

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

### Reading the scored gates

- **Competition depth.** A page-one of 10 strong brands is a hard niche. a page-one
  with weak listings and tired images is an opening.
- **Review barrier.** If the top listings have 200 to 800 reviews, a new entrant can
  climb in. If they have 5,000-plus, the review wall alone can take a year.
- **Differentiation room.** Read the top listings' reviews. recurring complaints are
  the room to differentiate. If buyers are already happy, there is no opening.
- **Seasonality and risk.** A niche that sells only in December is a different
  business. a niche full of patented designs or one dominant brand is a trap.

How the two layers relate. The Square asks "is this specific product the right bet."
The Scorecard asks "is the surrounding niche worth fighting in at all." A product can
look strong in the Square and still sit inside a brutal niche, in which case the
verdict should be Investigate at minimum.

## Step by step

1. **Collect inputs.** The product idea, category, typical price, what the user can
   observe about the top listings (reviews, ratings, image quality, complaints),
   rough costs, any known patents, gating, or compliance issues, and any seasonality
   or brand concentration signals.

2. **If the question is niche-level, run the Scorecard first.** Pass-or-fail gates
   before the scored ones. A failed gate ends the analysis with Avoid.

3. **Score each corner of the Square.** Strong, mixed, or weak, each backed by
   evidence.

4. **Run the profit math** properly. landed cost, full fee stack, returns, storage,
   launch ads. Do not let a guess stand in for the calculation.

5. **Find the angle.** If this is a go, state the specific reason a new entrant wins:
   an unmet complaint, a weak incumbent, a price or quality gap.

6. **Verdict.** Go (at least three strong corners and a real angle, niche not Avoid),
   Investigate (mixed, name what data would settle it), or No-go (two weak corners,
   no angle, or niche-level Avoid).

7. **Run the quality check**, then deliver.

## Output format

```
## Product Research. [product]

### The Opportunity Square
Demand: [strong/mixed/weak] . [evidence]
Competition: [strong/mixed/weak] . [evidence]
Profit: [strong/mixed/weak] . [the net margin number]
Barrier to entry: [strong/mixed/weak] . [evidence]

### Niche Scorecard (if niche-level)
Demand gate: [pass/fail] . [evidence]
Margin headroom gate: [pass/fail] . [evidence]
Competition depth: [score] . [notes]
Review barrier: [score] . [notes]
Differentiation room: [score] . [notes]
Seasonality and risk: [score] . [notes]

### The angle
[the specific way to win, or "no clear angle"]

### Verdict: [GO / INVESTIGATE / NO-GO]
[reasoning, naming which corners carry it and which are risks]

### If GO, next step
[sourcing, sampling, or deeper validation]
```

## Worked example

Idea: a silicone stretch lid set, around 14 USD.

Demand: strong, steady year-round volume. Competition: mixed, a crowded page-one but
the listings are generic and the images are weak. Profit: weak, at 14 USD after the
fee stack, landed cost, and launch ads the net margin is thin. Barrier: low, easy to
source, which also means easy for others.

Niche Scorecard: demand passes, margin headroom borderline-fail at this price point,
review barrier high (top listings 3k-6k reviews), differentiation room real
(recurring complaints about stretch tearing).

Verdict: No-go as-is. Two weak-leaning corners, profit and barrier, a borderline
margin gate, and a low-price product where ads eat the margin. The angle (better
images, better listing, non-tearing version) is real but cannot fix a structurally
thin margin. Investigate a higher-priced, clearly premium version that lifts the
profit corner before committing.

## Quality check

- All four corners of the Square are scored with evidence, not asserted.
- If niche-level, the Scorecard pass-or-fail gates were checked first and a failed
  gate produced Avoid.
- The profit corner uses a real calculation through the full fee stack, not a guess.
- A product with two weak corners is a no-go, and the verdict says so.
- A go verdict names a specific, concrete angle to win.
- The verdict is Go, Investigate, or No-go, with reasoning that names the carrying
  corners and the risks.

## Common mistakes

- **Demand tunnel vision.** Picking a product because search volume is high, ignoring
  that profit or competition fails.
- **Guessing the margin.** Skipping the real fee-stack math and assuming it works.
- **Ignoring the trend.** Today's demand looks fine while the category is sliding.
- **No angle.** Entering a niche of excellent listings with happy buyers and nothing
  to take.
- **Falling for demand alone at the niche level.** High search volume in a niche with
  no margin or a 10,000-review wall is a trap, not an opportunity.
- **Skipping the risk scan.** Walking into a patented design or a single-brand-locked
  category.
- **Confirmation bias.** Researching to justify a product the seller already chose.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
