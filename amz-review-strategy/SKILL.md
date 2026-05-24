---
name: amz-review-strategy
description: >-
  Build a compliant Amazon review-generation strategy that grows review count
  and rating without breaking policy. Covers the Request a Review button, the
  Amazon Vine program (including a deep-dive on gating criteria, unit-count
  math, expected feedback quality, and when Vine is worth it vs not), product
  inserts, follow-up timing, and what is strictly prohibited. Use when a user
  asks how to get more reviews, increase review count, improve rating, the
  Request a Review button, Vine, product insert cards, review follow-up, the
  Vine program, Vine reviews, enrolling in Vine, getting first reviews on a new
  product, or whether Vine is worth it. Trigger phrases. "get more reviews",
  "review strategy", "increase reviews", "request a review", "Vine", "insert
  card", "improve my rating", "Vine program", "Vine reviews", "first reviews",
  "enroll in Vine", "is Vine worth it". Works with zero tools.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Review Strategy

Reviews are the trust layer of a listing. count and rating both move conversion. But
review generation is the single most dangerous area for an account, because the fast
methods are the prohibited ones. This skill builds a strategy that grows reviews using
only what Amazon allows.

## When to use this

- A new product has few reviews and needs a compliant ramp.
- A seller wants more reviews and is unsure what is allowed.
- A seller is considering Vine and wants to know if it fits.
- A seller has been doing something risky and needs a safe replacement.

## The hard line. what is prohibited

Start here, because crossing this line can suspend an account.

- **Never** offer a refund, a free product, money, a gift card, or any compensation
  in exchange for a review. The only Amazon-sanctioned exception is the Vine program.
- **Never** ask only happy customers for a review, or ask customers to change or
  remove a negative review.
- **Never** use review services that supply reviews, or review-exchange groups.
- **Never** review your own products or have family or staff do it.
- An insert card may **never** ask for a positive review or offer anything for a
  review. It may only point to genuine support and product registration.

If a tactic feels like a shortcut, it is almost certainly the prohibited kind.

## The framework. The Compliant Review Engine

Three legitimate sources, run together.

### 1. Request a Review

Amazon's own button (and the API behind it) sends the standardized, policy-safe
review request. It is the workhorse. The only lever is timing: request after the
product has been delivered and the customer has had a few days to actually use it,
not the moment it ships. Sent at the right time, to every order, it compounds.

### 2. Amazon Vine

Vine enrolls a product and gives units to Amazon's trusted reviewers for honest
reviews. It is the compliant way to get the first reviews on a new product. Use it
at launch to cross the cold-start barrier. See the Vine deep-dive below for the
gating criteria and the unit-count math.

### 3. The insert card, done right

A product insert can lift reviews indirectly and legally. It thanks the customer,
points to genuine support to resolve any problem before it becomes a 1-star review,
and offers product registration or a warranty. It must not ask for a positive review
or offer anything in exchange. Its real value is catching unhappy customers before
they leave a public review, and reminding happy ones the brand exists.

## Vine deep-dive

Vine is the only sanctioned way to seed reviews, and it works specifically because
the reviewers owe the seller nothing. That makes it safe and credible, and
unforgiving. Plan it carefully.

### Gating criteria. The Vine-ready test

Before enrolling, the product must pass all three:

- **Genuinely good.** The product does what the listing claims and the quality is
  real. Vine on a weak product produces honest 2-star reviews that are now permanent.
- **Listing is finished.** Title, images, A+, and copy are done. Vine reviewers
  review what they receive against what the listing promised. an unfinished listing
  invites expectation-gap reviews.
- **In stock.** There is no point seeding reviews onto a listing that cannot sell.

Fail the test and the fix is the product or the listing, not Vine.

### Unit-count math

Amazon offers Vine in three tiers per parent ASIN. 0, 10, or 30 units, with a 200
USD enrollment fee per parent (billed after the first review). The math.

- **30 units** is the right call for most launches. it crosses the credibility
  threshold where shoppers stop hesitating, typically lands the listing in the 15-25
  review range once Vine and early organic reviews layer.
- **10 units** is the right call when the seller wants to test reception with
  limited downside, or when stock is tight, or when the product is borderline-ready
  and 30 honest reviews on a weaker product would be costly to recover from.
- **0** is the right call when the product fails any Vine-ready test gate.

The true cost is the units given away plus the 200 USD fee. price the units at
landed cost, add the fee, and compare against the cost of running ads into a zero-
review listing that does not convert. Vine is almost always cheaper.

### Expected feedback quality

Vine reviews are a spread, not a wall of 5 stars. A genuinely good product
typically lands a Vine average a little below the eventual organic average, because
Vine reviewers grade harder than the average buyer. plan for that gap, do not
panic when it shows up. The critical Vine reviews are free product feedback, mine
them as a roadmap. Vine reviewers also tend to write longer and more detailed
reviews than organic shoppers, which helps Rufus and AI search match the listing
to specific buyer questions.

### When Vine is worth it vs not

Worth it.

- New product, listing finished, stock in, product genuinely good. Cold-start
  problem is the bottleneck.
- A relaunched listing or a child variation that resets review count and needs to
  cross the credibility threshold again.
- A product entering Q4 with too few reviews to convert holiday traffic.

Not worth it.

- A weak product or an unfinished listing. fix those first.
- A product with 100+ honest reviews already. Vine adds nothing the listing does
  not already have.
- A product where the seller cannot stomach an honest spread. Vine reviewers will
  write critical reviews if the product earns them, and those are permanent.

## Step by step

1. **Collect inputs.** The product, its age and current review count and rating,
   whether it is a launch or established, the listing completeness, the stock
   position, and what the seller is currently doing for reviews.

2. **Audit for risk first.** If the seller is doing anything on the prohibited list,
   that is the priority. stop it and replace it before anything else.

3. **Set Request a Review.** Confirm it is being sent to every eligible order at the
   right time. delivered plus a few days of use.

4. **Decide on Vine.** Run the Vine-ready test. If it passes, pick the unit tier
   from the math above and time enrollment at or just before launch. If it fails,
   route the fix to the product or the listing first.

5. **Design the insert.** Compliant copy: thanks, a support path, registration. no
   review ask, no incentive.

6. **Set expectations.** Reviews compound slowly. A compliant strategy is a steady
   curve, not a spike. Vine produces a spread, not a wall of 5 stars. Tie the plan
   to a realistic review-per-month estimate.

7. **Run the quality check**, then deliver.

## Output format

```
## Review Strategy. [product]

### Risk audit
[anything prohibited currently in use, and the immediate stop]

### The compliant engine
Request a Review: [timing and coverage]
Vine: [Vine-ready test result, unit tier if enrolling, timing, cost as a launch
       marketing line, or "fix product/listing first"]
Insert card: [compliant copy direction]

### Expectations
[realistic reviews per month, steady not spike. Vine spread is honest, not perfect]
[plan to mine critical Vine reviews as product feedback]
```

## Worked example

A new product, 11 reviews, 4.5 stars, genuinely good. The seller had been slipping a
card offering a 10 USD gift card for a 5-star review.

Risk audit: the gift-card offer is prohibited and an account risk. Stop immediately
and remove the card from all future units. The compliant engine: enroll the launch
in Vine at the 30-unit tier (listing finished, stock in, product genuinely good,
crosses the credibility threshold), switch Request a Review on for every order
timed to a few days after delivery, and replace the insert with a compliant card
that points to support and registration only. Vine cost is roughly 30 landed-cost
units plus the 200 USD fee, booked as a launch marketing line, cheaper than ads
into a thin-review listing. Expect a Vine average a touch below the eventual
organic average, and read the critical Vine reviews as a free product roadmap.
Reviews then grow steadily and the account is safe.

## Quality check

- The prohibited list is checked first. any incentivized or manipulated review tactic
  is flagged for an immediate stop.
- Request a Review is set to every eligible order, timed after real use.
- The Vine-ready test was run before recommending enrollment. a weak or unfinished
  product is not enrolled.
- The Vine unit count is matched to the launch stage (30 for cold start, 10 for
  tighter tests, 0 if the product is not ready).
- Timing for Vine is at or just before launch, when review count is near zero.
- The Vine cost is framed honestly as a launch marketing line, not as free.
- Expectations are set for an honest rating spread, not a perfect one.
- A plan exists to mine critical Vine reviews as product feedback.
- The insert card copy asks for no review and offers no incentive.

## Common mistakes

- **Incentivized reviews.** A gift card, refund, or free product for a review. the
  fastest way to lose an account.
- **Insert cards that ask for 5 stars.** A card steering customers to leave positive
  reviews is prohibited.
- **Vine on a weak product.** Honest reviewers produce honest low ratings that are
  now permanent on the listing.
- **Enrolling Vine before the listing is finished.** Reviewers judge against an
  unfinished listing and write expectation-gap reviews.
- **Expecting all 5 stars from Vine.** Vine is honest by design. a realistic spread
  is the point, and the critical reviews are useful.
- **Treating Vine as free.** The units and fee are a real launch cost. they are just
  a cost worth paying versus a zero-review listing.
- **Enrolling Vine too late.** Vine's value is the cold start. running it after the
  product already has reviews wastes most of the benefit.
- **Requesting too early.** Asking for a review before the customer has used the
  product wastes the request.
- **Cherry-picking.** Asking only the happy customers. that is manipulation and it is
  prohibited.

This skill is general guidance on Amazon policy. when in doubt, the Amazon Communication
Guidelines and policy pages are the authority.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
