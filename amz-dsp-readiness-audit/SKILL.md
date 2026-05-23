---
name: amz-dsp-readiness-audit
description: >-
  Assess whether an Amazon brand is ready for Amazon DSP (Demand-Side Platform).
  Scores budget, ASIN coverage, conversion baseline, audience size, and lifecycle
  stage, and outputs an audience-and-creative starter plan or a 'stay on
  Sponsored' recommendation. Use when a user asks about Amazon DSP, programmatic
  ads, Display vs DSP, off-Amazon DSP, or whether they are ready for DSP. Trigger
  phrases: "Amazon DSP", "DSP readiness", "programmatic", "off-Amazon ads",
  "audience targeting at scale". Works with zero tools.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# DSP Readiness Audit

Amazon DSP is powerful but expensive and unforgiving. Sellers who jump in without
the foundation burn budget. This skill scores readiness and either greenlights DSP
with a starter plan or routes the seller back to Sponsored ads.

## When to use this

- The seller is curious about DSP and asks if they should run it.
- An ad agency is pitching DSP and the seller wants an independent check.
- Sponsored ads have plateaued and DSP feels like the next step.
- DSP minimums dropped and it now feels accessible.

## The framework. The Five Readiness Gates

Five gates. Pass 4 or 5 of the gates to greenlight DSP. Fail 2+ and DSP is the
wrong tool right now.

| Gate | Pass condition |
|------|----------------|
| Budget | Sustained $15k+ monthly DSP spend (minimum to meaningfully optimize) |
| ASIN coverage | 10+ ASINs across catalog, or a high-value flagship with adjacent SKUs |
| Conversion baseline | Healthy on-Amazon conversion rate. DSP traffic must convert too |
| Audience size | Brand has retargetable audience (recent viewers, purchasers) or aligned audiences |
| Lifecycle stage | Brand at growth or mature stage. not pre-launch |

## What DSP does well (and doesn't)

- Excellent for: retargeting recent shoppers, custom audiences from purchase data,
  off-Amazon impressions to drive on-Amazon search, video on Twitch / Fire TV.
- Bad for: pre-launch awareness on a single SKU. small budgets that can't reach
  statistical significance. brands with weak listings (DSP delivers traffic to a
  listing that does not convert and the budget burns).

## Step by step

1. **Collect inputs.** Monthly Sponsored ad spend, total catalog ASIN count, average
   conversion rate, on-Amazon retargetable audience size if known, brand lifecycle
   stage.

2. **Score each gate.** Pass or fail.

3. **Tally the readiness verdict.** 4-5 pass = GO, 3 = WATCH, 0-2 = STAY ON
   SPONSORED.

4. **If GO, build the starter plan.** Audiences: views remarketing first, then
   purchases remarketing for repurchase, then aligned-audience prospecting.
   Creatives: video + responsive eCommerce ads. Budget split: 60% retargeting,
   40% prospecting.

5. **If STAY ON SPONSORED, name what to fix.** Usually the listing conversion rate
   or the catalog depth. Re-evaluate in 90 days.

6. **Run the quality check**, then deliver.

## Output format

```
## DSP Readiness. [brand]

### Five-gate score
1. Budget: [pass/fail]
2. ASIN coverage: [pass/fail]
3. Conversion baseline: [pass/fail]
4. Audience size: [pass/fail]
5. Lifecycle stage: [pass/fail]

### Verdict: [GO / WATCH / STAY ON SPONSORED]

### If GO, starter plan
Audiences: [views, purchases, prospecting]
Creatives: [video + responsive eCommerce]
Budget split: [retargeting % / prospecting %]
Initial monthly budget: [$]

### If STAY ON SPONSORED
What to fix first: [conversion / catalog / lifecycle]
Re-evaluate in: [90 days / 6 months]
```

## Worked example

A brand with 5 ASINs, monthly Sponsored spend at 6k USD, average 14% conversion
rate (strong), launched 8 months ago.

Gates: Budget fails (DSP needs sustained 15k+). ASIN coverage fails (5 is too narrow).
Conversion baseline passes. Audience size passes. Lifecycle stage passes.

Verdict: STAY ON SPONSORED. 2 of 5 fail. DSP would burn budget across too few ASINs
with not enough scale to optimize. What to fix first: expand the catalog to 10+
ASINs and grow Sponsored spend to a sustained 15k+ before considering DSP. Re-
evaluate in 6 months. Saved the seller roughly 180k of misallocated 12-month spend.

## Quality check

- All five gates are scored, not just budget.
- The verdict is one of GO, WATCH, STAY, with reasoning.
- A GO verdict includes a specific starter plan with audiences, creatives, and
  budget split.
- A STAY verdict names what to fix and when to re-evaluate.
- The seller is not greenlighted for DSP if they fail 2+ gates, regardless of
  marketing pressure.

## Common mistakes

- **DSP because an agency pitched it.** The agency makes money. the seller does
  not always.
- **Pre-launch DSP.** Almost never works. organic and Sponsored come first.
- **No retargeting base.** Trying to prospect with DSP without an audience is far
  more expensive than warm retargeting.
- **Tiny budget.** A DSP campaign at 3k a month cannot generate the statistical
  significance to optimize.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
