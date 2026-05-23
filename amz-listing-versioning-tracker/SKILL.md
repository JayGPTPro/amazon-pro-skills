---
name: amz-listing-versioning-tracker
description: >-
  Log every Amazon listing change (title, bullets, image, A+, price) with date
  and impact on sessions and conversion. Lets the seller roll back regressions
  with evidence. Use when a user asks about tracking listing changes, A/B
  testing, change log, before-and-after, or rolling back a listing change.
  Trigger phrases: "listing changes", "change log", "before after", "A/B test",
  "rollback", "version history". Works with zero tools.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Listing Versioning Tracker

Sellers blindly change listings and lose rank without knowing the cause. This skill
establishes a change log so every edit is dated, the impact is measured, and
regressions are caught and reverted with evidence.

## When to use this

- A listing's performance changed and the seller cannot remember what was last
  edited.
- About to make a significant rewrite and want to measure impact properly.
- Multiple people touch the listing and changes are not coordinated.
- Setting up Manage Your Experiments and want a tracking layer.

## The framework. The Change Log

Every change is one row in a log. Six fields per row.

1. **Date** of the change.
2. **What changed** (specifically. "main image" or "bullet 3" or "price").
3. **Why** (the hypothesis: "test scrollable hook").
4. **Before** value.
5. **After** value.
6. **Impact** (sessions and conversion 14 days after the change).

Run the log per ASIN. one row per change, never bulk.

## Step by step

1. **Set up the log.** A simple spreadsheet, a Notion table, or paste into this
   skill each time. one row per change.

2. **Before any change:** record current state. sessions/day (trailing 14d),
   conversion rate (trailing 14d), Buy Box %, price.

3. **Make exactly one change.** Multiple changes at once make impact unattributable.

4. **Wait 14 days.** Then read the post-change sessions and conversion.

5. **Compare.** Is the change positive, neutral, or negative?

6. **Decide.** Positive: keep. Neutral: keep or revert based on cost. Negative:
   revert and document why.

7. **Build the pattern view.** After 6-12 changes, patterns emerge. certain types
   of changes consistently help or hurt. that knowledge compounds.

8. **Run the quality check**, then deliver.

## Output format

```
## Change Log. [ASIN]

### Latest change
Date: [date]
What: [specifically]
Why: [hypothesis]
Before: [value]
After: [value]
Impact (14d post): sessions [delta], conv rate [delta], BB% [delta]
Verdict: [keep / neutral / revert]

### Patterns observed
[recurring lessons across multiple changes]
```

## Worked example

ASIN at 80 sessions/day, 14% conversion. Change date 2026-03-12: main image updated
to add a usage scene. Hypothesis: a real-use scene lifts the click. Before main was
a clean studio shot. 14 days later: sessions 92/day (+15%), conversion 11.5%
(-2.5pp). Verdict: mixed. Sessions are up because more clicks, but conversion is
down because the new image set an expectation the rest of the gallery did not
match. Action: revert the main image and instead update gallery frame 2 to add the
scene without changing the main. The log makes the decision evidence-based instead
of a hunch.

## Quality check

- One change per row. multiple simultaneous changes make impact unattributable.
- Before-state is captured before the change, not estimated after.
- A 14-day window is used. shorter windows are noise.
- The verdict is based on both sessions and conversion, not one in isolation.
- Patterns across multiple changes are recorded and used for future decisions.

## Common mistakes

- **Bulk changes.** Rewriting bullets, swapping images, and changing price at once.
  No one knows which moved the needle.
- **Looking too soon.** Reading impact after 3 days. noise.
- **No before-state.** Trying to remember the previous bullets is unreliable.
- **Single metric.** A sessions lift can hide a conversion loss. read both.
- **No rollback.** A change that hurt is left in place because the seller did not
  notice.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
