---
name: amz-pricing-war-defense
description: >-
  Detect when a competitor or hijacker has started a price war on your ASIN
  and respond without racing to the bottom. Diagnoses the attacker (real
  competitor, reseller, hijacker), and recommends Buy Box defense moves
  (coupon, bundle, variation split, walk-away). Use when a user asks about a
  price war, competitor undercutting, race to the bottom on Amazon, or
  defending pricing. Trigger phrases: "price war", "undercut", "race to the
  bottom", "competitor dropped price", "pricing attack". Works with zero tools.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Pricing War Defense

A price war is a margin-destroying spiral. The seller who refuses to fight wins,
but only if they have moves besides the price. This skill diagnoses the attacker
and chooses the response.

## When to use this

- A competitor or new seller dropped price on the same listing or a parallel one.
- A hijacker is on your brand's listing pulling down the price.
- An automated repricer is producing a slow downward drift across the niche.
- The seller's instinct is to match. that is usually wrong.

## The framework. The Three Attacker Types

Each type has a different response.

| Attacker | Signal | Response |
|----------|--------|----------|
| Hijacker on your listing | Unauthorized seller on your brand's ASIN | Route to amz-hijacker-removal. do not engage on price |
| Reseller race on a shared listing | Multiple sellers, prices drifting down | Set the floor (amz-repricing-strategy) and hold. let competitors lose money below |
| Real competitor on a parallel listing | A different ASIN, your direct competitor lowered price | Differentiate, do not match |

## The response ladder for a real competitor

When a real competitor lowers price, the response is rarely to match. Climb the
ladder.

1. **Wait one week.** Many price drops are short experiments. they revert when
   sales do not respond enough.
2. **Add a coupon** (amz-coupon-strategy). Earn the green badge at 5-10 percent
   without permanently moving the price. Often defends share without the spiral.
3. **Add a bundle** (amz-product-bundling). A multi-pack or accessory bundle
   moves the comparison off price.
4. **Split the variation.** If the competitor cut their cheapest variant, your
   matching variant can match while your premium variant holds price. Selective.
5. **Walk away.** If the competitor's price is genuinely below your break-even,
   let them have those sales. you keep margin. they lose money on every unit.

Match the price only if all four above fail and you have a real cost advantage to
sustain it.

## Step by step

1. **Collect inputs.** Your ASIN, the attacker (seller name or competitor ASIN),
   the price change observed, the timing, your floor (from amz-repricing-strategy
   or compute now), your current Buy Box share.

2. **Identify the attacker type.** Hijacker, reseller, or real competitor.

3. **For hijackers:** route to amz-hijacker-removal. do not engage on price.

4. **For resellers:** route to amz-repricing-strategy. Hold at the floor.

5. **For real competitors:** climb the response ladder. start at step 1 (wait one
   week) and only escalate if share is materially lost.

6. **Set the metrics to watch.** Buy Box share, units per day, profit per unit.
   not just price.

7. **Document the playbook.** Same attacker will likely try again. record what
   worked.

8. **Run the quality check**, then deliver.

## Output format

```
## Price War Defense. [ASIN]

Attacker type: [hijacker / reseller / real competitor]
Their price: [$]   Your price: [$]   Your floor: [$]

### Response
[ladder step chosen and reasoning]

### Watch
Buy Box share, units/day, profit/unit. not just price.

### If response fails
[escalation step on the ladder]
```

## Worked example

A real competitor on a parallel listing dropped their price from 35 USD to 28 USD.
Your floor is 30 USD. Initial impulse: match. Plan: wait one week, monitor share.
If share holds (sometimes shoppers do not switch), do nothing. If share drops, add
a coupon for 10% off at 35 USD, earning the green badge without moving the price.
If share continues to drop after the coupon, bundle with an accessory at 39 USD to
move the comparison off direct price. Only if all of these fail, and you have a
cost advantage at 30 USD, consider matching. Most often, the competitor's 28 USD
move is a short experiment that reverts within 2-3 weeks.

## Quality check

- The attacker type is identified before any response.
- Hijackers route to brand protection, not price war.
- Resellers route to repricer floor, not price war.
- Real competitors get the response ladder, starting from the lowest step.
- Matching price is the last option, not the first.
- Metrics watched include share and profit, not just price.

## Common mistakes

- **Matching reflexively.** The fastest way to lose margin.
- **Treating a hijacker like a competitor.** Fighting them on price funds their
  margin race and ignores brand protection tools.
- **No floor.** No floor means no end to the race.
- **One metric.** Watching price without watching share, units, and profit means
  you cannot tell if the war is being lost or not.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
