---
name: amz-wholesale-sourcing
description: >-
  Plan Amazon wholesale sourcing. finding suppliers and brands to resell,
  opening wholesale accounts, negotiating terms and minimum order quantities,
  and checking that a wholesale deal is actually profitable and not gated. Use
  when a user asks about wholesale sourcing, finding suppliers, reselling
  brands, opening wholesale accounts, negotiating with distributors, or
  evaluating a wholesale product. Trigger phrases: "wholesale", "wholesale
  sourcing", "find suppliers", "resell brands", "distributor", "wholesale
  account", "MOQ negotiation". Works with zero tools.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Wholesale Sourcing

Wholesale on Amazon means buying established branded products from authorized
suppliers and reselling them. It skips product development, but it has its own trap:
most wholesale products, by the time you find them, are already a crowded, low-margin
fight. This skill finds the wholesale deals that actually pay.

## When to use this

- A seller wants to start or grow a wholesale (reselling) business on Amazon.
- A seller has a supplier offer and needs to know if it is a good deal.
- A seller keeps finding wholesale products that turn out unprofitable.
- Preparing to approach brands and distributors.

## The framework. The Wholesale Deal Test

A wholesale product is worth pursuing only when it clears five gates. The first two
are pass-or-fail.

1. **Authorized and ungated.** The supplier must be the brand or a genuinely
   authorized distributor, and the seller must be able to get ungated for the brand
   and category if they are gated. An unauthorized source is a counterfeit and
   intellectual-property risk. Pass or fail.

2. **The margin survives the crowd.** Wholesale listings are usually shared, many
   sellers on one listing, and the Buy Box rotates on price. The real question is not
   the margin at today's price, it is the margin at the price the Buy Box will settle
   to once you join the competition. If that margin is not positive, the deal fails.

3. **Buy Box reachability.** How many sellers are already on the listing, and are any
   of them the brand itself or Amazon? A listing the brand or Amazon dominates leaves
   little Buy Box share for a new reseller.

4. **Demand.** The product sells at a steady rate, enough that your share of the Buy
   Box rotation still moves real volume.

5. **Terms.** The minimum order quantity, the unit price, payment terms, and lead
   time are workable for the seller's cash position.

Fail gate 1 or gate 2 and the deal is dead regardless of the rest.

## Finding and approaching suppliers

- Target brands whose products sell well on Amazon but whose listings are not already
  swarmed by resellers, or where the brand wants more distribution.
- Approach as a real business: a registered entity, a resale certificate, a
  professional pitch. Brands screen out hobbyists.
- Ask directly whether the brand restricts Amazon selling. many do, and selling
  against a brand's wishes invites complaints and takedowns.

## Negotiation levers

- **Minimum order quantity.** Often negotiable, especially for a first order. ask for
  a smaller trial quantity to test the product before a large commitment.
- **Unit price.** Improves with volume and with a relationship. the first order
  rarely gets the best price.
- **Payment terms.** Net terms instead of payment up front free up cash.
- **Exclusivity or restricted distribution.** The strongest lever. a brand that
  limits how many sellers it authorizes protects the reseller's margin. worth more
  than a small price cut.

## Step by step

1. **Collect inputs.** The supplier or brand, the product, the wholesale unit price,
   the minimum order quantity, the current Amazon listing situation (sellers on it,
   price, brand or Amazon present), and the demand signal.

2. **Run gate 1.** Confirm the source is authorized and the brand and category are
   ungated or ungatable.

3. **Run gate 2.** Project the Buy Box settling price once the seller joins, and
   compute the margin at that price through the full fee stack. This is the real
   number.

4. **Run gates 3 to 5.** Buy Box reachability, demand, and terms.

5. **Verdict.** Pursue, negotiate (the deal works only if a specific term improves),
   or pass.

6. **If pursuing, set the negotiation plan.** Which levers to push, starting with a
   trial order quantity and, where possible, restricted distribution.

7. **Run the quality check**, then deliver.

## Output format

```
## Wholesale Deal Evaluation. [product / brand]

### The five gates
1. Authorized and ungated: [pass / fail]
2. Margin at the Buy Box settling price: [the number] . [pass / fail]
3. Buy Box reachability: [score]
4. Demand: [score]
5. Terms (MOQ, price, payment, lead time): [score]

### Verdict: [PURSUE / NEGOTIATE / PASS]
[reasoning]

### Negotiation plan (if pursuing)
[levers to push, starting with a trial order and restricted distribution]
```

## Worked example

A distributor offers a known kitchen brand at a wholesale price that looks like a
healthy margin against the current Amazon price.

Gate 1: the distributor is authorized, the brand is not gated. pass. Gate 2: the
listing already has eight resellers and the Buy Box price has been drifting down. At
the price the Buy Box will realistically settle to once a ninth seller joins, the
margin through the full fee stack is barely positive. The "healthy margin" was an
illusion of today's price. Gate 3: eight sellers already, so Buy Box share per seller
is thin.

Verdict: Negotiate, and only pursue if the distributor will grant restricted
distribution or a materially lower price. Without one of those, this is a crowded
low-margin listing and the deal is a pass.

## Quality check

- The source is confirmed authorized, and the brand and category gating is checked.
- The margin is computed at the projected Buy Box settling price, not today's price.
- Buy Box reachability accounts for the number of sellers and whether the brand or
  Amazon is on the listing.
- The verdict is Pursue, Negotiate, or Pass, with reasoning.
- A negotiation plan leads with a trial order and restricted distribution, not just
  a price cut.

## Common mistakes

- **Margin at today's price.** The Buy Box price falls as you join the competition.
  the deal must be judged at the future price.
- **Unauthorized sources.** Buying from a non-authorized seller risks counterfeit and
  intellectual-property complaints and a takedown.
- **Ignoring the crowd.** A listing with a dozen resellers splits the Buy Box so thin
  that even a positive margin earns little.
- **Big first order.** Committing to a large minimum order quantity before testing
  the product's real Buy Box economics.
- **Chasing price, not distribution.** A small price cut is worth far less than a
  brand limiting how many sellers it authorizes.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
