---
name: amz-listing-indexation-audit
description: >-
  Audits whether an ASIN is indexed for its top 30 target keywords on Amazon
  search. Builds a heatmap and diagnoses root cause per missing keyword.
  A listing can be live but invisible for 40% of its target terms, this finds
  the gap. Use when a user asks about indexation, why their ASIN does not show
  up, or organic ranking failure. Trigger phrases: "Amazon indexation check",
  "ASIN not ranking", "indexed keywords", "why isn't my listing showing up".
  Works with zero tools.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Listing Indexation Audit

A listing can be fully live, Buy Box won, plenty of inventory, and still not
indexed for 40% of its target keywords. Sellers throw PPC at it and wonder why
organic rank never climbs. The fix is not bidding, it is indexation. The most
common causes: a restricted term in backend search, a 250-byte truncation, a
brand-locked variant, or a prohibited claim quietly stripped by Amazon's
content filter. This audit produces a heatmap of indexed vs not indexed for
the top 30 keywords plus a root-cause diagnosis per gap.

## When to use this

- 60-90 days post-launch and organic rank refuses to move
- PPC for a keyword performs well but the ASIN never shows organically
- After a backend keyword edit, verifying nothing was silently stripped
- Pre-launch sanity check, confirming indexation before scaling PPC

## The framework. The Indexation Matrix

For each ASIN x target keyword pair, run a search on Amazon.com:
```
{ASIN} {keyword}
```

If the ASIN appears in results, INDEXED. If not, NOT INDEXED. If it appears
only with quoted phrase fragments, PARTIAL.

### Root cause diagnosis table

| Symptom | Likely root cause | Fix |
|---|---|---|
| Not indexed, term is in title | Brand-locked or prohibited claim | Review title, replace risky terms |
| Not indexed, term is in bullets | Bullet character limit or filter strip | Move to backend, simplify |
| Not indexed, term only in backend | 250-byte overflow or duplicate | Re-prioritize backend, dedupe |
| Partial (some variants only) | Variation parent indexation issue | Update parent-level keywords |
| Indexed but no rank movement | Indexed but irrelevant per A9/COSMO | Improve relevance signals in copy |

## Step by step

1. **Build the target keyword list.** Top 30 commercial-intent terms for the
   product. Pull from Helium 10 Cerebro, Brand Analytics top search terms, or
   the seller's known target list.

2. **Run the matrix.** For each keyword, search "{ASIN} {keyword}" on Amazon.
   Log INDEXED, NOT INDEXED, or PARTIAL.

3. **Build the heatmap.** Visual grid, green for indexed, yellow for partial,
   red for not indexed. Sort by search volume descending.

4. **Diagnose root causes.** For every red row, walk through the diagnosis
   table. Identify the most likely cause.

5. **Check backend search terms.** Edit > Keywords. Confirm under 250 bytes,
   no duplicate words across title and backend, no restricted terms.

6. **Check for prohibited claims.** Words like "FDA approved", "best", "cure",
   "kills bacteria" without certification, "organic" without USDA cert. These
   get silently stripped from indexation.

7. **Generate per-keyword fix list.** Specific, actionable. "Move 'antibacterial'
   to backend, remove 'kills 99% germs' from bullet 2".

8. **Run the quality check**, then submit edits.

## Output format

```
## Indexation Audit. [ASIN]

**Heatmap (top 30 keywords sorted by search volume)**
Keyword | SV | Status | Where it appears | Diagnosis
[rows]

Indexed: [N] of 30
Partial: [N] of 30
Not indexed: [N] of 30

**Backend health check**
- Byte count: [N] of 250
- Duplicates with title: [list]
- Restricted terms detected: [list or "none"]

**Fix list (ranked by SV impact)**
1. [Specific edit] - unlocks [keyword] - SV [N]
2. [...]
```

## Worked example

ASIN: B0F4XYZ123, sleep mask, 30 target keywords. Matrix run results:
indexed 19, partial 3, not indexed 8.

Not indexed analysis:
- "blackout sleep mask" (SV 14,800): in title but missing. Diagnosis: title is
  187 chars, Amazon truncated. Fix: shorten title to 145 chars, prioritize this
  term in first 80 chars.
- "anti aging eye mask" (SV 5,400): in bullet 4. Diagnosis: bullet has "FDA
  approved" claim, full bullet got filtered. Fix: remove FDA claim.
- "silk sleeping mask" (SV 9,100): not in any field. Diagnosis: missing.
  Fix: add to backend search terms (uses 18 bytes).
- 5 more similar.

Backend health: 287 bytes (over limit by 37, last 4 keywords are not indexed),
3 duplicates with title wasting 22 bytes. Cleanup recovers 59 bytes for new
terms.

Fix list ranked by SV impact: 8 specific edits, total SV unlock = 67,000
monthly searches. Projected organic impression lift: 35-50% within 14 days
of edit.

## Quality check

- Search performed on amazon.com logged out or in incognito (personalization off)
- Search includes the ASIN to force-find regardless of rank
- Backend byte count measured in UTF-8 bytes, not characters
- Restricted terms checked against current 2026 prohibited claims list
- Variation parent and child both checked if listing is varied

## Common mistakes

- **Searching by keyword only.** Without ASIN you cannot tell if the listing is
  indexed but just ranked low.
- **Using character count for backend.** Amazon uses bytes. Non-ASCII chars
  count as 2-4 bytes.
- **Duplicating title words in backend.** Wastes the 250 bytes, no ranking benefit.
- **Ignoring partial status.** Partial means a variation issue, easy to miss.
- **Not re-auditing after edits.** Index updates take 24-72 hours. Re-run the
  matrix to confirm fix took effect.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
