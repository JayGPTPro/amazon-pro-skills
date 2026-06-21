---
name: amz-search-term-report-miner
description: >-
  Parses Amazon Search Term Reports (50K+ rows) into 4 actionable buckets:
  negative exacts, negative phrases, exact-match harvest, and hero scale terms.
  Produces a Bulk Operations upload-ready file in minutes instead of the eyeball
  approach that misses 60% of opportunities. Use when a user mentions STR, PPC
  bulksheet, or search term analysis. Trigger phrases: "search term report",
  "STR analysis", "PPC bulksheet", "negative keywords bulk upload", "harvest
  exact match". Works with zero tools.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Search Term Report Miner

A Search Term Report from a mature account is 50,000+ rows. Sellers download it,
open Excel, scroll for 20 minutes, find 4 negatives, give up. Meanwhile real
money leaks: terms with 30+ clicks and 0 orders, exact-match converters stuck
in broad campaigns, and dead clusters that drain $200/day. This skill carves
the file into 4 surgical buckets and outputs a Bulk Operations upload ready to
submit.

## When to use this

- Monthly PPC review and you want a clean negative sweep
- Account spending $3K+/month on PPC with ACoS drift
- New product 60 days post-launch ready for the first harvest pass
- Pre-Q4 cleanup. Push wasted spend out before peak

## The framework. The Four Buckets

Pull the Search Term Report (60-day window). For every search term, route to
exactly one bucket based on click and order thresholds.

| Bucket | Filter | Action |
|---|---|---|
| 1. Negative Exact | Clicks >= 10, Orders = 0, ACoS = blank | Add as Negative Exact at campaign |
| 2. Negative Phrase | 3+ terms share root, combined clicks >= 25, orders <= 1 | Add root as Negative Phrase |
| 3. Exact Harvest | Orders >= 2, ACoS < target ACoS, term not already exact | Move to new exact-match campaign |
| 4. Hero Scale | Impressions >= 1000, CVR well above your account average, ACoS < target | Increase budget + bid +20% |

Anything else: leave alone.

A note on the Hero gate: there is no universal "good" CVR. It varies hugely by
category, price, and product. Do not hardcode a fixed number like 12%. Instead,
compare each term to YOUR account or category baseline. A practical hero gate is
roughly 1.5x to 2x your average CVR for that product. Compute your baseline
first, then set the gate from it.

## Step by step

1. **Download the STR.** Advertising > Reports > Sponsored Products > Search Term
   Report. Date range: last 60 days. Format: CSV.

2. **Set the target ACoS.** Usually 25-35% depending on margin. This is the
   threshold for bucket 3 and 4.

3. **Apply Bucket 1 filter.** Clicks >= 10 AND Orders = 0. Export the search
   term column. Format as Negative Exact rows for Bulk Operations.

4. **Cluster for Bucket 2.** Group remaining 0-1 order terms by shared 2-word
   root. If a root cluster has 25+ combined clicks, add the root as Negative
   Phrase.

5. **Apply Bucket 3 filter.** Orders >= 2 AND ACoS < target. Check each term is
   not already an exact keyword in any campaign. Format as new exact-match
   campaign rows.

6. **Apply Bucket 4 filter.** Impressions >= 1000 AND CVR well above your
   account average (roughly 1.5-2x your baseline for that product) AND ACoS <
   target. These are scale candidates. Generate bid +20% rows.

7. **Build the Bulk Operations file.** 4 sheets, one per bucket. Use Amazon
   Bulk Sheet template columns.

8. **Run the quality check**, then upload to Campaign Manager.

## Output format

```
## STR Mining Output. [Account] [date range]

**Summary**
- Total search terms analyzed: [N]
- Bucket 1 (Negative Exact): [N] terms, wasted spend last 60d: $[X]
- Bucket 2 (Negative Phrase): [N] roots
- Bucket 3 (Exact Harvest): [N] terms, projected exact-match orders/month: [N]
- Bucket 4 (Hero Scale): [N] terms

**Bulk Operations file structure**
Sheet 1: Negative Exacts
Campaign | Ad Group | Negative Keyword | Match Type
[rows]

Sheet 2: Negative Phrases
[rows]

Sheet 3: Exact Match Harvest. New campaigns
Campaign | Ad Group | Keyword | Match Type | Bid
[rows]

Sheet 4: Hero Scale. Bid increases
Campaign | Ad Group | Keyword | Old Bid | New Bid
[rows]
```

## Worked example (illustrative)

The figures below are an example to show how the buckets shake out, not a
benchmark to expect. Your term counts, CVR, ROAS, and savings depend entirely
on your account.

Account: home goods seller, 42 SKUs, $8,400/month PPC spend. 60-day STR has
38,200 unique search terms. After parsing:

Bucket 1: 184 negative exact candidates. Wasted spend = $1,847 over 60 days,
or $924/month immediately saved.

Bucket 2: 12 phrase roots like "cat", "for dogs", "wholesale". 412 clicks, 8
orders. Adding negative phrases blocks 200+ wasted clicks/month.

Bucket 3: 67 exact-match harvest candidates. In this example the harvested
terms convert well above the account average and move to exact campaigns at
1.2x bid. The incremental-orders and ROAS figures you would model here are
account-specific. do not assume a fixed order count or a particular ROAS. run
the projection off your own term-level CVR and AOV.

Bucket 4: 14 hero terms. +20% bid aims to move them from mid page 1 toward the
top of search.

Total projected impact in this scenario combines the negative-keyword savings
with the harvested-term upside. Both are illustrative. compute your own numbers
from your account data rather than carrying these over.

## Quality check

- Date range is 60 days, not 30 (need volume for cluster math)
- Target ACoS set before bucketing, not after
- Bucket 3 harvest terms confirmed not already exact in any campaign
- Negative phrases checked for accidental brand cannibalization
- Bulk file uses correct column headers per Amazon template

## Common mistakes

- **30-day STR.** Not enough volume per term. Bucket 2 cluster math breaks down.
- **No target ACoS.** Bucket 3 and 4 lose their gate, you scale unprofitable terms.
- **Adding negative phrases without checking brand terms.** Easy to accidentally negative-match your own brand variant.
- **Harvesting terms that already exist as exact.** Creates internal bid wars.
- **Skipping Bucket 4.** Most sellers focus on cutting waste and miss the scale upside, which is often the larger lever.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
