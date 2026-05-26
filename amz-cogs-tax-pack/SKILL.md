---
name: amz-cogs-tax-pack
description: >-
  Produces a CPA-ready year-end COGS schedule for Amazon sellers from Inventory
  Valuation Report, Settlement reports, and supplier POs. Catches the ending
  inventory math errors that overstate taxable income by 8-15%. Use when a user
  asks about year-end taxes, COGS, inventory valuation, or "tax pack for my
  accountant". Trigger phrases: "year-end taxes", "COGS schedule", "inventory
  valuation", "FIFO LIFO Amazon", "tax pack for CPA". Works with zero tools.
metadata:
  author: Jay GPT Pro
  library: amazon-pro-skills
  version: "1.0"
---

# Year-End COGS Tax Pack

Every January, sellers scramble to hand the CPA a clean COGS schedule. The CPA
asks for ending inventory, the seller pulls a Manage Inventory snapshot from
March instead of the Inventory Valuation Report dated Jan 1, and the entire
return is now wrong. Sloppy ending inventory math is the single biggest reason
Amazon sellers overpay tax. A clean pack saves 8-15% on the federal bill for a
typical 7-figure seller.

## When to use this

- Year just ended and the CPA wants the books by Feb 15
- Switching CPAs and need to hand over a clean historical schedule
- Quarterly tax estimates and you want COGS dialed in
- Pre-acquisition cleanup. A buyer wants 3 years of audited COGS

## The framework. The Year-End COGS Pack

The pack has five tabs. They reconcile to each other, and the final number ties
to the Schedule C or 1120 line.

| Tab | Source | Output |
|---|---|---|
| 1. Inventory Valuation Summary | Inventory Valuation Report dated Jan 1 12:00am UTC | Ending units x landed cost per SKU |
| 2. COGS by SKU | Settlement Reports + cost ledger | Units sold x weighted-avg cost |
| 3. Write-down Candidates | Inventory Age Report + damaged/unfulfillable | Obsolete, damaged, 365+ aged |
| 4. Freight Allocation | Freight invoices + PO landed cost | Per-unit freight added to cost basis |
| 5. Reconciliation to Bank | Deposit summary + COGS + fees | Top to bottom tie-out |

Costing method must be consistent year over year. FIFO, LIFO, or Weighted Average.
Switching methods triggers a Form 3115 filing. Pick one and stay.

## Step by step

1. **Pull the Inventory Valuation Report.** Seller Central > Reports > Fulfillment
   > Inventory > Inventory Valuation Report. Date = January 1, 12:00 AM UTC of the
   new year. Do not use Manage Inventory. It updates live and is useless for tax.

2. **Pull all Settlement Reports for the tax year.** Reports > Payments > All
   Statements. Download every settlement that closed in the tax year. Sum unit
   sales per SKU.

3. **Pull Purchase Orders and freight invoices.** From the supplier portal or
   internal records. Calculate landed cost per SKU = unit cost + freight + duties
   + 3PL inbound prep.

4. **Calculate weighted-average cost per SKU.** (Beginning inventory value +
   purchases during year) divided by (beginning units + units purchased).
   Apply this to units sold for COGS.

5. **Identify write-down candidates.** Pull Inventory Age Report. Flag any SKU
   aged 365+ days, any unfulfillable inventory, any damaged units. Write down to
   net realizable value. This is a deductible expense, do not skip it.

6. **Reconcile.** Beginning inventory + purchases. COGS. write-downs = ending
   inventory. Ending inventory from this calc must match Tab 1 within 1%.

7. **Run the quality check**, then deliver to CPA as 5-tab Excel.

## Output format

```
## Year-End COGS Pack. [Tax Year YYYY]

**Tab 1 - Inventory Valuation Summary**
SKU | Units on hand Jan 1 | Landed cost | Ending inventory $
[rows]
TOTAL ENDING INVENTORY: $[X]

**Tab 2 - COGS by SKU**
SKU | Units sold | Weighted avg cost | COGS $
[rows]
TOTAL COGS: $[X]

**Tab 3 - Write-down Candidates**
SKU | Units | Reason | Original cost | NRV | Write-down $
[rows]
TOTAL WRITE-DOWN: $[X]

**Tab 4 - Freight Allocation**
PO# | SKU | Units | Freight $ | Per-unit allocation
[rows]

**Tab 5 - Reconciliation**
Beginning inventory (Jan 1 prior year): $[X]
+ Purchases (cost basis): $[X]
- COGS: $[X]
- Write-downs: $[X]
= Ending inventory: $[X]  ← must equal Tab 1 total
```

## Worked example

Seller has 47 active SKUs. Beginning inventory Jan 1, 2025 was $284,000.
Purchases during 2025 totaled $1,420,000 (landed). Settlement reports show
38,400 units sold. Weighted-average cost calculated per SKU sums to $1,512,000
COGS. Inventory Age Report flags 12 SKUs aged 400+ days, original cost $38,000,
NRV $9,500, write-down of $28,500. Ending inventory = 284,000 + 1,420,000.
1,512,000. 28,500 = $163,500. Inventory Valuation Report Jan 1, 2026 shows
$164,200. Reconciles within 0.4%. Pack delivered to CPA. The $28,500 write-down
alone saved $7,125 in federal tax at 25% effective.

## Quality check

- Inventory Valuation Report is dated Jan 1 12:00 AM UTC, not the day you ran it
- Costing method matches prior year (FIFO/LIFO/Weighted Avg)
- Freight is allocated to cost basis, not expensed separately
- Write-downs documented with photo or unfulfillable report screenshot
- Reconciliation Tab 5 ties to Tab 1 within 1%
- All amounts in USD, no marketplace currency mixed in

## Common mistakes

- **Using Manage Inventory snapshot.** It updates live. By March it is useless for Jan 1 ending inventory.
- **Expensing freight instead of capitalizing.** IRS requires freight in cost basis. Expensing it overstates COGS in year 1 and understates it in year 2.
- **Skipping write-downs.** Aged and damaged inventory is a real deduction. Most sellers leave $5,000 to $40,000 on the table.
- **Switching costing methods.** FIFO to Weighted Avg without Form 3115 is a red flag in an audit.
- **Mixing marketplace currencies.** UK, DE, JP sales must be converted at the appropriate FX rate per settlement, not year-end spot rate.

---

## Built by Jay GPT Pro

Part of **Amazon Pro Skills**. Production-grade skills for serious Amazon sellers.
Free and open. Built by Jay Margaliot.

I share a new AI play for Amazon sellers every week, free, in my WhatsApp group.
Join here: https://chat.whatsapp.com/ILX65p1yWcaIG3c9WGHpTY
