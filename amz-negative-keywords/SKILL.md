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

This is the deep-dive on the negative-keyword decision. Building the campaign
structure that produces these search terms (auto, broad, exact funnel) lives in
amz-ppc-campaign.

## When to use this

- A campaign spends on search terms that clearly do not match the product.
- ACoS is high and the search term report is full of junk terms.
- An auto or broad campaign is bringing irrelevant traffic.
- A seller wants a repeatable rule for what to negate, run on a schedule.

## The framework. The Search Term Sieve

Pour every term in the report through the sieve. It sorts each one into exactly one
of four outcomes, and only two of them fall into the negative bucket. Run the checks
in order. the first one a term matches is its verdict.

| # | Gate | Term pattern | Verdict |
|---|------|--------------|---------|
| 1 | Drain | Spend past the cost-of-a-sale threshold with zero or near-zero sales | Negate. money drain |
| 2 | Irrelevant | Clicks but clearly wrong item or wrong intent for the product | Negate. it will never convert |
| 3 | Winner | Converting at acceptable ACoS | Keep, and graduate it to an exact-match keyword |
| 4 | Noise | Too few clicks to judge either way | Wait. do not negate on noise |

Order matters: check Noise last, so a term is only ever sent to Wait when it has not
already earned a Negate or a Keep. The drain threshold for gate 1: a term that has
spent more than the cost of one sale (roughly 1 to 1.5 times your target cost per
acquisition) with no sale is a drain. Below that, it is still data collection.

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

- "plastic dog bowl" spent 14 USD, zero sales. Gate 1, drain, and gate 2, wrong
  material. Negate it. The token "plastic" is a whole irrelevant theme, so a phrase
  negative on "plastic" would be efficient if it is safe. Run the safety check: scan
  every converting term for the word "plastic". The winners here are "dog water bowl"
  and "stainless steel bowl", and neither contains "plastic", so the phrase negative
  cannot block a converter. Verdict: add "plastic" as a negative phrase. It also kills
  any future "plastic feeding bowl" or "plastic pet dish" before they spend.
  (Had a converting term contained "plastic", the rule flips: drop the phrase and
  negate "plastic dog bowl" as negative exact only.)
- "dog water bowl" converting at 4 USD per sale. Gate 3, winner. Keep and graduate to
  an exact-match keyword.
- "bowl" with 2 clicks, no data. Gate 4, noise. Wait.

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

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
