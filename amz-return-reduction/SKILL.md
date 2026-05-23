---
name: amz-return-reduction
description: >-
  Diagnose why an Amazon product gets returned and build a plan to cut the
  return rate. Reads return reasons and reviews, finds the root cause, and fixes
  it at the listing, the product, or the packaging. Use when a user asks about
  reducing returns, a high return rate, why customers return a product, return
  reasons, or refunds eating profit. Trigger phrases: "reduce returns", "return
  rate", "why are customers returning", "return reasons", "too many refunds",
  "cut returns". Works with zero tools. the user pastes return reasons and
  reviews.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Return Reduction

Every return costs twice: the refunded sale and the return processing, often plus a
unit that cannot be resold. A high return rate also drags rank and risks the listing.
Most returns trace to a small number of root causes. This skill finds them and fixes
them at the source.

## When to use this

- A product's return rate is above the category norm.
- Refunds are visibly eating into profit.
- A seller wants to know why a specific product gets sent back.
- A return rate is climbing and the cause is unclear.

## The framework. The Return Root Map

Returns are not random. Almost every one is one of five root causes, and each has a
different fix. Reading return reasons and the 1 to 3 star reviews tells you which.

| Root cause | The signal | The fix lives in |
|------------|-----------|------------------|
| Expectation gap | "Not as described", "smaller than expected" | The listing. images and copy oversold or under-informed |
| Sizing or fit | "Too small", "wrong size", "did not fit" | A size guide, clearer dimensions, better sizing copy |
| Defect or quality | "Broken", "stopped working", "poor quality" | The product or the supplier. a real quality issue |
| Damaged in transit | "Arrived damaged", "box crushed" | The packaging. protection and FBA prep |
| Changed mind or wrong item | "No longer needed", "bought by mistake" | Mostly unavoidable. do not over-fix this bucket |

The diagnosis rule: an expectation gap is a listing problem and is the cheapest to
fix. A defect is a product problem and the most expensive to ignore. Never treat all
returns as one thing.

## Step by step

1. **Collect inputs.** The return reasons and their counts if available, the 1 to 3
   star reviews, the product, the listing copy and images, and the packaging.

2. **Sort every return into a root cause.** Build the distribution. which root cause
   is the biggest share.

3. **Diagnose the dominant cause.** Focus the plan on the one or two biggest buckets.
   Ignore the "changed mind" bucket. chasing it wastes effort.

4. **Fix at the source.**
   - Expectation gap: correct the images and copy so the listing promises exactly
     what arrives. often the listing is overselling. dial it to honest.
   - Sizing: add a size guide, put real dimensions in the images, rewrite the sizing
     copy.
   - Defect: this is a supplier or design problem. quantify the cost and address the
     product, not the listing.
   - Transit damage: improve protective packaging and FBA prep. see amz-fba-prep.

5. **Estimate the impact.** Roughly, cutting the dominant bucket by half saves what?
   Tie it to a dollar figure so the fix is prioritized correctly.

6. **Run the quality check**, then deliver.

## Output format

```
## Return Reduction Plan. [product]

### Return root distribution
Expectation gap: [%]
Sizing or fit: [%]
Defect or quality: [%]
Transit damage: [%]
Changed mind: [%]

### Dominant cause: [cause]

### The fix
[specific changes at the listing, product, or packaging]

### Estimated impact
[rough refund and return-cost saving if the dominant bucket is halved]
```

## Worked example

A pair of headphones, return rate well above the category norm. Return reasons and
reviews sorted: 55 percent expectation gap ("the bass is weak", "looked bigger in the
photos"), 20 percent defect, 15 percent changed mind, 10 percent transit.

Dominant cause: expectation gap. The listing images make the headphones look larger
and the copy promises "deep, powerful bass" the product does not deliver. Fix: reshoot
with honest scale, add a size reference, and rewrite the audio copy to describe the
sound accurately rather than overselling it. Honest copy sells slightly fewer units
but the ones it sells stay sold, and the return cost and the rank drag both fall.

## Quality check

- Every return is sorted into one of the five root causes.
- The plan focuses on the dominant one or two buckets, not all of them.
- The "changed mind" bucket is acknowledged as mostly unavoidable, not over-fixed.
- Expectation-gap fixes make the listing honest, not just prettier.
- Defects are sent to the product or supplier, not patched with copy.
- The impact is tied to a rough dollar saving.

## Common mistakes

- **Treating returns as one problem.** A defect and an expectation gap need opposite
  fixes. lumping them wastes the effort.
- **Overselling the listing.** Images and copy that promise more than the product
  delivers buy a sale and then a return.
- **Patching a defect with copy.** No listing change fixes a product that breaks.
- **Chasing "changed mind" returns.** Mostly unavoidable. effort spent there is wasted.
- **Ignoring the rank cost.** A high return rate is not only refunds. it drags
  organic rank too.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. 50 production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
