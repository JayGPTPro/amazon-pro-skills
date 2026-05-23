---
name: amz-repricing-strategy
description: >-
  Build an Amazon repricing strategy that protects margin instead of racing to
  the bottom. Sets a price floor and ceiling, defines rules for Buy Box defense,
  and decides when to compete on price and when not to. Use when a user asks
  about repricing, repricer settings, price wars, a competitor undercutting
  them, setting a price floor, or dynamic pricing on Amazon. Trigger phrases:
  "repricing", "repricer", "price war", "competitor undercut", "price floor",
  "dynamic pricing", "automatic pricing". Works with zero tools.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Repricing Strategy

Most repricers are set to one rule: be the cheapest. That rule wins the Buy Box and
loses the business. Repricing done right defends margin, not just price. This skill
builds a repricing strategy with a floor that cannot be crossed.

## When to use this

- A seller is setting up a repricer and does not want a race to the bottom.
- A competitor is undercutting and the seller is tempted to chase.
- Margins are eroding and the repricer is suspected.
- A seller on a shared listing needs Buy Box rules that still make money.

## The framework. The Price Corridor

Never reprice to a single target. Reprice inside a corridor with a hard floor and a
ceiling. The repricer may move freely between them and must never cross either.

### The floor. non-negotiable

The floor is the lowest price that still earns an acceptable contribution margin
after the full fee stack. Compute it: floor equals landed cost, plus fees, plus the
minimum acceptable contribution. The repricer is never allowed below it. If winning
the Buy Box requires going below the floor, you do not want that Buy Box. that sale
loses money.

### The ceiling

The ceiling is the highest price the listing converts at. when you hold the Buy Box
uncontested, the repricer should drift up toward it, not sit at the floor. Most
sellers leave money on the table by camping at a low price even when nobody is
competing.

### The rules between floor and ceiling

- **Own brand, sole seller.** No repricing war is possible. Sit near the ceiling,
  adjust only for demand. The threat is price suppression, not competitors.
- **Own brand, resellers present.** The real fix is brand protection, not a price
  war. see amz-buy-box. Reprice only to the floor, never below, and remove
  unauthorized sellers.
- **Shared listing, reselling.** Compete inside the corridor. Match or slightly beat
  the competing offer down to the floor, and stop. When rivals stock out or raise,
  drift back up toward the ceiling.

## Step by step

1. **Collect inputs.** Landed cost, the full fee stack, the minimum acceptable
   contribution margin, the listing type (own brand sole, own brand with resellers,
   shared), and the current price and competition.

2. **Compute the floor.** Landed cost plus fees plus minimum contribution. This is
   the hard stop.

3. **Set the ceiling** from the highest price the listing has converted well at.

4. **Pick the rule set** for the listing type.

5. **Define the repricer behavior.** When to move down (a real competing offer above
   the floor), when to hold (at the floor, do not chase below), when to drift up
   (uncontested, move toward the ceiling).

6. **Add the alerts.** Flag when a competitor sits below your floor (let them lose
   money, do not follow) and when you have been camped at the floor while uncontested.

7. **Run the quality check**, then deliver.

## Output format

```
## Repricing Strategy. [product]

Listing type: [own sole / own with resellers / shared]

### Price corridor
Floor: [$]  (landed cost + fees + min contribution)
Ceiling: [$]  (best-converting high price)
Current price: [$]

### Repricer rules
Move down when: ...
Hold when: ...
Drift up when: ...
Never: cross the floor

### Alerts
[competitor-below-floor and camped-at-floor alerts]
```

## Worked example

A shared listing, the seller is reselling. Landed cost plus fees is 22 USD, minimum
acceptable contribution 4 USD, so the floor is 26 USD. The listing converts well up
to a ceiling of 34. A competitor drops to 24.

Rule: the competitor is below the 26 floor. Do not follow. They are selling at a loss
or on worse economics. Hold at the floor, 26, and let their stock run down. When they
sell out or raise, the repricer drifts the price back up toward 34. Chasing them to
24 would have meant selling every unit at a loss to win a Buy Box not worth winning.

## Quality check

- A hard floor is computed from landed cost, fees, and a minimum contribution margin.
- The repricer is never allowed below the floor, even to win the Buy Box.
- A ceiling is set and the strategy drifts up toward it when uncontested.
- The rule set matches the listing type. own-brand reseller cases route to brand
  protection, not a price war.
- Alerts cover both a competitor below the floor and camping at the floor uncontested.

## Common mistakes

- **Race to the bottom.** A repricer set to always be cheapest, with no floor,
  selling at a loss to win a Buy Box.
- **No floor at all.** The repricer chases a competitor straight through profitability.
- **Camping at the floor.** Holding a low price even when no competitor is present,
  leaving margin on the table.
- **Price-warring your own brand.** Fighting resellers on price instead of removing
  them through Brand Registry.
- **Following a loss-leader.** Matching a competitor who is below your floor and is
  themselves losing money.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. 50 production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
