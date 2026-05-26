---
name: amz-ai-image-policy-compliance
description: >-
  Audits AI-generated or AI-enhanced listing images against the 2026 Amazon
  disclosure and representation policy before submission. About 23% of AI
  images get rejected in Q1 2026, this gate flow catches them. Use when a user
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
disclosure and representation policy landed and turned it into a minefield.
About 23% of AI-enhanced lifestyle images submitted Q1 2026 got rejected.
Rejection means image stripped, ranking penalty, sometimes a manual review
flag on the account. A 5-gate audit before submission catches the issues that
trigger Amazon's automated AI detection.

## When to use this

- Generated a lifestyle scene with Nano Banana or Gemini and want to ship it
- Replaced a real product photo with a CGI/AI render
- A composite where the product is real but the model/scene is AI
- Pre-launch image set review before bulk upload

## The framework. The Five-Gate AI Image Audit

Each image passes through 5 gates in order. Fail any gate, fix before next.

| Gate | Question | Pass condition |
|---|---|---|
| 1. Product photo authentic | Is the product depiction a real photograph or AI? | Real photo of actual unit. AI-generated product is blocked. |
| 2. Scene authenticity | If the scene is AI, does it accurately depict the product? | Color, dimensions, texture, materials match physical product within 5% tolerance |
| 3. Accuracy vs reference | Compared to real product photo, what is the delta? | No invented features, no exaggerated size, no false materials |
| 4. Disclosure language | Is required Amazon AI disclosure metadata present? | "Image contains AI-generated elements" alt text + image content type field set correctly |
| 5. Policy risk flags | Does the image imply something it should not? | No implied human endorsement, no faked use cases, no implied performance claims, no faked before/after |

## Step by step

1. **Inventory the image set.** For each image, classify: 100% real photo, 100%
   AI, or hybrid (real product + AI scene).

2. **Gate 1: Product photo authenticity.** For each image, confirm the product
   pixels are from a real photograph of the actual unit. AI-generated product
   pixels are policy-blocked since 2026.

3. **Gate 2: Scene authenticity.** If the scene is AI, hold up a real reference
   photo of the product. Check color (delta E < 5), dimensions (within 5%),
   visible materials and textures. Mismatch = revise prompt.

4. **Gate 3: Accuracy vs reference.** Visual compare to listing main image.
   Flag any feature that exists in the AI image but not the product (extra
   button, fake LED, fake texture). Strip the invention.

5. **Gate 4: Disclosure language.** Add Amazon-required disclosure in image
   alt text and select "AI-generated" content type when uploading via API or
   Manage Images.

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

**Disclosure metadata to apply (per image)**
- Alt text: "[descriptive text]. Image contains AI-generated elements."
- Content type: AI-generated [yes/no]
- Composite: [yes/no]

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

Result: 5 of 8 ship as-is, 3 revised, 0 rejected by Amazon on upload. Without
this audit, expected rejection rate on this set was 3-4 images.

## Quality check

- Real reference photo used for Gate 2 comparison, not a render
- Delta E color check actually performed, not eyeballed
- Disclosure alt text added per image, not just on main
- Gate 5 checklist reviewed against current Amazon 2026 policy doc
- AI-generated content type flag set when uploading

## Common mistakes

- **Using AI product pixels.** Hard block in 2026. The product must be photographed.
- **Skipping color check.** Customers return when the real product is darker/lighter than the AI scene.
- **No disclosure metadata.** Even compliant images get flagged without the alt text disclosure.
- **AI humans implying endorsement.** Hands holding the product, models wearing apparel. All Gate 5 triggers.
- **Fake before/after scenes.** Weight loss, hair growth, cleaning results. Instant policy violation.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
