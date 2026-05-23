---
name: amz-international-listings
description: >-
  Manage Amazon listings across multiple marketplaces. Covers localization versus
  machine translation, localized keyword research, marketplace-specific pricing,
  Build International Listings (BIL), and keeping a multi-country catalog in sync.
  Use when a user asks about translating listings, localizing for another
  marketplace, BIL, syncing listings across countries, or managing a catalog in
  several Amazon stores. Trigger phrases: "international listings", "translate my
  listing", "localize listing", "BIL", "build international listings", "multi
  marketplace catalog". Works with zero tools.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# International Listings Manager

Once a brand sells in more than one country, the listings are a system, not a set of
copies. A translated listing is not a localized one. This skill localizes properly,
prices per market, and keeps the multi-country catalog in sync.

## When to use this

- A product is expanding into a new marketplace and needs a real localized listing.
- Existing international listings are machine-translated and convert poorly.
- A seller is deciding whether to use Build International Listings to sync the catalog.
- Prices or content have drifted out of sync across marketplaces.

## The framework. Translate, Localize, Tune

A listing crosses a border in three layers. most sellers stop after layer one and
wonder why it does not sell.

### Layer 1. Translate

Get the language correct and natural. machine translation is a draft, never the final
copy. A native speaker or a professional localizer must pass over it. Literal
translation produces copy that reads as foreign and quietly kills conversion.

### Layer 2. Localize

Adapt the listing to how that market actually shops.

- **Keywords.** Shoppers in the new market search different words. Redo keyword
  research in the local language. a translated keyword is often not the searched one.
- **Units and norms.** Metric versus imperial, local sizing, local date and voltage
  conventions, local spelling.
- **Images.** Text inside images must be in the local language. Some scenes and
  references do not travel and should be reshot.
- **Compliance text.** Local safety, labeling, and claim rules.

### Layer 3. Tune

Set the offer for the market.

- **Price** to the local market and its competition and fees, not by currency
  conversion of the home price.
- **Watch the local competitive set**, which differs from the home one.

## Build International Listings

BIL can replicate a source listing into target marketplaces and auto-translate and
auto-price by a rule. It is a real time saver for layer 1 and for price syncing, but
it does not do layer 2. Use BIL to create and keep listings in sync, then localize
the content and keywords by hand on top of it.

## Step by step

1. **Collect inputs.** The source listing and marketplace, the target marketplaces,
   whether BIL is in use, and the product category.

2. **Decide the creation method.** BIL for fast replication and price syncing, or
   manual creation. either way, layer 2 localization is still required.

3. **Run layer 1.** Flag any machine-translated copy as a draft that needs a native
   pass.

4. **Run layer 2.** Local keyword research, local units and norms, image text in the
   local language, local compliance text.

5. **Run layer 3.** Set local pricing from the local market, not from a currency
   conversion. Note the local competitive set.

6. **Set the sync rule.** Define what stays synced automatically (price rules, stock)
   and what must be maintained per market (localized copy and keywords).

7. **Run the quality check**, then deliver.

## Output format

```
## International Listing Plan. [product]

Source: [marketplace]   Targets: [marketplaces]
Creation method: [BIL / manual]

### Per target marketplace
Translate: [status, native pass needed?]
Localize: [keywords, units, image text, compliance]
Tune: [local price, local competitive set]

### Sync rules
Auto-synced: [what]
Maintained per market: [what]
```

## Worked example

A US seller expanding a backpack to Amazon UK and Germany.

UK: BIL replicates the listing and syncs price by a rule. Copy needs a native UK
pass for spelling and idiom. Keyword research redone in UK English, "rucksack" is a
real search term that the US copy never used.

Germany: full German localization, professional translation, German keyword research,
all image text in German, metric units, and a price set from the German competitive
set, not a euro conversion of the US price.

## Quality check

- Machine-translated copy is flagged as a draft requiring a native pass.
- Keyword research is redone in the local language, not translated from the source.
- Image text is localized, not left in the source language.
- Local pricing is set from the local market, not a currency conversion.
- The plan separates what BIL syncs automatically from what is maintained per market.

## Common mistakes

- **Machine translation as final copy.** Reads as foreign, converts poorly.
- **Translated keywords.** The literal translation of a keyword is often not what
  local shoppers type.
- **Currency-converted pricing.** The home price in euros ignores local fees,
  competition, and willingness to pay.
- **Image text left in English.** Infographic text in the wrong language signals a
  careless seller.
- **Assuming BIL localizes.** BIL replicates and translates. it does not do real
  localization.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. 50 production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
