---
name: amz-brand-tailored-promotions
description: >-
  Plan Amazon Brand Tailored Promotions. targeted discounts sent to specific
  shopper audiences such as repeat customers, recent customers, brand followers,
  cart abandoners, and high-spend shoppers. Picks the right audience, the right
  discount depth, and the right goal for each promotion. Use when a user asks
  about Brand Tailored Promotions, targeting past customers with a discount,
  re-engaging repeat buyers, rewarding brand followers, or winning back lapsed
  customers. Trigger phrases: "brand tailored promotions", "BTP", "target repeat
  customers", "win back customers", "brand follower discount". Works with zero
  tools. the user describes their brand and audience sizes.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Brand Tailored Promotions Planner

Brand Tailored Promotions let a brand send a discount to a specific, pre-built
audience of real shoppers. most sellers either ignore the tool or blast the same
generic 10 percent to everyone. This skill matches the audience to the goal so each
promotion does one job well.

## When to use this

- A brand wants to re-engage past customers instead of only chasing new ones.
- Inventory needs to move and a broad coupon would waste margin on full-price buyers.
- A brand has followers or a loyal base and never rewards them.
- The seller wants repeat purchase rate to climb.

## The framework. Audience to Goal Match

Each built-in audience exists for a different reason. Sending the wrong offer to the
wrong audience either wastes margin or fails to move. Match them.

| Audience | What they are | The right goal | Discount depth |
|----------|---------------|----------------|----------------|
| Brand followers | Opted in, warmest | Reward, launch new SKU | Low, 10 to 15% |
| Repeat customers | Bought 2+ times | Deepen loyalty, subscribe | Low to mid |
| Recent customers | Bought once, lately | Cross-sell a complement | Mid |
| High-spend customers | Top spenders | New or premium SKU | Low. they pay full price already |
| Cart abandoners | Added, did not buy | Convert the hesitation | Mid to deep |
| Lapsed customers | Bought long ago | Win back | Deep, 20%+ |

The rule: the colder and more hesitant the audience, the deeper the discount. Warm
audiences need a reason, not a bribe. Cold audiences need a real incentive.

## Step by step

1. **Collect inputs.** The goal (move stock, launch a SKU, raise repeat rate, win
   back), the audiences available and their sizes, the product and its margin, and
   any deadline. Ask one compact follow-up if the goal is unclear.

2. **Pick the audience that matches the goal**, using the table. Do not default to
   "all customers".

3. **Set the discount depth** by audience temperature. Never discount a high-spend
   audience deeply. they convert at full price and you would burn margin.

4. **Check the margin floor.** Confirm the discounted price still clears contribution
   margin after fees. If not, reduce depth or pick a different audience.

5. **Define the offer and the window.** Short windows (3 to 7 days) create urgency.
   Pair the audience, the SKU, the depth, and the dates.

6. **Plan the sequence.** If running several, order them: reward followers first,
   then cross-sell recent buyers, then win back lapsed. Do not overlap audiences in
   a way that lets one shopper stack offers.

7. **Run the quality check**, then deliver.

## Output format

```
## Brand Tailored Promotions Plan. [brand]

Goal: [stated goal]

### Promotion 1
Audience: [audience] . size: [N]
SKU: [product]
Discount: [depth] . discounted price: [$] . margin after: [$]
Window: [dates]
Why this match: [one line]

### Sequence
[order and timing if multiple]
```

## Worked example

Goal: raise repeat purchase rate on a coffee brand.

- Promotion 1: Repeat customers audience, 12 percent off the subscribe-and-save
  starter, 5-day window. Goal is to convert proven buyers into subscribers.
- Promotion 2: Recent customers audience, 15 percent off the complementary grinder.
  Goal is the cross-sell while the brand is fresh in mind.
- High-spend audience deliberately excluded. they already buy at full price. a
  discount there is pure margin loss.

## Quality check

- Each promotion has one audience matched to one goal, per the table.
- Discount depth scales with audience temperature. warm shallow, cold deep.
- The discounted price clears contribution margin. confirmed, not assumed.
- High-spend audiences are not deeply discounted.
- Windows are short enough to create urgency.
- Multiple promotions are sequenced so one shopper cannot stack them.

## Common mistakes

- **One offer for everyone.** The same 10 percent to followers and to lapsed buyers
  underpays the cold audience and overpays the warm one.
- **Deep-discounting top spenders.** Handing margin to people who would have paid full.
- **No margin check.** A promotion that sells below contribution margin loses money
  on every unit.
- **Open-ended windows.** No deadline, no urgency, no spike.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
