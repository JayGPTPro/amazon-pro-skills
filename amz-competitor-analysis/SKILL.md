---
name: amz-competitor-analysis
description: >-
  Run a full competitor analysis for an Amazon product. Compares listings,
  pricing, images, reviews, ratings, and ad presence against direct competitors,
  finds the weaknesses to exploit and the strengths to neutralize, and outputs a
  prioritized attack plan. Use when a user asks to analyze competitors, compare
  their listing to a rival, find a competitor's weak spots, understand why a
  competitor outranks them, or plan how to beat a specific ASIN. Trigger phrases:
  "competitor analysis", "analyze my competition", "beat this competitor",
  "why is this ASIN ranking", "compare my listing". Works with zero tools. the
  user pastes competitor listing details and reviews.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Competitor Analysis

Most competitor analysis is a feature comparison table that leads nowhere. Real
competitor analysis ends with a plan: where to attack, what to defend, and what to
ignore. This skill produces that plan.

## When to use this

- Planning a launch into a category and sizing up the incumbents.
- A specific competitor outranks the user and they need to know why.
- A listing has stalled and the competitive set has moved.
- Choosing where to invest. copy, images, price, or ads.

## The framework. The Gap Map

Score the user's product and each competitor on the five things a buyer actually
weighs. The pattern of gaps tells you where to attack and where to defend.

| Battlefront | What the buyer sees | Win condition |
|-------------|---------------------|---------------|
| First impression | Main image, price, rating, review count | Earns the click from the search page |
| The promise | Title and bullets | States a sharper benefit than rivals |
| The proof | Images, A+, video, review themes | Answers objections rivals leave open |
| Social proof | Rating value and review volume | Credible enough to not lose on trust |
| Visibility | Keyword coverage, ad presence | Appears where rivals appear |

For each battlefront, mark the user as Ahead, Even, or Behind versus the set.

- **Behind** on a high-weight battlefront is a **fix-first priority**.
- **Ahead** is a **defend**: protect it and lean on it in copy.
- A front where a competitor is **Behind** is an **opening**: exploit it.

## Step by step

1. **Collect inputs.** The user's product and listing, and for 2 to 5 direct
   competitors: price, main image description, title, bullets, rating, review count,
   review themes, and whether they run ads. Ask the user to paste what they have.

2. **Score the Gap Map.** Rate the user Ahead, Even, or Behind on each of the five
   battlefronts versus the set.

3. **Mine competitor reviews.** The 1 to 3 star reviews of competitors are the gift.
   recurring complaints are the openings. Pull the top 3 complaint themes per
   competitor.

4. **Find the openings.** Cross the Gap Map with the review complaints. An opening is
   where competitors are weak and buyers care.

5. **Find your exposure.** List the fronts where the user is Behind on a
   high-weight battlefront. These are fix-first.

6. **Build the plan.** Three lists: Fix (your exposure), Exploit (their openings),
   Defend (your strengths). Rank by revenue impact.

7. **Run the quality check**, then deliver.

## Output format

```
## Competitor Analysis. [product]

Competitive set: [competitors]

### Gap Map
[battlefront] . you: [ahead/even/behind] . notes
...

### Competitor weaknesses (from reviews)
[competitor] . top complaints: ...

### The plan
Fix first (your exposure): ...
Exploit (their openings): ...
Defend (your strengths): ...

### Top 3 moves this month
1. ...
```

## Worked example

A user sells a yoga mat at 40 USD. Three competitors at 25 to 35 USD.

Gap Map: first impression Behind, the main image is studio-empty while rivals show
the mat in use. Proof Even. Social proof Behind, 200 reviews versus 2,000-plus.
Competitor reviews complain repeatedly that the cheaper mats are slippery when sweaty.

Plan: Fix the main image first, it is losing the click. Exploit the slip complaint,
the listing should lead on grip with proof. Defend nothing yet, there is no clear
lead. Social proof gap is real but slow, so it is a review-generation track, not a
this-week move.

## Quality check

- Every battlefront is scored Ahead, Even, or Behind, not described vaguely.
- Competitor 1 to 3 star reviews were mined for openings. not just their copy.
- The plan separates Fix, Exploit, and Defend. it is not one undifferentiated list.
- Fix-first items are genuine high-weight exposures, not cosmetic.
- The top 3 moves are ranked by revenue impact.

## Common mistakes

- **A table with no plan.** Comparing 30 attributes and recommending nothing.
- **Ignoring competitor reviews.** Their 1-star reviews are the cheapest market
  research on Amazon and most analyses skip them.
- **Attacking where you are already ahead.** Polishing a strength while an exposure
  bleeds sales.
- **Copying the leader.** Matching the top competitor feature for feature gives the
  buyer no reason to switch. find the opening they left.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
