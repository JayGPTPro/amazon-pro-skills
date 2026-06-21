---
name: amz-product-bundling
description: >-
  Design Amazon product bundles and multipacks that lift average order value and
  margin. Covers virtual bundles, physical bundles, multipacks, the right
  pairing logic, bundle pricing, and listing setup. Use when a user asks about
  bundling products, virtual bundles, multipacks, what to bundle, bundle
  pricing, raising average order value, or creating a set. Trigger phrases:
  "product bundle", "virtual bundle", "multipack", "what should I bundle",
  "bundle pricing", "raise AOV", "create a set". Works with zero tools.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Product Bundle Designer

A bundle is the cheapest way to raise average order value on Amazon. no new product,
no new ad spend, just a smarter offer. But a random bundle of unrelated items does
not sell. This skill designs bundles around how customers actually buy.

## When to use this

- A seller has several related SKUs and never bundled them.
- Average order value is low and the seller wants to lift it without new products.
- A market basket report shows products bought together (see amz-brand-analytics).
- A seller wants a higher-priced offer to sit alongside the single unit.

## The framework. The Bundle Logic

A bundle works when the items belong together in the customer's mind. Three valid
bundle types. anything else is a random grab bag that does not convert.

| Bundle type | Logic | Example |
|-------------|-------|---------|
| Complete-the-job | Everything needed to do the task once | Coffee + filters + scoop |
| Use-it-up multipack | More of a consumable the buyer will rebuy anyway | 3-pack of the refill |
| Good-better tier | The single unit plus the accessory that upgrades it | Knife + the sharpener and guard |

The test: would a real customer have searched for both items in the same session? If
yes, the bundle has logic. If no, it is a grab bag.

## Virtual versus physical bundles

- **Virtual Bundle.** A Brand Registry tool. Links existing listings into one bundle
  page. no new packaging, no new inventory, the items still ship separately. Fast,
  low-risk, reversible. Start here.
- **Physical bundle.** Items packed and shipped as one unit, one SKU, one barcode.
  More work and committed inventory, but it can win the bundle keyword and control
  the unboxing. Use it when the bundle is proven and worth the commitment.
- **Multipack.** Several of the same item as one SKU. The simplest. strong for
  consumables.

## Bundle pricing

The bundle must give the buyer a visible reason to choose it over buying the parts
separately, while still earning more total margin than a single unit.

- Price the bundle below the sum of the individual prices. a 5 to 15 percent bundle
  saving is typical.
- Confirm the bundle's total contribution margin, after all fees on the bundle, beats
  the single-unit margin. The point is more margin per order, not just a bigger price.
- Never bundle so deep that the bundle cannibalizes the single unit at a worse margin.

## Step by step

1. **Collect inputs.** The catalog of related SKUs, their prices and margins, any
   market-basket or co-purchase data, and whether the brand is Brand Registered.

2. **Find the pairings.** Apply the bundle logic. Group SKUs into complete-the-job,
   use-it-up, or good-better bundles. Reject any grab-bag pairing.

3. **Choose the format.** Virtual bundle to start (fast, reversible). physical or
   multipack when the bundle is proven or the format genuinely wins.

4. **Price each bundle.** Set the bundle saving, then confirm the bundle's total
   contribution margin beats the single unit.

5. **Plan the listing.** A bundle needs its own images showing all items together,
   copy that sells the combined outcome, and bundle keywords ("set", "kit", "bundle").

6. **Run the quality check**, then deliver.

## Output format

```
## Bundle Plan. [brand]

### Bundle 1
Items: [SKUs]
Logic: [complete-the-job / use-it-up / good-better]
Format: [virtual / physical / multipack]
Price: [$] (vs [$] bought separately, [X]% saving)
Margin check: bundle contribution [$] vs single-unit [$]

### Listing notes
[images, copy angle, bundle keywords]
```

## Worked example

A coffee brand with three SKUs: whole-bean coffee, paper filters, a measuring scoop.

Bundle: complete-the-job, all three as a virtual bundle. The customer who buys beans
needs filters and a scoop in the same session. Priced at a 10 percent saving versus
buying the three separately. Margin check: the bundle's contribution after fees beats
the bean-only order, because the filters and scoop carry margin too. Virtual bundle
chosen first. no new inventory, reversible, and if it sells well it becomes a
physical kit later.

## Quality check

- Every bundle passes the same-session test. the items belong together.
- No grab-bag bundles of unrelated items.
- The format is justified. virtual to start unless physical genuinely wins.
- The bundle price shows a visible saving versus buying the parts separately.
- The bundle's total contribution margin beats the single-unit margin. confirmed.
- The bundle has its own images, copy, and keywords planned.

## Common mistakes

- **Grab-bag bundles.** Pairing unrelated SKUs because they are both slow movers.
- **Bundling at a worse margin.** A discount so deep the bundle earns less than a
  single sale would.
- **Physical first.** Committing packaging and inventory before a virtual bundle has
  proven the demand.
- **No bundle listing.** Reusing the single-unit images so the buyer cannot see they
  get all the items.
- **Cannibalizing the hero SKU.** A bundle priced so well it steals single-unit
  sales at a lower margin.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
