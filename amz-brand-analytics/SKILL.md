---
name: amz-brand-analytics
description: >-
  Turn Amazon Brand Analytics reports into decisions. Reads Search Query
  Performance, Search Catalog Performance, Market Basket, Repeat Purchase, and
  Top Search Terms exports, and converts them into ranked actions. Use when a
  user pastes or describes Brand Analytics data, asks about Search Query
  Performance, SQP, market basket analysis, search frequency rank, click share,
  conversion share, repeat purchase behavior, or wants to know what their Brand
  Analytics is telling them. Trigger phrases: "brand analytics", "SQP", "search
  query performance", "market basket", "click share", "conversion share",
  "repeat purchase". Works with zero tools. the user pastes the report data.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Brand Analytics Interpreter

Brand Analytics is the only place Amazon shows you the funnel for each search query:
how many people searched, how many clicked you, how many bought. Most sellers open
it, feel overwhelmed, and close it. This skill turns each report into a short list
of ranked actions.

## When to use this

- The user pasted a Search Query Performance or Market Basket export.
- They ask what a Brand Analytics report means or what to do about it.
- They want to find where their listing leaks shoppers in the funnel.
- They want bundle or cross-sell ideas from real co-purchase data.

## The framework. The Query Funnel

Every search query is a three-stage funnel. Brand Analytics gives you all three
numbers. The stage where your share drops is the stage you fix.

| Stage | Brand Analytics metric | If your share is low here |
|-------|------------------------|---------------------------|
| Seen | Impression share | Visibility problem. rank or ads. |
| Clicked | Click share vs impression share | Listing entry problem. main image, title, price, rating. |
| Bought | Conversion share vs click share | Listing close problem. bullets, A+, reviews, price. |

The diagnosis rule: compare your share at each stage. If click share is far below
impression share, the main image or price loses the click. If conversion share is
far below click share, the listing body loses the sale. Never guess. the report says.

## The four buckets

Classify every important query into one bucket, then act:

- **Defend.** You dominate the query, including your own brand terms. Maintain. flag
  any branded query where competitors are stealing impression share.
- **Grow.** Strong click and conversion share but low impression share. The listing
  works. buy more visibility with ads and rank.
- **Fix.** Real impressions but click or conversion share collapses. A listing or
  image bottleneck. Do not spend ad money here until the leak is patched.
- **Ignore.** No meaningful share and not strategic. Do not waste attention.

## Step by step

1. **Identify the report.** Search Query Performance, Market Basket, Repeat Purchase,
   or Top Search Terms. Each answers a different question.

2. **For Search Query Performance:** sort queries by search volume. For each top
   query, compute the funnel. impression share, then click share, then conversion
   share. Diagnose the leaking stage. Assign a bucket.

3. **For Market Basket:** rank co-purchased products by attach rate. Classify each
   pair as a bundle candidate, a Sponsored Display target, a complement to mention
   in copy, or noise.

4. **For Repeat Purchase:** identify which products have real repeat rates. those are
   subscribe-and-save and retention candidates.

5. **Date check.** If the data is more than a quarter old, flag it at the top and
   recommend pulling a fresh export before acting on dollar figures.

6. **Rank the actions.** Produce the top 5 actions by estimated revenue impact, each
   with the query, the bucket, the specific fix, and a realistic dollar estimate.

7. **Run the quality check**, then deliver.

## Output format

```
## Brand Analytics Read. [report type]

Bottom line: [3 sentences. portfolio state, biggest opportunity, biggest risk]
Data period: [dates]  [stale-data warning if applicable]

### Query funnel
[query] . impr share [X]% . click share [Y]% . conv share [Z]% . leak: [stage] . bucket: [bucket]
...

### Top 5 actions this week
1. [query] . [bucket] . [specific fix] . est. impact [$]
...

### One hidden insight
[something most sellers would miss in this data]
```

## Worked example

Query "karaoke machine for kids", 40,000 monthly searches. Impression share 22
percent, click share 19 percent, conversion share 6 percent.

Diagnosis: click share tracks impression share, so the main image earns the click.
Conversion share is one third of click share. the listing loses the sale. Bucket:
Fix. Action: rebuild bullets and A+ for the kids buyer and add the missing proof,
before spending another dollar on ads for this query.

## Quality check

- Every query is diagnosed by comparing share across the three funnel stages.
- Every query has a bucket and a specific, not generic, fix.
- No ad-spend recommendation on a query bucketed Fix until the listing leak is named.
- Stale data, if any, is flagged at the top before any dollar figure.
- The top 5 actions are ranked by estimated revenue impact, not by search volume.
- Dollar estimates are marked as estimates.

## Common mistakes

- **Reading volume, not the funnel.** A huge query you convert at 2 percent is a trap.
- **Throwing ads at a Fix query.** Paying for clicks into a listing that cannot close
  is the fastest way to burn budget.
- **Ignoring branded queries.** Competitors bidding on your brand show up as lost
  impression share on your own name. that is a leak worth defending.
- **Acting on old data.** Brand Analytics exports age fast. dollar targets from a
  six-month-old report are fiction.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
