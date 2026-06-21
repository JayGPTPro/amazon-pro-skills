---
name: amz-category-renoding-fix
description: >-
  Detect and fix silent Amazon category re-noding. When Amazon quietly moves
  listings to incorrect browse-tree nodes, sales drop sharply because the
  listing now ranks against the wrong queries. This skill audits the nodes,
  identifies the wrong placements, and writes the browse-node correction case
  for Seller Central. Use when a user notices a sudden sales drop with flat ad spend, a
  listing in the wrong browse category, or wonders why their product is not
  showing up for the right keywords. Trigger phrases: "category", "browse node",
  "wrong category", "re-noded", "sales dropped no reason", "browse tree". Works
  with zero tools.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Category Re-Noding Fix

Amazon periodically re-organizes the browse tree and silently moves products to new
nodes. A listing moved to the wrong node loses 30-70 percent of its organic search
visibility overnight, because Amazon scores it against the wrong query set. This
skill finds the wrong placement and writes the correction case.

## When to use this

- Sales dropped sharply on a listing without a known cause.
- A listing should rank for a category but does not appear in its filters.
- Recently received a notification that a product was re-categorized.
- Routine quarterly browse-tree audit.

## The framework. The Node Audit

Four questions to confirm a re-noding issue.

1. **What node is the listing actually in now?** Look at the breadcrumb on the
   listing's own detail page and the category in Manage Inventory.

2. **What node should it be in?** The most logical browse path a customer would use
   to find the product, plus what comparable competitors are in.

3. **Is the difference material?** Some re-nodings are cosmetic. Others move the
   product out of the queries that drive its sales.

4. **What does the data show?** Sessions and conversion before and after the
   suspected re-noding date.

If the node is wrong and the data shows the drop, file the correction.

## Step by step

1. **Collect inputs.** The ASIN, the current breadcrumb / browse node ID, the
   expected node, recent sessions and sales trend, and the date of the suspected
   change.

2. **Confirm the change.** Compare the current node against the expected. Verify
   the drop in sessions or conversion ties to a specific date.

3. **Find the correct browse node.** Use Amazon's browse tree (BTG) or look at
   where comparable products sit.

4. **Write the catalog correction case.** Subject: "Browse-node correction needed
   for [ASIN]". Body: current node, requested node, business reason, before/after
   data.

5. **Submit through the right path.** First try the self-serve fix: edit the
   listing's recommended browse node / item type, using the Browse Tree Guide to
   pick the correct node, either on the listing directly or via the Category
   Listings Report. If the self-serve edit does not stick, open a case. Brand
   Registered sellers file through Brand Registry > Manage Your Case. everyone
   else uses Seller Central > Help > Get Support > Catalog category. Attach a
   screenshot of the wrong placement and reference the correct browse node ID.

6. **Track resolution.** Re-noding corrections take 5-15 business days. Watch the
   listing's breadcrumb and the session recovery.

7. **Run the quality check**, then deliver.

## Output format

```
## Category Re-Noding Fix. [ASIN]

Current node: [breadcrumb / node ID]
Should be: [breadcrumb / node ID]
Suspected change date: [date]

### Impact
Sessions before: [n/day]   After: [n/day]   Drop: [%]

### Case to file
Subject: Browse Tree Guide correction for [ASIN]
Body:
- Current placement: ...
- Requested placement: ...
- Business reason: ...
- Data attached: sessions and conversion before/after the change

### Submission path
1. Self-serve: edit recommended browse node / item type via the listing or
   Category Listings Report, using the Browse Tree Guide
2. If that fails: Brand Registry case (if enrolled) or Seller Central > Catalog
   support case
```

## Worked example

A kitchen-tool ASIN suddenly drops from 80 sessions a day to 22, ad spend flat.
Investigation: the breadcrumb shows the product was moved from "Kitchen and Dining
> Cookware and Bakeware > Specific subcategory" to a generic "Home and Kitchen"
parent node a week ago. Comparable competitor products sit in the original
subcategory. Case filed with sessions data attached. Corrected within 8 days,
sessions recover to baseline.

## Quality check

- The current and expected nodes are documented, not described vaguely.
- The drop is tied to a specific date by data, not assumed.
- The expected node is justified by comparable competitor placement.
- The fix is attempted self-serve first (listing / Category Listings Report via the Browse Tree Guide), then escalated to the right case channel (Brand Registry or Catalog support) if needed.
- Resolution is tracked to confirm recovery.

## Common mistakes

- **Blaming the listing.** Spending days rewriting bullets while the issue is a
  browse-node move.
- **No before/after data.** A correction case without sessions data is dismissed.
- **Wrong submission path.** Filing under generic support instead of the Brand
  Registry case path or the Catalog category in Seller Central.
- **One-off thinking.** Amazon re-nodes multiple SKUs in one wave. check the whole
  catalog when one is found.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
