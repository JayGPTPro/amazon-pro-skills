---
name: amz-attribution-campaign-planner
description: >-
  Plan Amazon Attribution setup for external-traffic campaigns (TikTok, IG,
  Google, YouTube, email, influencer). Defines the tag taxonomy, link structure
  per source and creator, and the reporting cadence to measure off-Amazon
  conversion. Use when a user asks about Amazon Attribution, external traffic
  tracking, tagging links, measuring off-Amazon sales, or influencer
  attribution. Trigger phrases: "Amazon Attribution", "external traffic",
  "tag links", "off-Amazon", "influencer attribution". Works with zero tools.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Attribution Campaign Planner

Off-Amazon traffic drives over 40 percent of Amazon sales for many brands, but most
sellers send it untagged and have no idea what works. Amazon Attribution gives the
visibility, but only with the right tag taxonomy. This skill plans it.

## When to use this

- The brand is sending external traffic (social, email, influencer, paid) and
  cannot tell which source converts.
- Influencers ask for an attribution link and the seller has nothing structured.
- The brand qualifies for Amazon Attribution and has not enrolled.
- Bonus: brands eligible for a Brand Referral Bonus on attributed sales (typically 5-10% depending on category).

## The framework. The Tag Taxonomy

Every attribution link is one combination of: source channel, campaign, content,
audience. Build the taxonomy first, then tag every link from it. Consistency is the
whole game.

| Layer | Examples |
|-------|----------|
| Source | tiktok, instagram, youtube, google, email, podcast, influencer |
| Campaign | spring2026launch, blackfriday, evergreen |
| Content | post1, post2, story, reel, video, dm |
| Audience | warm, cold, retargeting, influencerX |

A tag string like `tiktok_spring2026_reel_creatorA` is parseable in reporting and
groups properly. random tags do not.

## Step by step

1. **Collect inputs.** Brand, products, current external channels, creators or
   campaigns planned for the next 90 days.

2. **Define the taxonomy.** Lock the four-layer pattern above for the brand. Once
   set, do not deviate.

3. **Enroll in Amazon Attribution.** Brand Registered required. Free.

4. **Generate the attribution links** per source/campaign/content/audience combo.
   Amazon's Attribution tool produces the tagged URL.

5. **Set the reporting cadence.** Daily attention during a campaign, weekly
   roll-up. Watch click-through, detail page views, and Brand Referral Bonus
   accrual.

6. **Tie incentives to creators.** Influencer commission tied to attributed sales,
   not just clicks. Their link is unique by creator tag.

7. **Plan the optimization loop.** What is converting, double down. What is not,
   cut.

8. **Run the quality check**, then deliver.

## Output format

```
## Attribution Plan. [brand]

### Taxonomy
Source codes: [list]
Campaign codes: [list]
Content codes: [pattern]
Audience codes: [pattern]

### Planned links (next 90 days)
Source x Campaign x Content x Audience . tag string . destination ASIN
[example: tiktok_spring2026_reel_creatorA → ASIN]

### Reporting
Daily during active campaign
Weekly roll-up

### Creator incentive (if used)
[commission % tied to attributed sale, per-creator tag]
```

## Worked example

A brand running a TikTok influencer campaign with 6 creators. Taxonomy locked.
Each creator gets a unique link like `tiktok_spring2026_reel_creator[A-F]` to the
hero ASIN. Reporting setup. Week 1: creators C and E are converting 4x the rate of
A and B. Pivot more budget to creators C and E, drop A and B in week 2. Brand
Referral Bonus accruing at 10% on attributed sales adds back ~10% effective margin.
Without attribution, the seller would have run all 6 creators flat and never known
which to scale.

## Quality check

- The taxonomy is locked before any link is generated.
- Every link is built from the taxonomy, not ad-hoc.
- Amazon Attribution enrollment is confirmed (Brand Registered).
- Reporting cadence is set, daily during campaigns.
- Creator incentives are tied to attributed sales, not just clicks.

## Common mistakes

- **Untagged links.** Sending external traffic and never knowing what worked.
- **Ad-hoc tagging.** Each campaign with a different tag pattern, impossible to
  roll up.
- **Reporting after the campaign ended.** No time to optimize. daily reads during
  the campaign are the lever.
- **Skipping Brand Referral Bonus.** A free 5-10% back on attributed sales (rate varies
  by category), missed by sellers who never enrolled.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
