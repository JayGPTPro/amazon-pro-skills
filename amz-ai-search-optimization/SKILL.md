---
name: amz-ai-search-optimization
description: >-
  Optimize a listing for Amazon's AI shopping assistants (Rufus on the web,
  Alexa+ on devices, and the COSMO ranking layer behind them). Rewrites bullets
  as question answers, completes the Attributes section, models voice query
  anatomy, and reinforces with review-language. Use when a user asks about
  Rufus, Alexa+, AI shopping, AI-driven search, COSMO, conversational shopping,
  question-style queries, voice shopping, voice search, smart speaker
  discovery, or conversational query optimization. Trigger phrases. "Rufus",
  "Alexa+", "AI shopping", "AI search", "COSMO", "conversational query",
  "question answering", "voice shopping", "Alexa search", "voice query", "smart
  speaker", "conversational shopping". Works with zero tools.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# AI Search Optimization (Rufus + Alexa+ + COSMO)

Amazon's AI assistants (Rufus on the web, Alexa+ on devices, and the COSMO ranking
layer behind them) changed how shoppers find products. Queries are longer and more
conversational, and the AI cites the listing sections that answer questions
directly. Optimizing for the AI is now part of SEO, and it covers both typed
conversational queries (Rufus) and spoken ones (Alexa+).

## When to use this

- Listing built before the AI assistants rolled out and feels like it lost reach.
- Customers are asking questions in queries (longer, "best X for Y under $Z").
- Attributes section is half-filled or empty.
- The seller wants to surface in the AI's "Researched by AI" recommendations.
- A category where voice shopping share is meaningful (pantry, household, baby,
  pet, beauty replenishment).
- A subscribe-and-save consumable product where voice reorders are common.

## The framework. The Four-Step AI Rewrite

1. **Intent map.** List the 10-20 questions a real buyer asks before choosing this
   product. "How long does the battery last?", "Will it fit a 15-inch laptop?",
   "Is it dishwasher safe?". These are the queries the AI now sees.

2. **Attributes audit.** The Seller Central Attributes section is the single
   highest-impact AI-readable signal. the AI reads attributes before the title, and
   most listings leave the section badly under-filled. For the full attributes fill
   audit, see `amz-attributes-completer`. here, just confirm the high-impact
   AI-relevant fields are populated. battery life, materials, dimensions,
   certifications, compatibility, use cases.

3. **Q&A bullets.** Rewrite bullets to directly answer the top buyer questions.
   Lead with the answer, then the supporting detail. Each bullet maps to one
   question from the intent map.

4. **Review-language reinforcement.** Mine the listing's own reviews and competitor
   reviews for the exact words customers use. weave those phrases into bullets and
   A+ text. The AI cross-references review language. matching it lifts relevance.

## Voice query anatomy (Alexa+ specifically)

Typed Rufus queries can be discursive. Spoken Alexa+ queries are short and parsed
literally. The AI breaks a voice query into three parts. listings that match all
three explicitly win the voice surface.

1. **The product noun.** "running shoes", "coffee pods", "diapers".
2. **The constraints.** Price band, size, count, audience, attribute. "under $50",
   "for sensitive skin", "decaf".
3. **The intent verb (sometimes).** "reorder", "find", "best", "cheapest".

A listing optimized for voice exposes the noun, constraints, and intent verb in
matchable form. Text search tolerates partial matches. voice does not. The
Attributes section and one explicit "this product is for [audience] who want
[constraint]" bullet do most of the work. For consumables, enroll in Subscribe &
Save so the "Alexa, reorder" use case lands on this listing (see
`amz-subscribe-save`).

## Step by step

1. **Collect inputs.** Product, listing copy, current Attributes section status,
   recent reviews of own product and key competitors, and the typical voice phrases
   a buyer might use if the category is voice-relevant.

2. **Build the intent map.** 10-20 real buyer questions for Rufus, drawn from
   product research, customer questions tab, and review themes.

3. **If voice-relevant, build the voice phrase set.** 10-15 realistic voice queries
   with the noun, constraints, and intent verb. Cross-reference the listing. for
   each voice phrase, does the listing currently contain all three parts in
   matchable form?

4. **Audit the Attributes section.** List fields available in the category, fields
   currently filled, fields empty. Identify the high-impact empty fields, with
   special weight on voice-relevant attributes (price tier, audience,
   compatibility, count).

5. **Rewrite the bullets** as Q&A. one question per bullet, answer-first. Include
   one explicit audience-and-constraint bullet for voice match.

6. **Mine review language** and weave the customer's words into bullets and A+.

7. **Title.** If voice is in scope, lead with the product noun, then the top
   constraint (size, count, audience), then brand. avoid keyword-stuffing. voice
   queries reward clear nouns.

8. **Plan for replenishment voice queries** if applicable. Enroll in Subscribe &
   Save. voice reorders go through SnS first.

9. **Plan external content** (briefly, with a handoff to amz-aeo-external-content
   for deeper work) so the brand shows up in the AI's external-source citations.

10. **Run the quality check**, then deliver.

## Output format

```
## AI Search Optimization. [ASIN]

### Intent map (Rufus)
[10-20 buyer questions]

### Voice phrase set (Alexa+, if in scope)
1. [phrase] . noun: [...] . constraints: [...] . intent: [...]
...

### Attributes audit
Filled: [%]   High-impact empty fields: [list]   Fill priority: [order]

### Bullet rewrite (Q&A format)
1. Q: [question] . Bullet: [answer-first text]
...
Audience bullet (voice): [text]

### Title (if changed)
Before: [...] . After: [...]

### Review language to weave in
[phrases from real reviews]

### Replenishment plan (if consumable)
[SnS enrollment, voice reorder flow]

### External handoff
[topics for off-Amazon content the AI assistants cite. Reddit, YouTube, Quora]
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

Voice-side example. A coffee brand selling K-cups. Voice phrases: "Alexa, find
decaf coffee pods", "Alexa, reorder coffee pods", "best medium roast K-cups for a
Keurig". Title rewrite leads with the noun and the top constraint. attributes
filled: roast level, caffeine content, count, machine compatibility, price band.
New audience bullet: "For Keurig owners who want a medium roast without the
caffeine, in a 12-pod count." Enrolled in Subscribe & Save so voice reorders flow
through it.

## Quality check

- An intent map of 10+ real buyer questions exists before any rewrite.
- If voice-relevant, 10+ realistic voice phrases were modeled with noun,
  constraints, and intent verb.
- The Attributes section audit names specific empty high-impact fields, including
  voice-relevant ones.
- Every bullet answers one question, answer-first.
- At least one bullet explicitly states audience and constraint for voice match.
- Review language is incorporated, not just brand language.
- Replenishment is planned for consumable products through Subscribe & Save.
- The skill connects to the external-content plan for the off-Amazon side.

## Common mistakes

- **Ignoring the Attributes section.** The single highest-impact AI-readable signal,
  routinely half-filled.
- **Bullets as feature lists.** "Stainless steel construction" is not an answer to
  any buyer question.
- **Brand-language only.** Customers use different words. matching their language is
  the lift.
- **Optimizing for text only.** Voice queries are structurally different and parsed
  literally. attributes carry the voice match.
- **Keyword-stuffed titles.** Voice does not parse a list of synonyms well. clear
  nouns and constraints win.
- **Ignoring replenishment.** A consumable without SnS misses the entire "Alexa,
  reorder" use case.
- **Stopping at the listing.** The AI cites external content too. a fully optimized
  listing without an external content plan misses half the surface area.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
