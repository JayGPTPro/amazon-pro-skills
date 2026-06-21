---
name: amz-ai-image-policy-compliance
description: >-
  Audits AI-generated or AI-enhanced listing images against the 2026 Amazon
  disclosure and representation policy before submission. A 5-gate flow catches
  the issues that trigger suppression or a misrepresentation flag. Use when a user
  asks about AI image policy, AI photo rules, image suppression, or 2026 image
  compliance. Trigger phrases: "AI image Amazon policy", "AI generated photos
  listing", "image suppression AI", "Amazon AI image rules 2026". Works with
  zero tools.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# AI Image Policy Compliance

AI image generation became mainstream for Amazon sellers in 2025. Then the 2026
disclosure and representation policy raised the bar. Two rules sit at the core:
sellers must clearly disclose images that are substantially AI-generated, and
every image must accurately represent the physical product that ships, regardless
of the tool used to make it. Get either wrong and the image can be suppressed,
sometimes with a misrepresentation flag on the account. A 5-gate audit before
submission catches the issues before upload.

## When to use this

- Generated a lifestyle scene with Nano Banana or Gemini and want to ship it
- Replaced a real product photo with a CGI/AI render
- A composite where the product is real but the model/scene is AI
- Pre-launch image set review before bulk upload

## The framework. The Five-Gate AI Image Audit

Each image passes through 5 gates in order. Fail any gate, fix before next.

| Gate | Question | Pass condition |
|---|---|---|
| 1. Product photo authentic | Is the product depiction a real photograph or AI? | Real photo of actual unit. an AI-fabricated product depiction risks the misrepresentation rule. |
| 2. Scene authenticity | If the scene is AI, does it accurately depict the product? | Color, dimensions, texture, materials match the physical product. tight match, this skill uses a tolerance heuristic, not an Amazon number |
| 3. Accuracy vs reference | Compared to real product photo, what is the delta? | No invented features, no exaggerated size, no false materials |
| 4. Disclosure | Is the image substantially AI-generated, and if so is it disclosed? | If substantially AI-generated, a clear plain-language disclosure is added prominently (Amazon points to the product description). minor retouching may not require it |
| 5. Policy risk flags | Does the image imply something it should not? | No implied human endorsement, no faked use cases, no implied performance claims, no faked before/after |

The Gate 2 match thresholds this skill applies, a color difference under roughly Delta E 5
and a size deviation under about 5 percent, are the skill's own QA heuristic for flagging
drift. Amazon does not publish a numeric tolerance. its actual rule is qualitative:
disclose substantial AI generation and represent the real product accurately.

## Step by step

1. **Inventory the image set.** For each image, classify: 100% real photo, 100%
   AI, or hybrid (real product + AI scene).

2. **Gate 1: Product photo authenticity.** For each image, confirm the product
   pixels are from a real photograph of the actual unit. an AI-fabricated product
   depiction runs straight into the 2026 misrepresentation rule.

3. **Gate 2: Scene authenticity.** If the scene is AI, hold up a real reference
   photo of the product. Check color, dimensions, visible materials and textures
   against it. The thresholds this skill uses below (a Delta E color limit, a
   percentage size band) are the skill's own QA heuristic for catching drift, not
   an Amazon-published rule. Mismatch = revise prompt.

4. **Gate 3: Accuracy vs reference.** Visual compare to listing main image.
   Flag any feature that exists in the AI image but not the product (extra
   button, fake LED, fake texture). Strip the invention.

5. **Gate 4: Disclosure.** If the image is substantially AI-generated, add a
   clear, plain-language disclosure that buyers can understand. Amazon's current
   guidance points to the product description, near the top. Minor retouching
   (crop, brightness, background removal) generally does not require disclosure.
   confirm the current placement and wording in Amazon's policy, since this is
   tightening through 2026.

6. **Gate 5: Policy risk flags.** Run the policy checklist below. Common
   triggers: humans appearing to endorse the product, before/after weight loss
   scenes, food preparation showing impossible results, kids using adult
   products.

7. **Final pass/fail per image.** All 5 gates pass = ship. Any fail = revise.

8. **Run the quality check**, then submit.

## Output format

```
## AI Image Audit. [SKU / image set]

**Per-image pass/fail**
Image # | Gate 1 | Gate 2 | Gate 3 | Gate 4 | Gate 5 | Verdict | Fix needed
1       | PASS   | PASS   | FAIL   | PASS   | PASS   | REVISE  | Remove fake LED indicator
2       | PASS   | PASS   | PASS   | PASS   | PASS   | SHIP    |
3       | FAIL   | -      | -      | -      | -      | REJECT  | Product is fully AI, re-shoot real

**Disclosure to apply**
- Per image, classify: AI-generated [yes/no], Composite [yes/no]
- If any shipping image is substantially AI-generated, add a clear plain-language
  disclosure prominently (Amazon's current guidance points to the product description).
  confirm the exact placement and wording in current Amazon policy before publishing.

**Policy risk summary**
[Any Gate 5 flags surfaced with specific revision instructions]
```

## Worked example

8-image set for kitchen knife block. Real product photographed against white.
Lifestyle scenes (5 of 8) generated in Nano Banana with the real product
composited in.

- Images 1-3: pure product on white, real photos. All gates PASS. SHIP.
- Image 4: AI kitchen scene, knife block composited. Gate 1 PASS, Gate 2 FAIL
  (wood handle color is #6B3410 in AI but actual product is #4A2510). Revise
  prompt with hex code. Resubmit.
- Image 5: AI scene with hand using knife. Gate 5 FAIL (implied human use
  endorsement, hand is AI-generated). Revise to remove hand, show knife in
  cutting board mid-scene without user.
- Image 6: AI before/after of dull vs sharp blade cut. Gate 5 FAIL (performance
  claim implied). Replace with neutral product detail shot.
- Images 7-8: AI scenes, all gates pass. SHIP.

Result: 5 of 8 ship as-is, 3 revised, 0 rejected by Amazon on upload. The three
caught here (a color mismatch, an implied-endorsement hand, a faked before/after)
are exactly the kind of issue that draws suppression or a misrepresentation flag
when it slips through.

## Quality check

- Real reference photo used for Gate 2 comparison, not a render
- Color and size check actually performed against the reference, not eyeballed (using the skill's heuristic, not an Amazon number)
- Disclosure added for any substantially AI-generated image, per current Amazon placement guidance
- Gate 5 checklist reviewed against current Amazon 2026 policy doc
- Each image classified AI-generated yes/no for internal tracking

## Common mistakes

- **Fabricating the product itself with AI.** A made-up product depiction collides with the 2026 misrepresentation rule. show the real unit.
- **Skipping color check.** Customers return when the real product is darker/lighter than the AI scene.
- **Skipping disclosure.** A substantially AI-generated image needs a clear disclosure. confirm Amazon's current placement, do not assume image alt text alone covers it.
- **AI humans implying endorsement.** Hands holding the product, models wearing apparel. All Gate 5 triggers.
- **Fake before/after scenes.** Weight loss, hair growth, cleaning results. Instant policy violation.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
