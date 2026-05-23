---
name: amz-negative-keywords
description: >-
  Find and manage Amazon PPC negative keywords to cut wasted ad spend without
  blocking converting traffic. Reads a search term report, flags the terms
  draining budget, decides negative-exact versus negative-phrase, and protects
  valuable terms from being blocked by accident. Use when a user asks about
  negative keywords, wasted ad spend, search term reports, irrelevant clicks,
  high-ACoS terms, or cleaning up a PPC campaign. Trigger phrases: "negative
  keywords", "wasted ad spend", "search term report", "irrelevant clicks",
  "high ACoS terms", "clean up campaign". Works with zero tools. the user pastes
  the search term report.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Negative Keyword Manager

Every PPC account leaks money on search terms that click and never buy. Negative
keywords stop the leak. But a careless negative also blocks a term that converts.
This skill cuts the waste without cutting a winner.

## When to use this

- A campaign spends on search terms that clearly do not match the product.
- ACoS is high and the search term report is full of junk terms.
- An auto or broad campaign is bringing irrelevant traffic.
- A seller wants a repeatable rule for what to negate, run on a schedule.

## The framework. The Negative Decision

Every search term in the report is one of four things. Only two of them become
negatives.

| Term pattern | Verdict |
|--------------|---------|
| Spend with zero or near-zero sales, past the cost-of-a-sale threshold | Negate. money drain |
| Clicks but irrelevant to the product (wrong item, wrong intent) | Negate. it will never convert |
| Converting at acceptable ACoS | Keep. and graduate it to an exact-match keyword |
| Too few clicks to judge | Wait. do not negate on noise |

The drain threshold: a term that has spent more than the cost of one sale (roughly
1 to 1.5 times your target cost per acquisition) with no sale is a drain. Below that,
it is still data collection.

## Exact versus phrase negatives

- **Negative exact.** Blocks only that precise term. Use it for a specific drain term
  that you want gone while keeping close variations live.
- **Negative phrase.** Blocks any search term containing that phrase. Use it for a
  whole irrelevant theme (a wrong-product word, a wrong-audience word).
- The danger: a broad negative phrase can silently block converting terms that happen
  to contain the phrase. Before adding a negative phrase, scan the report for any
  converting term that contains it. If one exists, use negative exact instead.

## Step by step

1. **Collect inputs.** The search term report with spend, clicks, orders, and sales
   per term, the product, and the target ACoS or cost per acquisition.

2. **Compute the drain threshold** from the target cost per acquisition.

3. **Classify every term** into the four buckets.

4. **Protect the winners.** List every converting term. Before any negative phrase is
   added, confirm it would not block one of these.

5. **Choose negative type per term.** Exact for a single drain term, phrase for a
   whole irrelevant theme that is safe to block.

6. **Graduate the winners.** Converting search terms found in auto or broad campaigns
   should be added as exact-match keywords in a harvest campaign, not just left.

7. **Set a cadence.** Negative keyword work is recurring. recommend a weekly or
   biweekly pass.

8. **Run the quality check**, then deliver.

## Output format

```
## Negative Keyword Plan. [campaign]

Drain threshold: spend over [$] with no sale

### Negatives to add
[term] . [negative exact / phrase] . reason . spend wasted [$]
...

### Protected (do not block)
[converting terms that a phrase negative could catch]

### Graduate to exact-match keywords
[converting search terms to promote]

### Cadence
Re-run this pass: [weekly / biweekly]
```

## Worked example

A search term report for a stainless steel dog bowl. Target cost per acquisition 6 USD.

- "plastic dog bowl" spent 14 USD, zero sales. Negate. wrong material, will never
  convert. Negative phrase "plastic" is tempting, but the report has "stainless steel
  bowl" converting and a phrase negative on a single word is risky here, so negate
  "plastic dog bowl" as exact plus "plastic" as phrase only after confirming no
  converting term contains it.
- "dog water bowl" converting at 4 USD per sale. Keep and graduate to an exact-match
  keyword.
- "bowl" with 2 clicks, no data. Wait.

## Quality check

- The drain threshold is computed from the target cost per acquisition, not guessed.
- Every term is classified into one of the four buckets.
- No negative phrase is added without scanning for converting terms it would block.
- Converting search terms are graduated to exact-match keywords, not just kept.
- Low-click terms are left alone, not negated on noise.
- A recurring cadence is set.

## Common mistakes

- **Negating on noise.** Blocking a term with 3 clicks and no sale. that is not data.
- **Broad phrase negatives.** Adding a negative phrase that quietly kills converting
  terms containing the same word.
- **Negating winners.** A high-ACoS term that still converts may be worth keeping at
  a lower bid, not negating.
- **Find and forget.** Running the pass once. new junk terms appear every week.
- **Not graduating.** Negating the junk but never promoting the converting discoveries.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. 50 production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
