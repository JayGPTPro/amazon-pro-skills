---
name: amz-aeo-external-content-plan
description: >-
  Plan external (off-Amazon) content that Amazon's AI assistants (Rufus, Alexa+)
  cite when a shopper asks a question. Covers Reddit answers, Quora, YouTube
  reviews, blog posts, and topic clusters that surface the brand above its own
  listing. Use when a user asks about AEO (Answer Engine Optimization), getting
  cited by Rufus, external SEO for Amazon, off-Amazon content strategy, or
  appearing in the "Researched by AI" section. Trigger phrases: "AEO", "answer
  engine", "external content for Amazon", "Rufus citations", "off-Amazon SEO",
  "researched by AI". Works with zero tools.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# External Content Plan for AI Search (AEO)

Amazon's AI assistants now cite external sources (Reddit threads, YouTube reviews,
blog posts, Quora) in the "Researched by AI" section. A brand mentioned in that
section often shows up before its own listing. This skill plans the external
content that earns those citations.

## When to use this

- The brand is invisible in Rufus/Alexa+ recommendations.
- Competitors keep getting cited in the "Researched by AI" panel.
- A new product needs more than a listing. it needs the external trust signals.
- The seller has been doing only on-Amazon work and the AI ignores the brand.

## The framework. The Topic Cluster Plan

The AI cites sources that answer specific buyer questions. Build clusters of content
around the questions, not random posts.

For each cluster:

1. **The seed question.** A real query a shopper asks, often longer than a keyword.
2. **The pillar.** One in-depth piece on the seller's site, blog, or YouTube
   channel that answers the question fully.
3. **The supporting posts.** 3-5 satellite posts: Reddit answers in relevant
   subreddits, Quora answers, comparison pieces, YouTube videos.
4. **The brand mention.** Each piece naturally mentions the seller's brand or
   product as the example or recommendation.

## Where the AI looks

In rough order of citation frequency:

- **Reddit threads** in product-specific subreddits.
- **YouTube reviews** with the seller's product on camera.
- **Independent blog posts** on category-specific sites.
- **Quora answers** to the seed question.
- **Forum posts** (specialty communities for the niche).

## Step by step

1. **Collect inputs.** Brand, products, the top 5-8 buyer questions (from
   `amz-ai-search-optimization` or fresh), current external presence.

2. **Pick the topic clusters.** Each cluster anchored on one seed question.

3. **Plan the pillar per cluster.** Format (long blog post, YouTube video, in-depth
   Reddit answer), platform, and the angle.

4. **Plan the supporting posts.** Specific subreddits, YouTube creators to
   approach, Quora questions to answer.

5. **Set the brand mention pattern.** Naturally placed, not promotional. The AI
   penalizes obvious self-promotion.

6. **Sequence the publish plan.** Pillar first, then supporting posts over 4-8
   weeks to build the citation density.

7. **Track citations.** Periodically ask Rufus/Alexa+ the seed question. Note if
   the brand or product is cited.

8. **Run the quality check**, then deliver.

## Output format

```
## External Content Plan. [brand]

### Topic clusters
Cluster 1. Seed question: [question]
  Pillar: [format] on [platform] . angle: [the take]
  Supporting:
   - Reddit answer in r/[subreddit]
   - YouTube: pitch [creator] for [video angle]
   - Quora: answer [question URL]
  Brand mention pattern: [natural placement]

Cluster 2. ...

### Publish sequence
[week-by-week order]

### Citation tracking
[seed questions to test in Rufus/Alexa+ monthly]
```

## Worked example

A meditation cushion brand. Seed question: "What is the best cushion for back pain
during meditation?". Pillar: a 2,500-word blog post on the brand's site comparing
cushion shapes for back pain. Supporting: an answer in r/meditation, a YouTube
collaboration with a yoga teacher, a Quora answer on the exact question. Each
naturally mentions the seller's specific cushion as the recommendation for the
back-pain use case. After 6 weeks the AI starts citing the blog post and the
Reddit answer when shoppers ask the seed question, and the brand appears above
the listing in the AI recommendation.

## Quality check

- Each cluster anchors on one specific buyer question, not a generic keyword.
- Each cluster has a pillar plus 3-5 supporting pieces.
- Brand mentions are naturally placed, not promotional.
- The publish sequence builds citation density over weeks, not days.
- Citation tracking is set up. you cannot improve what you do not measure.

## Common mistakes

- **Generic SEO.** Targeting keywords instead of the buyer's actual question.
- **Promotional tone.** Reddit and Quora communities flag and penalize self-promo.
  the brand mention must be subtle.
- **One-off posts.** A single Reddit answer does not earn an AI citation.
  density across multiple sources is what gets cited.
- **No tracking.** Building content without ever checking whether Rufus actually
  cites it.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
