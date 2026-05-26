---
name: amz-supplier-sample-evaluation
description: >-
  Runs a 25-point quality control test on a supplier sample before mass
  production. Catches the defects that turn into 18% return rates and stranded
  inventory. Produces a back-message to the supplier with specific fixes
  required before greenlighting the PO. Use when a user mentions Alibaba
  sample, supplier sample, sample QC, or before mass production. Trigger
  phrases: "Amazon supplier sample", "Alibaba sample evaluation", "sample
  QC", "before mass production", "supplier quality test". Works with zero tools.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Supplier Sample Evaluation

New sellers order one sample, hold it, say "looks good", wire $8,400 for 1,000
units. Two months later returns hit 18%. The product was 0.4 inches off spec,
the packaging failed FBA prep, the polybag had no suffocation warning. By
then 600 units are stranded. A 25-point sample test before mass production
catches all of this. Costs 30 minutes. Saves $3K-$10K per launch.

## When to use this

- Sample just arrived from a new supplier
- Switching suppliers on an existing SKU
- Adding a new variation (color, size) and supplier sent a sample
- Pre-trade-show evaluation of multiple supplier candidates

## The framework. The 25-Point Sample Test

Five sections, five points each. Each point is pass or fail. Three or more
fails in any single section = full rejection, request a new sample.

### Section 1. Specs (5 points)
1. Dimensions match listing within 3% tolerance
2. Weight matches listing within 5% tolerance
3. Color matches reference Pantone or hex
4. Materials match advertised (cotton vs polyester, real wood vs MDF)
5. Accessories included match the spec (cables, manuals, mounts)

### Section 2. Quality (5 points)
1. Drop test from 3 feet onto hard floor, no functional damage
2. Scratch test with a coin on visible surfaces, no chipping
3. Accuracy test (electronics measure to spec, kitchenware fits standard sizes)
4. Finish inspection, no glue residue, no flash, no rough edges
5. Durability cycle (open/close 50x, plug/unplug 20x), no degradation

### Section 3. Packaging (5 points)
1. Polybag is 1.5+ mil thickness with suffocation warning >= 5/8" type
2. FNSKU barcode placement clean, scannable, not covered by other labels
3. Inserts and manuals included, language correct, no typos
4. Master carton handles factory damage in transit (corner crush test)
5. Per-unit box quality matches premium positioning if applicable

### Section 4. Compliance (5 points)
1. FBA prep type correctly applied (polybag for textile, bubble for fragile)
2. Required certifications visible (CE, FCC, CPSC, FDA where applicable)
3. Warning labels present per category (Prop 65, age warnings, choking hazard)
4. Country of origin marking on product AND retail box per FTC
5. Suffocation warning meets size threshold for the polybag dimensions

### Section 5. Safety (5 points)
1. No sharp edges (touch test on every edge, light pressure)
2. No choking hazards on kids products (small parts test if under-3 age range)
3. No toxic materials (lead, phthalates, formaldehyde) per category MSDS
4. Age-appropriate (heavy parts off toddler items, small magnets off kids')
5. Allergen labeling present on food, supplement, skincare contact items

## Step by step

1. **Unbox in good light.** Photograph the unboxing. Keep the box, polybag,
   inserts.

2. **Run Section 1 Specs.** Use calipers, scale, Pantone book or hex picker.
   Log measurements vs spec sheet.

3. **Run Section 2 Quality.** Perform the destructive tests on one sample if
   multiple. Otherwise functional checks only.

4. **Run Section 3 Packaging.** Verify polybag mil with thickness gauge.
   Scan FNSKU. Read inserts for typos.

5. **Run Section 4 Compliance.** Cross-reference category requirements per
   Amazon and FTC. Photograph any missing labels.

6. **Run Section 5 Safety.** Physical inspection plus material certificate
   review from supplier.

7. **Score the test.** Tally pass/fail. Any section with 3+ fails: REJECT,
   request new sample. Any single fail on safety or compliance: BLOCK PO until
   resolved.

8. **Write supplier message.** Specific, photo-attached, actionable. Set a
   deadline. Re-sample required if changes are material.

9. **Run the quality check**, then decide.

## Output format

```
## Sample Evaluation. [Supplier] / [Product]

**Section scores**
1. Specs: [X] / 5
2. Quality: [X] / 5
3. Packaging: [X] / 5
4. Compliance: [X] / 5
5. Safety: [X] / 5

**Verdict**: [APPROVE / REVISE / REJECT / BLOCK]

**Failed points with detail**
- Point [X.Y]: [what failed] | photo: [file] | required fix: [specific]

**Supplier message (ready to send)**

Hi [supplier name],

Thank you for the sample. We have completed our quality review. Before
production, the following items need to be addressed:

1. [Issue 1 with specific spec/photo reference]
2. [Issue 2]
3. [...]

Please confirm changes and send a revised sample by [date]. We cannot proceed
to PO until these are resolved.

Best,
[Buyer name]
```

## Worked example

Supplier: Shenzhen Hengli, Product: bamboo cutting board 16x10x0.75 inches,
sample arrived day 14 of negotiation.

Section 1 Specs: 4/5. Width measured 9.6" instead of 10" (4% off, fail).
Section 2 Quality: 5/5. Pass all.
Section 3 Packaging: 3/5. Polybag is 1.2 mil (fail), no suffocation warning
(fail), FNSKU placement covers Country of Origin (fail). Hits the 3-fail
section threshold = REJECT.
Section 4 Compliance: 4/5. Country of Origin not on product, only on box (fail).
Section 5 Safety: 5/5. Pass.

Verdict: REJECT. Request new sample with: width corrected to 10", polybag 1.5 mil
with 5/8" suffocation warning, FNSKU placement on side panel, Country of Origin
laser-etched on bottom of board. Lead time impact: +14 days. Cost impact: $0.04
per unit polybag upgrade. Without this catch: 1,000 units would have arrived,
failed FBA receiving on the polybag spec, 1,000 units returned to 3PL for
re-prep at $0.85 per unit = $850 rework cost plus 21 days delay.

## Quality check

- Calipers used for dimension check, not a tape measure
- Photos taken at every fail point, not just notes
- Material certificates requested if any Section 5 doubt exists
- Mil gauge used on polybag, not estimated
- Supplier message specifies a deadline, not "soon"

## Common mistakes

- **Eyeballing dimensions.** A 4% width error is invisible to the eye, fatal in returns.
- **Approving on the "looks good" test.** No structured rubric = inconsistent QC.
- **Skipping Section 4 compliance.** Missing CE or FCC mark on electronics = listing suppression and FBA rejection.
- **One sample, multiple variations.** Different colors often come from different molds. Sample each.
- **No re-sample after fixes.** Verbal promise to fix is not a verified fix. Pay $40 for a re-sample.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
