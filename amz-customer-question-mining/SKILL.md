---
name: amz-customer-question-mining
description: >-
  Mine the Customer Questions tab of a listing for unanswered buyer intent.
  Generates branded answers to publish, then feeds the recurring question
  themes back into bullets, A+ content, and backend keywords. Use when a user
  asks about Customer Questions section, Q&A tab, unanswered questions, or
  using questions for SEO. Trigger phrases: "Customer Questions", "Q&A tab",
  "unanswered questions", "questions on my listing". Works with zero tools.
  the user pastes the questions.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Customer Question Mining

Amazon's AI assistants (Rufus, Alexa+) cite the Customer Questions tab when
shoppers ask the same questions. Most sellers leave questions unanswered for weeks.
Each unanswered question is a missed conversion. This skill mines them, answers
them, and feeds the themes back into the listing.

## When to use this

- A listing has many unanswered Customer Questions.
- AI search visibility is weak and the seller wants to lift it.
- Conversion rate is soft and unanswered objections are suspected.
- The seller has no process for the Q&A tab.

## The framework. The Question Loop

1. **Mine.** Pull all open questions and recent answered ones. Cluster by theme.

2. **Answer.** Reply to every open question as the brand. Factual, branded, links
   to relevant policy or warranty where appropriate.

3. **Feed back.** The questions are buyer intent. The themes belong in the bullets,
   the A+, the attributes section, and the backend keywords.

4. **Loop.** New questions arrive. answer within 24 hours. updated bullets prevent
   the same question from being asked again.

## What a branded answer looks like

- Factual. "Yes, the cable is 6 feet long." not "We hope you enjoy our product."
- Specific. Includes the exact spec, not "many sizes available".
- Signed. Says "Brand Team" or your store name.
- Updates the listing copy if the question reveals a missing fact.

## Rufus citation patterns

Rufus and the AI surface cite Customer Questions answers preferentially when those
answers fit a specific shape. Writing for that shape lifts citation rate.

- **Branded and factual, not promotional.** "Yes, this fits a 15-inch MacBook Pro,
  external dimensions 14.2 x 9.8 x 0.8 inches." Promotional language
  ("the best sleeve for your laptop", "you'll love how it fits") gets filtered out.
  Rufus quotes the answer that reads like a spec sheet, not the one that reads
  like marketing.
- **Phrased as the buyer phrased it.** Mirror the buyer's wording in the first
  clause of the answer. "Will this fit a 15-inch MacBook Pro?" gets answered "Yes,
  this fits a 15-inch MacBook Pro." not "Compatibility includes MacBook Pro 15."
  Rufus matches semantic similarity. lead with the buyer's verbatim noun phrase.
- **Answer length 80 to 200 words.** Under 80 the answer is too thin to cite. over
  200 it gets truncated and the cited fragment loses context. The sweet spot is one
  clear yes/no, then 2-3 sentences of specific attribute support, then one
  sentence of practical guidance.
- **Specific attribute claims that match the listing.** Every claim in the answer
  should also appear in the listing copy, A+, or attributes. Rufus cross-references.
  an answer that says "water resistant to IPX4" pulls more weight when the listing
  attributes also carry "water resistance: IPX4". If the listing does not back the
  claim, fix the listing first, then answer.

## Step by step

1. **Collect inputs.** The listing URL or the Customer Questions paste, the
   product, recent bullets and A+ for cross-reference.

2. **Cluster the questions.** Group by theme. compatibility, sizing, materials,
   use case, warranty, country of origin. The cluster sizes show what the listing
   is not communicating clearly.

3. **Draft answers.** One per open question. Factual, branded.

4. **Map clusters to listing changes.**
   - Heavy compatibility cluster: add a compatibility list to attributes and a
     bullet.
   - Heavy sizing cluster: add a size guide image to the gallery.
   - Heavy use-case cluster: rewrite bullet 1 to lead with the use case.
   - Heavy materials cluster: add materials to attributes and bullet 2.

5. **Add the cluster phrases to backend keywords** if not present.

6. **Set the cadence.** Daily check on a busy listing, weekly on slower ones.

7. **Run the quality check**, then deliver.

## Output format

```
## Customer Question Mining. [ASIN]

### Question clusters
1. [theme] . [N questions] . [the missing fact]
2. ...

### Branded answers (one per open question)
Q: [question]
A: [factual branded answer]
...

### Listing updates derived
Bullet: [which bullet to add/edit and what to say]
A+: [module to update]
Attributes: [fields to fill]
Backend keywords: [phrases to add]

### Cadence
[daily / weekly review]
```

## Worked example

A laptop sleeve listing with 18 unanswered questions over 3 months. Clusters:
laptop compatibility (8 questions), zipper durability (4), water resistance (3),
return policy (3).

Branded answers drafted for all 18. Listing updates: add a compatibility list to
attributes ("Fits MacBook Pro 13/14/15/16 inch, Dell XPS 13/15..."), update bullet
3 to lead with "Fits all major 13-16 inch laptops". Add a "Zipper rated to 50,000
cycles" bullet. Add "water resistant" to attributes and a bullet. The water-
resistance question stops being asked because the listing now answers it before
the buyer needs to ask. Sessions stay flat but conversion rises because the listing
now closes the objections the Q&A tab was carrying.

## Quality check

- Every open question gets an answer. none are left.
- Answers are branded and factual, not generic.
- Question clusters drive specific listing changes, not just generic 'improve'.
- Themes are added to attributes and backend keywords, not only bullets.
- A daily or weekly cadence is set so new questions are answered fast.

## Common mistakes

- **Ignoring the tab.** Months of unanswered questions are months of missed
  conversions and AI signal.
- **Generic answers.** "We hope you love our product" is not useful. Specific
  facts are.
- **Answering without updating the listing.** Same question gets asked again next
  week.
- **Letting buyers answer.** Buyer-answered questions get cited by the AI just
  like brand-answered ones. but buyers sometimes give wrong info. answer first.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
