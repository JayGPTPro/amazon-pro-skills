---
name: amz-review-analyzer
description: >-
  Mine Amazon reviews for product, listing, and marketing intelligence. Extracts
  recurring complaints, feature requests, the words customers use, and the
  reasons they chose the product, then turns them into listing fixes, product
  improvements, and copy. Use when a user pastes reviews and asks to analyze
  them, find complaint patterns, mine reviews, understand customer sentiment,
  pull insights from competitor reviews, or turn reviews into improvements.
  Trigger phrases: "analyze reviews", "review analysis", "complaint patterns",
  "what customers say", "mine reviews", "competitor reviews". Works with zero
  tools. the user pastes the reviews.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Review Analyzer

Reviews are the cheapest market research on Amazon and the most ignored. They contain
the product roadmap, the listing fixes, and the exact words that convert. This skill
mines a set of reviews and turns them into action, on your product or a competitor's.

## When to use this

- A seller wants to know what to fix on their product or listing.
- Analyzing competitor reviews to find openings (see amz-competitor-analysis).
- A product has mixed ratings and the seller needs the pattern, not anecdotes.
- Writing or rewriting copy and needing the customer's own language.

## The framework. The Four Extractions

Read every review for four things. Each feeds a different decision.

### 1. Complaints (the negative reviews)

Sort the 1 to 3 star reviews into recurring themes. A complaint that appears once is
noise. A complaint that appears repeatedly is a root cause. Rank themes by frequency
and by severity (a safety or defect complaint outranks a cosmetic one).

- On your product, the top complaints are the product and listing roadmap.
- On a competitor, the top complaints are your openings. the things to do better.

### 2. Feature requests

Buyers say what they wish the product did. "I wish it came with a lid", "it would be
perfect if it were taller". These are the next version, the bundle idea, or the
variation to add.

### 3. The chosen-for reasons (the positive reviews)

The 4 to 5 star reviews say why people are glad they bought. These are the real
selling points, validated by customers. They belong at the top of the bullets and in
the A+ Content, because they are proven to matter.

### 4. The customer's language

The exact phrases buyers use. Not your words, theirs. These phrases are keyword
candidates and the most converting copy you can write, because they mirror how the
buyer already thinks and searches.

## Step by step

1. **Collect inputs.** The pasted reviews, whether they are the seller's product or a
   competitor's, and the product.

2. **Run the four extractions.** Complaints, feature requests, chosen-for reasons,
   and customer language.

3. **Rank the complaints** by frequency and severity. Separate recurring root causes
   from one-off noise.

4. **Translate to action.**
   - Own-product complaints become listing fixes and product improvements.
   - Competitor complaints become positioning openings.
   - Feature requests become roadmap, bundle, or variation ideas.
   - Chosen-for reasons become bullet-one and A+ material.
   - Customer language becomes keyword and copy candidates.

5. **Prioritize.** The top 3 actions by impact: usually fix the most frequent severe
   complaint, amplify the strongest chosen-for reason, and exploit the biggest
   competitor opening.

6. **Run the quality check**, then deliver.

## Output format

```
## Review Analysis. [product] . [own / competitor]

### Recurring complaints (ranked)
[theme] . frequency . severity . [the fix or the opening]
...

### Feature requests
[request] . [roadmap / bundle / variation idea]

### Why customers chose it
[reason] . [use in bullet 1 / A+]

### Customer language to use
[phrases] . [keyword / copy candidate]

### Top 3 actions
1. ...
```

## Worked example

A user pastes reviews of their own kitchen scale.

Complaints: the most frequent is "turns off too fast while I am still measuring", a
recurring usability theme. Defects are rare. Feature requests: several buyers wish it
had a larger weighing platform. Chosen-for: buyers repeatedly praise the accuracy for
baking. Customer language: "accurate to the gram", "great for sourdough".

Actions: fix or document the auto-off issue, it is the top complaint and is fixable
with a setting note in the listing and a firmware or model change later. Lead bullet
one on "accurate to the gram for baking", the validated selling point. Consider a
larger-platform version, a real feature request. Add "for sourdough" to the keyword
set, it is the buyer's own language.

## Quality check

- All four extractions are run. complaints, requests, chosen-for, and language.
- Complaints are ranked by frequency and severity, with one-offs separated as noise.
- Every extraction is translated into a specific action.
- Competitor reviews are read as openings. own reviews as a fix list.
- Chosen-for reasons are routed to bullet one and A+ Content.
- The top 3 actions are prioritized by impact.

## Common mistakes

- **Reading anecdotes, not patterns.** Reacting to one dramatic review instead of the
  recurring theme.
- **Only reading the negative.** The 5-star reviews hold the validated selling points.
- **Ignoring customer language.** Rewriting copy in the seller's words when the
  customer's words convert better and are real keywords.
- **No prioritization.** A flat list of 20 findings with no decision about any.
- **Skipping competitor reviews.** The cheapest source of openings on Amazon, unused.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
