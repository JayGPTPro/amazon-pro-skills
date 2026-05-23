---
name: amz-product-research
description: >-
  Research and validate an Amazon product opportunity end to end. Assesses
  demand, competition, profit potential, and entry barriers, and returns a
  go/no-go with the reasoning. Use when a user asks to research a product, find
  a product to sell, validate a product idea, assess an opportunity, or decide
  whether to sell something on Amazon. Trigger phrases: "product research",
  "find a product to sell", "validate this product", "is this a good product",
  "product opportunity", "should I sell this". Works with zero tools. the user
  describes the product and what they can observe.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Product Research

Product research is the highest-stakes decision a seller makes. everything after it
is execution on a choice already made. This skill validates a product opportunity
across the four things that decide it and returns a clear go or no-go.

## When to use this

- A seller has a product idea and wants it pressure-tested before committing.
- A seller is comparing several product ideas.
- A seller keeps picking products that look promising and then disappoint.
- Validating a product before sourcing or sampling.

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

## Step by step

1. **Collect inputs.** The product idea, category, typical price, what the user can
   observe about the top listings (reviews, ratings, image quality, complaints),
   rough costs, and any known patents, gating, or compliance issues.

2. **Score each corner.** Strong, mixed, or weak, each backed by evidence.

3. **Run the profit math** properly. landed cost, full fee stack, returns, storage,
   launch ads. Do not let a guess stand in for the calculation.

4. **Find the angle.** If this is a go, state the specific reason a new entrant wins:
   an unmet complaint, a weak incumbent, a price or quality gap.

5. **Verdict.** Go (at least three strong corners and a real angle), Investigate
   (mixed, name what data would settle it), or No-go (two weak corners or no angle).

6. **Run the quality check**, then deliver.

## Output format

```
## Product Research. [product]

### The Opportunity Square
Demand: [strong/mixed/weak] . [evidence]
Competition: [strong/mixed/weak] . [evidence]
Profit: [strong/mixed/weak] . [the net margin number]
Barrier to entry: [strong/mixed/weak] . [evidence]

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

Verdict: No-go as-is. Two weak-leaning corners, profit and barrier, and a low-price
product where ads eat the margin. The angle (better images, better listing) is real
but cannot fix a structurally thin margin. Investigate a higher-priced, clearly
premium version that lifts the profit corner before committing.

## Quality check

- All four corners are scored with evidence, not asserted.
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
- **Confirmation bias.** Researching to justify a product the seller already chose.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. 50 production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
