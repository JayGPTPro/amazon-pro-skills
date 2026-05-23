---
name: amz-ai-search-optimization
description: >-
  Optimize a listing for Amazon's AI shopping assistants (Rufus, Alexa+, and the
  COSMO ranking layer). Rewrites bullets as question answers, completes the
  Attributes section, structures the listing for AI-driven query expansion, and
  reinforces with review-language. Use when a user asks about Rufus, Alexa+,
  AI shopping, AI-driven search, COSMO, conversational shopping, or
  question-style queries. Trigger phrases: "Rufus", "Alexa+", "AI shopping",
  "AI search", "COSMO", "conversational query", "question answering". Works
  with zero tools.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# AI Search Optimization (Rufus + Alexa+ + COSMO)

Amazon's AI assistants (Rufus on the web and the new Alexa+ on devices, plus the
COSMO ranking layer behind them) changed how shoppers find products. Queries are
longer and more conversational, and the AI cites the listing sections that answer
questions directly. Optimizing for the AI is now part of SEO.

## When to use this

- Listing built before the AI assistants rolled out and feels like it lost reach.
- Customers are asking questions in queries (longer, "best X for Y under $Z").
- Attributes section is half-filled or empty.
- The seller wants to surface in the AI's "Researched by AI" recommendations.

## The framework. The Four-Step AI Rewrite

1. **Intent map.** List the 10-20 questions a real buyer asks before choosing this
   product. "How long does the battery last?", "Will it fit a 15-inch laptop?",
   "Is it dishwasher safe?". These are the queries the AI now sees.

2. **Attributes audit.** Open the Seller Central Attributes section for this listing.
   Fill every field the category template offers. battery life, materials,
   dimensions, certifications, compatibility, use cases. The AI reads attributes
   before it reads the title. most sellers fill under 40 percent of fields. this is
   where most of the AI-readable signal sits.

3. **Q&A bullets.** Rewrite bullets to directly answer the top buyer questions.
   Lead with the answer, then the supporting detail. Each bullet maps to one
   question from the intent map.

4. **Review-language reinforcement.** Mine the listing's own reviews and competitor
   reviews for the exact words customers use. weave those phrases into bullets and
   A+ text. The AI cross-references review language. matching it lifts relevance.

## Step by step

1. **Collect inputs.** Product, listing copy, current Attributes section status,
   recent reviews of own product and key competitors.

2. **Build the intent map.** 10-20 real buyer questions, drawn from product
   research, customer questions tab, and review themes.

3. **Audit the Attributes section.** List fields available in the category, fields
   currently filled, fields empty. Identify the high-impact empty fields.

4. **Rewrite the bullets** as Q&A. one question per bullet, answer-first.

5. **Mine review language** and weave the customer's words into bullets and A+.

6. **Plan external content** (briefly, with a handoff to amz-aeo-external-content
   for deeper work) so the brand shows up in the AI's external-source citations.

7. **Run the quality check**, then deliver.

## Output format

```
## AI Search Optimization. [ASIN]

### Intent map
[10-20 buyer questions]

### Attributes audit
Filled: [%]   High-impact empty fields: [list]   Fill priority: [order]

### Bullet rewrite (Q&A format)
1. Q: [question] . Bullet: [answer-first text]
...

### Review language to weave in
[phrases from real reviews]

### External handoff
[topics for off-Amazon content. see amz-aeo-external-content-plan]
```

## Worked example

A 15-inch laptop sleeve listing. Intent map includes "Will it fit a 15-inch MacBook
Pro?", "Is the padding real or thin?", "Does it fit in a backpack?". Attributes
section is 38% filled, missing material, dimensions, compatibility list, and water
resistance. Bullets are feature-list ("Padded interior. Water-resistant exterior.")
rewritten Q&A-style: "Fits all 15-inch MacBook Pros and most 15.6-inch PC laptops.
Confirmed up to 14.2 x 9.8 x 0.8 inches." Review language pulled: "magnetic
closure", "thick foam", "feels premium". All three weave into bullets and A+. AI
queries like "what laptop sleeve fits a 15-inch MacBook Pro with thick padding" now
match this listing strongly.

## Quality check

- An intent map of 10+ real buyer questions exists before any rewrite.
- The Attributes section audit names specific empty high-impact fields.
- Every bullet answers one question, answer-first.
- Review language is incorporated, not just brand language.
- The skill connects to the external-content plan for the off-Amazon side.

## Common mistakes

- **Ignoring the Attributes section.** The single highest-impact AI-readable signal,
  routinely half-filled.
- **Bullets as feature lists.** "Stainless steel construction" is not an answer to
  any buyer question.
- **Brand-language only.** Customers use different words. matching their language is
  the lift.
- **Stopping at the listing.** The AI cites external content too. a fully optimized
  listing without an external content plan misses half the surface area.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
