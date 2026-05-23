---
name: amz-listing-suppression-recovery
description: >-
  Recover a suppressed, blocked, or deactivated Amazon listing. Maps the
  suppression reason code to the specific fix path and produces the
  reinstatement message. Use when a user asks about a suppressed listing, a
  blocked listing, listing deactivated, pricing error suppression, image policy,
  restricted phrase, or missing required field. Trigger phrases: "suppressed
  listing", "blocked listing", "listing deactivated", "pricing error",
  "image suppression", "restricted phrase". Works with zero tools. the user
  pastes the suppression notice.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Listing Suppression Recovery

Listings are suppressed for a long list of reasons, most of which Amazon states only
in code form. Sellers waste days guessing. This skill matches the reason code to the
fix and writes the reinstatement message.

## When to use this

- A listing was suppressed and the seller does not know why.
- The reason code is vague (e.g. 'pricing error' on a product that always sold at
  this price).
- An image was suppressed but the seller does not see what is wrong.
- Multiple SKUs suppressed and the seller wants a process.

## The framework. The Reason-Code Map

Suppression reasons cluster into seven groups. Each has a specific fix path.

| Reason group | Common code language | Fix path |
|--------------|---------------------|----------|
| Pricing | "pricing error", "high price" | Lower to reasonable, fix list price reference, contact Pricing team |
| Image | "main image policy", "additional image issue" | Reshoot to spec, white background, no text |
| Restricted phrase | "restricted phrase detected" | Remove the flagged word from title/bullets/description |
| Missing required field | "missing attribute", "incomplete listing" | Fill the category-required attribute |
| Variation issue | "parent-child conflict", "variation theme invalid" | Re-establish theme, separate offending child |
| Compliance | "safety document required", "certification missing" | Submit the requested document |
| Dimensional mismatch | "package dimensions" | Update dimensions to match real product |

## The pricing-error trap

The most common modern suppression. Amazon thinks your price is "higher than typical
on Amazon and other sites." Fixes: drop price to a reasonable level temporarily,
correct your list/MSRP reference price, or contact Amazon's pricing-suppression team
with comparable-price evidence. Raising the price back can be done after the listing
is restored.

## Step by step

1. **Read the exact suppression text.** Amazon's wording maps to one of the seven
   groups.

2. **Classify the suppression** into the right group.

3. **Apply the fix path.** Specific to the group. e.g. for image: reshoot to spec
   and re-upload. For pricing: drop or correct the reference.

4. **Write the reinstatement message** (if Amazon's case process requires one).
   Factual, references the specific fix, attaches evidence.

5. **Submit and watch the listing status.** Most suppressions clear within 24-72
   hours of the right fix. some require multiple submissions.

6. **Prevent recurrence.** If a restricted phrase or image policy issue, build the
   check into the listing workflow.

7. **Run the quality check**, then deliver.

## Output format

```
## Suppression Recovery. [ASIN]

Reason group: [group]   Code text: [Amazon's exact wording]

### Fix path
1. [specific change to the listing or attribute]
2. [submission method: re-publish vs case]

### Reinstatement message (if needed)
[factual, evidence-referenced text]

### Prevention
[what to add to the listing workflow]
```

## Worked example

A listing suppressed with "main image policy". Investigation: the listing's main
image has a small logo watermark in the corner, which violates Amazon's policy of no
text or logo on the main image. Fix path: reshoot or edit the main image to remove
the watermark, upload as new main, wait for re-index. Reinstated within 24 hours.
Prevention: add a pre-upload check to the listing workflow that the main image is
pure white, no text, no logo, no text overlay.

## Quality check

- The suppression text is read literally and matched to a group, not guessed.
- The fix path is specific to that group, not generic.
- Pricing suppressions are recognized as a specific case with its own playbook.
- The reinstatement message (if used) references the fix and attaches evidence.
- A prevention step is included so the same suppression does not recur.

## Common mistakes

- **Guessing the reason.** Acting on a hunch instead of reading the exact text.
- **Generic resubmission.** Submitting the same listing unchanged.
- **Fighting a pricing suppression.** The fix is usually a temporary price drop or a
  reference-price correction, not a long argument with Amazon.
- **No prevention.** Restoring the listing without adding the policy check that
  catches it next time.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
