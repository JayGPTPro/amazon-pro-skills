---
name: amz-supplier-negotiation-script
description: >-
  Generate a structured negotiation script for Alibaba, Canton, or domestic
  suppliers. Covers 7 levers (unit price, MOQ, payment terms, lead time,
  packaging, QC, tariff sharing) and produces email templates per negotiation
  round. Use when a user asks how to negotiate with a supplier, Alibaba
  negotiation, MOQ negotiation, supplier email scripts, or getting better
  terms. Trigger phrases: "negotiate supplier", "Alibaba", "MOQ", "payment
  terms", "supplier script", "supplier email". Works with zero tools.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Supplier Negotiation Script

Most sellers negotiate price only and leave 5-15 percent of margin on the table by
not negotiating the rest. A real negotiation uses seven levers in sequence. this
skill produces the scripts.

## When to use this

- First contact with a new supplier and you want the right opening.
- Existing supplier and you want better terms on the next order.
- Diversifying to a new origin and negotiating from scratch.
- Volume jumping and the seller wants to capture the leverage.

## The framework. The Seven Levers

Negotiate in this order. each lever is a separate ask, not all at once.

1. **Unit price.** The obvious one. Anchor with a target based on benchmark research
   or competitor sourcing. Always ask for the best price, not a number you will
   accept.

2. **MOQ (minimum order quantity).** Suppliers quote a high default. for a first
   order, request a smaller trial MOQ to test before commitment.

3. **Payment terms.** The default is 30% deposit, 70% on shipment. Negotiate to a
   smaller deposit (10-20%) with the balance net 30, or a 30/60/10 split where the
   final 10% is held until quality is confirmed. LC and escrow are alternatives.
   Cash terms are a real cost.

4. **Lead time.** Confirm production days, ask about expedite options, and pin
   down the actual ship date in writing.

5. **Packaging.** Branded, custom box, polybag spec. negotiate inclusion in the
   unit price or as a separate cost. crucial for FBA prep compliance.

6. **Quality control.** Pre-shipment inspection, AQL level, third-party inspection
   service, sample retention. negotiate who pays.

7. **Tariff sharing.** For tariff-volatile categories, negotiate that price
   adjustments require evidence and a cap, not unilateral supplier price hikes.

## Step by step

1. **Collect inputs.** The product, current quote or expected starting numbers,
   the seller's target volume, the seller's leverage (volume, future orders, brand
   credibility).

2. **Set targets per lever.** What is the ideal and what is the walk-away on each.

3. **Sequence the asks.** Initial email focuses on price + MOQ. Round 2 covers
   payment terms and lead time. Round 3 covers packaging and QC. Tariff sharing
   appears late, when the relationship is warm.

4. **Write each email.** Professional, brief, dollar-specific. Each ask is its own
   email or its own paragraph.

5. **Plan the concession ladder.** Be willing to accept on lever 4-5 in exchange
   for lever 1-2. Never give all in one round.

6. **Document agreements.** Email confirmation of every term agreed. spoken
   agreements with overseas suppliers do not stick.

7. **Run the quality check**, then deliver.

## Output format

```
## Negotiation Plan. [supplier or product]

### Targets per lever
1. Unit price: target [$], walk-away [$]
2. MOQ: target [N], walk-away [N]
...

### Email sequence
Email 1 (price + MOQ): [template]
Email 2 (payment + lead time): [template]
Email 3 (packaging + QC): [template]
Email 4 (tariff sharing, if relevant): [template]

### Concession ladder
[what to give up on to get what]
```

## Worked example

A new supplier quoted 4.50 USD per unit, MOQ 3,000, 30/70 payment. Seller's target
volume is 500 units initial sample then 5,000. Negotiation plan: email 1 anchors
3.80 USD per unit with a 500-unit sample MOQ, and frame the 5,000 volume as the
future. Likely supplier counter: 4.10, MOQ 1,000. Seller accepts 4.10 but reasserts
500 sample MOQ. Email 2 negotiates payment terms (30% / 60% on shipment / 10% on
arrival quality confirmed). Email 3 negotiates branded packaging included at the
4.10 price, AQL 2.5 with the seller's chosen inspection service. By the end, the
seller has the price, MOQ flexibility, payment protection, and packaging compliance
in place, not just a price discount.

## Quality check

- Targets and walk-aways are set for every lever, not just price.
- The negotiation is sequenced over multiple emails, not one giant ask.
- Concessions are planned in advance. you trade lever 4 for lever 1.
- Every agreed term is documented in writing, not spoken.
- Tariff-sharing language is in writing for tariff-volatile categories.

## Common mistakes

- **Negotiating price only.** Leaving MOQ, payment, and packaging unnegotiated.
- **One giant email.** Asking for everything at once produces a flat 'no' or one
  small concession.
- **No walk-away.** Without a real walk-away, the supplier knows you will accept.
- **Spoken agreements.** Production for orders agreed by WeChat or call alone often
  diverges from what the seller thought was agreed.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
