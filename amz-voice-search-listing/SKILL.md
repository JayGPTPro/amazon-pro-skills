---
name: amz-voice-search-listing
description: >-
  Optimize a listing for Amazon voice shopping (Alexa+, Echo, smart-home
  devices). Voice queries are conversational, longer, and intent-loaded
  ("best running shoes under $100 for flat feet"). This skill rewrites titles,
  bullets, and attributes to surface in voice intent. Use when a user asks
  about Alexa voice shopping, voice search, smart speaker discovery, or
  conversational query optimization. Trigger phrases: "voice shopping",
  "Alexa search", "voice query", "smart speaker", "conversational shopping".
  Works with zero tools.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Voice Search Listing Optimization

Voice shopping queries on Alexa+ and Echo devices are longer, more conversational,
and carry explicit constraints ("under $100", "for kids", "without sugar"). The AI
matches voice queries to listings differently than text search. this skill rewrites
the listing for that match.

## When to use this

- A category where voice shopping share is meaningful (pantry, household, baby,
  pet, beauty replenishment).
- The seller wants reach beyond keyboard search.
- A subscribe-and-save consumable product where voice reorders are common.
- Alexa+ rolled out and the seller's category is conversational.

## The framework. The Voice Query Anatomy

Voice queries have three parts the AI parses:

1. **The product noun.** "running shoes", "coffee pods", "diapers".
2. **The constraints.** Price band, size, count, audience, attribute. "under $50",
   "for sensitive skin", "decaf".
3. **The intent verb (sometimes).** "reorder", "find", "best", "cheapest".

A listing optimized for voice matches all three explicitly. text search tolerates
partial matches. voice does not, because the AI parses literally.

## Step by step

1. **Collect inputs.** Product, current title and bullets, attribute section, the
   typical voice phrases a buyer might use for this product.

2. **Build the voice phrase set.** 10-15 realistic voice queries with the noun,
   constraints, and intent verb.

3. **Cross-reference the listing.** For each voice phrase, does the listing
   currently contain all three parts in matchable form?

4. **Rewrite the title.** Lead with the product noun, then the most common
   constraint (price band, size, audience), then brand. avoid keyword-stuffing.
   voice queries reward clear nouns.

5. **Complete the attribute section.** Voice queries lean heavily on the structured
   attributes (price tier, size, audience, count). Fill every voice-relevant field.

6. **Rewrite one bullet** as a clear "this product is for [audience] who want
   [constraint]". the AI extracts this for voice match.

7. **Plan for replenishment voice queries** if applicable. Enroll in Subscribe &
   Save (see `amz-subscribe-save`). voice reorders go through SnS first.

8. **Run the quality check**, then deliver.

## Output format

```
## Voice Search Optimization. [ASIN]

### Voice phrase set
1. [phrase] . noun: [...] . constraints: [...] . intent: [...]
...

### Listing changes
Title rewrite: [before → after]
Attribute fills: [list of voice-relevant attributes to complete]
Audience bullet: [new bullet text]

### Replenishment plan
[SnS enrollment if consumable, voice reorder flow]
```

## Worked example

A coffee brand selling 12-count pods. Voice phrases: "Alexa, find decaf coffee pods
under $20", "Alexa, reorder coffee pods", "best medium roast K-cups for a Keurig
under fifteen dollars". Title currently: "Premium Coffee K-Cup Pods, Medium Roast,
Single Serve, 24 Count". Rewrite: "Medium Roast K-Cup Coffee Pods, Decaf Available,
12 Count, Fits Keurig". (Prices in titles violate Amazon style guidelines. the
price-tier signal goes in the Attributes section, not the title.) Attributes filled: roast level, caffeine
content, count, machine compatibility, price band. New bullet: "For Keurig owners
who want a medium roast without the caffeine, in a 12-pod count under 15 USD."
Voice query "decaf coffee pods under 20 dollars" now matches strongly. Enrolled in
Subscribe & Save so voice reorders flow through it.

## Quality check

- 10+ realistic voice phrases were modeled before any rewrite.
- Each phrase's noun, constraints, and intent verb are checked against the listing.
- Title leads with the product noun and the top constraint.
- Voice-relevant attribute fields are filled (price tier, audience, compatibility).
- Replenishment is planned for consumable products through Subscribe & Save.

## Common mistakes

- **Optimizing for text only.** Voice queries are structurally different and parsed
  literally.
- **Keyword-stuffed titles.** Voice does not parse a list of synonyms well. clear
  nouns and constraints win.
- **Empty attribute fields.** Voice extracts heavily from attributes. blank fields
  mean no match.
- **Ignoring replenishment.** A consumable without SnS misses the entire "Alexa,
  reorder" use case.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
