---
name: amz-seller-analytics
description: >-
  Analyze an Amazon seller storefront or product portfolio for competitive
  intelligence. Estimates revenue, identifies the top products, reads the growth
  trajectory, and uncovers the strategy pattern from observable signals. Use
  when a user asks to analyze a seller or storefront, estimate a competitor's
  revenue, find a competitor's best products, understand a rival's strategy, or
  do competitive intelligence on a brand. Trigger phrases: "analyze this
  seller", "storefront analysis", "competitor revenue", "competitor strategy",
  "competitive intelligence", "what is this brand doing". Works with zero tools.
  the user pastes what they can observe about the seller.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Seller Analytics

A competitor's storefront is a strategy document in plain sight. Which products they
push, how they price, how they bundle, how fast they grew. it is all readable. This
skill reads a seller and reconstructs what they are doing and where they are exposed.

## When to use this

- Sizing a competitor before entering their niche.
- Understanding why a rival brand is winning.
- Finding a competitor's weak products to attack and strong ones to avoid.
- Studying a successful seller to learn the playbook.

## The framework. The Four Reads

A seller analysis answers four questions. Each is reconstructed from observable signals.

### Read 1. Size

Estimate the storefront's revenue. Estimate each product's monthly sales from its BSR
(see amz-sales-estimator), multiply by price, and sum. The output is a revenue range
with a confidence note, never a hard number.

### Read 2. The portfolio shape

Which products carry the seller. Almost every storefront follows the same shape: one
to three hero products produce most of the revenue, and a long tail produces little.
Identify the heroes and the tail. The heroes are where the seller is strong and
defended. The tail is where they are inattentive.

### Read 3. The trajectory

Is the seller growing, holding, or fading? Read it from review velocity: a hero with
a fast-rising recent review count is growing, one with reviews that have gone quiet
is fading. A storefront adding new listings is expanding. one that has not launched
in a year is coasting.

### Read 4. The strategy pattern

Reconstruct how they operate. Price positioning (premium, mid, budget). Do they
bundle. How heavy is their A+ and image investment. Are they ad-dependent (ranking
positions that look propped by sponsored placement) or organically strong. The
pattern tells you how to compete.

## Finding the exposure

Cross the reads. The opening is usually one of:

- A **neglected hero**. a top product with a tired listing or fading reviews. it
  carries their revenue and they stopped tending it.
- A **gap in the portfolio**. an obvious adjacent product they never launched.
- An **ad dependency**. heroes that rank only with heavy sponsored support, beatable
  by a more organically efficient listing.

## Step by step

1. **Collect inputs.** The storefront or seller, the products the user can observe
   with their BSRs, prices, review counts and recent velocity, and listing quality.

2. **Read 1, size.** Estimate per-product sales, sum to a storefront revenue range,
   state confidence.

3. **Read 2, portfolio shape.** Identify the heroes and the tail.

4. **Read 3, trajectory.** Growing, holding, or fading, from review velocity and
   launch activity.

5. **Read 4, strategy pattern.** Price position, bundling, content investment, ad
   dependency.

6. **Name the exposure.** The specific opening a competitor could attack.

7. **Run the quality check**, then deliver.

## Output format

```
## Seller Analysis. [storefront]

### Read 1. Size
Estimated storefront revenue: [range]  (estimate, confidence: [level])

### Read 2. Portfolio shape
Heroes: [products and est. share]
Tail: [count and rough share]

### Read 3. Trajectory
[growing / holding / fading] . [evidence]

### Read 4. Strategy pattern
Price position, bundling, content, ad dependency

### The exposure
[the specific opening to attack]
```

## Worked example

A competitor storefront, 14 listings. Estimated revenue a mid-six-figure annual
range, low confidence from snapshot BSRs. Portfolio shape: two heroes produce most of
it, twelve in the tail. Trajectory: hero one's review velocity has slowed sharply
over recent months, hero two is steady. Strategy: mid-priced, no bundles, decent A+,
and hero one's rank looks propped by heavy sponsored placement.

Exposure: hero one. it carries the storefront, its reviews have gone quiet, and its
rank is ad-dependent. A new entrant with a sharper listing and better organic
conversion could take share from it while the seller is not paying attention. Hero
two is healthy. avoid a direct fight there.

## Quality check

- Revenue is reported as a range with a confidence note, never a hard number.
- The portfolio is split into heroes and tail.
- Trajectory is backed by review velocity and launch activity, not a guess.
- The strategy pattern covers price, bundling, content, and ad dependency.
- A specific exposure is named, not a generic "they have weaknesses".
- All estimates are marked as estimates.

## Common mistakes

- **Reporting hard revenue numbers.** Storefront revenue is an estimate of estimates.
  it must be a range.
- **Treating all products equally.** Two heroes carry the business. the tail is noise.
- **Missing the trajectory.** A storefront that looks big today may be fading. or
  rising fast and about to be much bigger.
- **No exposure.** An analysis that describes the competitor but never says where to
  attack.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. 50 production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
