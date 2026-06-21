---
name: amz-backend-keywords
description: >-
  Build the optimal 250-byte Amazon backend search term string. Collects every
  candidate keyword, removes anything already indexed in the title and bullets,
  strips duplicates and Amazon-prohibited terms, prioritizes by search value, and
  packs the field to the byte limit. Use when a user asks about backend keywords,
  search terms, the hidden keyword field, generic keywords, "Search Terms" in the
  listing back end, or wants to fix wasted backend space. Trigger phrases:
  "backend keywords", "search terms field", "hidden keywords", "250 bytes",
  "generic keywords". Works with zero tools. the user pastes the current title,
  bullets, and any keyword list.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Backend Keyword Packer

The backend Search Terms field is 250 bytes of pure indexing power that most sellers
either leave half empty or fill with words Amazon already indexed from the title.
This skill packs that field for maximum reach with zero waste.

## When to use this

- A new listing is going live and the Search Terms field is blank.
- An existing listing has never had its backend field optimized.
- A product is not indexed for keywords the seller expects to rank for.
- The Search Terms field contains brand names, repetition, or filler.

## The rule that everyone gets wrong

Amazon indexes the backend field once. A keyword already in your title or bullets is
already indexed. Repeating it in the backend wastes bytes and buys nothing. The
backend field is for the keywords that did NOT make it into your visible copy:
synonyms, alternate spellings, use cases, and audience terms.

## The framework. The Backend Funnel

Run every candidate keyword through five gates. What survives gets packed.

1. **Gate 1. Already indexed?** If the word appears in the title or bullets, drop it.
   Amazon already has it.
2. **Gate 2. Prohibited?** Drop brand names (yours or others), ASINs, competitor
   names, profanity, temporary claims ("new", "sale", "best"), and subjective claims.
   Amazon ignores or penalizes these.
3. **Gate 3. Relevant?** Drop anything that would bring the wrong shopper. Irrelevant
   keywords hurt conversion-based ranking.
4. **Gate 4. Duplicate?** Each word needs to appear only once across the whole field,
   in any order. "leather phone case" and "case for phone leather" are the same three
   words. Keep one set.
5. **Gate 5. Worth the bytes?** Rank survivors by search value. When the field is
   full, the lowest-value words are cut.

## Packing rules

- The limit is **250 bytes**, not characters. Most letters are 1 byte. accented and
  non-Latin characters can be 2 or more. Count bytes.
- **No commas needed.** Separate words with single spaces. Commas waste bytes.
- **Word order does not matter.** Amazon matches words in any order, so never write
  phrases. write a bag of unique words.
- **Singular or plural, pick one.** Amazon usually stems regular plurals, so do not
  spend bytes on both "bottle" and "bottles". The exception is irregular plurals
  (knife/knives, mouse/mice, child/children). include both forms.
- **Include** common misspellings, alternate spellings, abbreviations, synonyms,
  Spanish terms for the US market where relevant, and use-case and audience words.

## Step by step

1. **Collect inputs.** The current title, all bullets, the product, the category, and
   any keyword list the user already has. If no keyword list exists, generate
   candidates from synonyms, use cases, audiences, materials, and occasions.

2. **Build the indexed set.** Extract every meaningful word from the title and bullets.
   this is the "already indexed" exclusion list.

3. **Run all candidates through the five gates.**

4. **Rank survivors** by estimated search value, highest first.

5. **Pack to 250 bytes.** Add words highest value first until the next word would
   exceed the limit. Report the final byte count and which words were cut.

6. **Run the quality check**, then deliver.

## Output format

```
## Backend Search Terms. [Product]

[the final space-separated string]

Byte count: [X] / 250
Words included: [N]
Cut for space (next in line): [words]
Deliberately excluded: [word . reason]
```

## Worked example

Product: insulated stainless water bottle. Title already contains "insulated
stainless steel water bottle 32 oz".

- Dropped by Gate 1: insulated, stainless, steel, water, bottle, oz. already indexed.
- Kept: thermos flask canteen tumbler hydro jug leakproof gym hiking camping
  travel sports kids reusable bpa free wide mouth cold hot drinks.
- Dropped by Gate 2: a competitor brand name the user had pasted in.
- Final string packed to 247 of 250 bytes.

The win is not adding more words. it is not wasting a single byte on a word the
title already covers.

## Quality check

- Zero words from the field also appear in the title or bullets.
- Zero brand names, ASINs, or competitor names.
- Zero temporary or subjective claims ("best", "new", "sale", "amazing").
- Every word appears only once. no phrases, no repeated stems.
- Separated by single spaces, no commas.
- Byte count is 250 or below, and reported.
- Every included word could plausibly be typed by a real buyer.

## Common mistakes

- **Repeating the title.** The most common waste. half the field gone for nothing.
- **Counting characters, not bytes.** A field that looks under 250 characters can be
  over 250 bytes and get truncated silently.
- **Writing phrases.** "best water bottle for hiking" wastes "best" and the word order.
  write "hiking" once and let Amazon combine.
- **Brand names.** Putting your own or a competitor brand in the field. ignored at
  best, penalized at worst.
- **Both singular and plural.** Doubles the cost for no extra reach.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
