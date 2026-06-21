---
name: amz-sales-estimator
description: >-
  Estimate Amazon monthly sales and revenue from a Best Seller Rank, and size a
  niche or competitor from observable signals. Explains the BSR-to-sales
  relationship, adjusts by category and price, and returns a sales range with a
  confidence note. Use when a user asks how many units a product sells, to
  estimate sales from BSR, size a market or niche, gauge a competitor's volume,
  or judge demand. Trigger phrases: "sales estimate", "how many units",
  "estimate from BSR", "best seller rank", "market size", "competitor sales",
  "monthly sales". Works with zero tools. the user provides BSR, category, and
  price.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Sales Estimator

Best Seller Rank is the one demand signal Amazon shows publicly. It is not a sales
number, but it can be read into a sales range. This skill turns a BSR into an
estimate, and a set of BSRs into a market size, with honest confidence bounds.

## When to use this

- Estimating how many units a product or competitor sells per month.
- Sizing a niche from the BSRs of its top listings.
- Judging whether demand justifies entering a category.
- Comparing the demand behind two products or two price points.

## The framework. The Rank Curve Read

BSR is a rank, not a count. You never convert it with a magic constant. you read it
against the sales curve it sits on. The Rank Curve Read is three properties of that
curve, and every honest estimate has to respect all three.

1. **It is category-specific.** A BSR of 5,000 in a huge category (Home, Kitchen,
   Beauty) means far more sales than 5,000 in a small one. Always estimate within the
   product's main category, never across categories.

2. **The curve is steep at the top, flat in the tail.** The difference between rank
   100 and rank 1,000 is enormous. The difference between rank 50,000 and rank 60,000
   is small. A small rank change near the top is a big sales change. near the tail it
   is almost nothing.

3. **It is a snapshot, not an average.** BSR updates frequently and swings with every
   sale. One reading is noisy. An estimate is far stronger from several readings over
   days, or from the more stable 30-day average rank if available.

## The estimate method

1. Identify the **main category** the BSR belongs to and roughly how large that
   category is.
2. Place the BSR on the curve: top (steep), middle, or deep tail.
3. Produce a **range, never a single number.** A top-of-category BSR might be
   estimated as a wide band of units per month. The honest output is a range plus a
   confidence level.
4. **Sanity-check against price and reviews.** A very high estimated volume on a
   product with very few recent reviews is a flag that the BSR reading is a spike or
   the category is small. Cross-check.
5. **Mark every estimate with a warning symbol.** This is an estimate, not data.

## Sizing a niche

To size a niche, estimate the top 10 to 20 listings on page one, sum the ranges, and
report the niche as a band. Note the **concentration**: if two listings hold most of
the volume, it is a winner-take-most niche and a new entrant fights for scraps. if
volume is spread across many listings, there is room.

## Step by step

1. **Collect inputs.** The BSR or BSRs, the main category, the price, the review
   count, and whether the BSR is a single snapshot or a multi-day or 30-day figure.

2. **Flag the data quality.** A single snapshot gets a wide range and a low confidence
   note. Recommend multiple readings.

3. **Estimate the range** per product, category-aware, curve-aware.

4. **Sanity-check** against price and review velocity.

5. **For a niche,** sum the page-one estimates and report concentration.

6. **State confidence** and mark estimates with a warning symbol.

7. **Run the quality check**, then deliver.

## Output format

```
## Sales Estimate. [product or niche]

Category: [main category]   BSR: [value, snapshot or average]

### Estimate
Monthly units: [low] to [high]  (estimate)
Monthly revenue: [low] to [high]  (estimate)
Confidence: [low / medium] . [why]

### Sanity check
[does the review velocity and price support this?]

### Niche size (if applicable)
Page-one total: [range]   Concentration: [winner-take-most / spread]
```

## Worked example

A product at BSR 4,000 in a large category, price 25 USD, single snapshot.

Large category and a fairly strong rank, so a meaningful volume, but a single
snapshot, so the range is wide and confidence is low. Estimate: a broad band of units
per month, revenue the band times 25. Sanity check: the listing has steady recent
reviews, consistent with real ongoing sales, so the estimate is plausible.
Recommendation: take three more BSR readings across a week, or use the 30-day average
rank, to tighten the range before making a sourcing decision on it.

## Quality check

- The estimate is made within the product's main category, never across categories.
- The estimate is a range, never a single hard number.
- The steep-top, flat-tail shape of the curve is reflected in the estimate.
- A single-snapshot BSR is flagged as low confidence with a recommendation to take
  more readings.
- The estimate is sanity-checked against price and review velocity.
- Every estimate carries a warning symbol and a confidence level.

## Common mistakes

- **Treating an estimate as data.** Sourcing thousands of units on one BSR reading.
- **Comparing BSRs across categories.** Rank 5,000 means different things in
  different categories.
- **A single number.** Reporting "this product sells 900 units a month" with no range
  and no confidence.
- **One snapshot.** BSR swings with every sale. one reading is noise.
- **Ignoring concentration.** A big niche where two listings own it is not the
  opportunity the total makes it look.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
