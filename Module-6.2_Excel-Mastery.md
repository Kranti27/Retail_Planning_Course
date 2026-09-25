# Module 6.2: Excel Mastery for Planning

> *"Amateurs use Excel to store data. Planners use Excel to build logical models that predict the future and allocate capital. If your hands leave the keyboard to touch the mouse, you are moving too slowly."*

**Semester:** 6 — The Data  
**Prerequisites:** Module 6.1 (Planning Analytics)  
**Estimated Study Time:** 6-7 hours  
**Level:** Core

---

## Executive Summary & Core Dilemma

**How do retail planners translate theoretical planning concepts (allocation, replenishment, OTB, inventory aging) into robust, error-free, and dynamic spreadsheet models that drive millions of Rupees in inventory decisions?**

For a retail planner, Microsoft Excel is not a spreadsheet; it is an Integrated Development Environment (IDE) for business logic. 

**The Planner's Excel vs. Standard Excel**
Standard Excel usage is characterized by ad-hoc calculations, messy data entry, hardcoded numbers inside formulas, merged cells for aesthetic appeal, and extensive use of the mouse. 
The Planner's Excel is a highly structured, architected environment built on strict principles of data separation, dynamic referencing, and computational efficiency. 

---

## The Architecture of a Good Planning Model

A professional planning file is never a flat sheet of mixed data and calculations. It is always separated into three distinct architectural layers:

1. **The Input Tab (The Database):** Where raw data lives. This could be DC Inventory exports, Store Sales downloads, or Master Data tables. This tab has zero calculations. It is raw, unformatted, and tabular. 
2. **The Calc Tab (The Engine):** Where the logic happens. This is where INDEX/MATCH, SUMIFS, and complex nested formulas reside. This tab pulls from the Input Tab, transforms the data according to business rules (like applying a weeks-of-supply target), and stages it for output.
3. **The Output Tab (The Dashboard):** What David or VP of Merchandising actually sees. This contains Pivot Tables, Heatmaps, Slicers, and highly formatted summaries. 

### The Cardinal Sin: Merged Cells
Planners *never* use merged cells. Merged cells break sorting, filtering, macro execution, and formula dragging. If you need a title to span multiple columns for aesthetic reasons, use "Center Across Selection" in the Format Cells menu, never Merge & Center.

### Keyboard over Mouse
A planner processes hundreds of thousands of rows of data daily. Relying on a mouse to scroll, highlight, or navigate is a critical bottleneck. Mastery requires internalizing keyboard shortcuts: `Ctrl + Arrow Keys` to jump across data blocks, `Ctrl + Shift + L` to toggle filters, `Alt + E + S` for Paste Special, and `F4` to toggle absolute and relative cell references.

---

## Structured Tables (Ctrl+T)

If you are referencing raw data, never use standard ranges like `A2:D5000`. Next week, when the dataset grows to 5001 rows, your formulas will miss the new data.

**The Solution:** Convert data into a Structured Table by pressing `Ctrl + T`.
- **Benefits for Planners:** 
  1. Formulas automatically expand when new data is pasted at the bottom.
  2. Formulas use readable syntax (e.g., `SUM(SalesTable[Revenue])` instead of `SUM(C2:C5000)`).
  3. No need to reference entire columns (like `C:C`), which slows down recalculation speeds.

---

## Power Query: The Data Pipeline

Before you can write a formula, you need clean data. At Aura Global Retail, you might have inventory data in SAP, sales data in a separate BI tool, and store grades in a local CSV. 

**Power Query** is Excel's built-in ETL (Extract, Transform, Load) tool. It replaces the tedious process of downloading, copying, pasting, and manually cleaning data every Monday morning.

### Key Power Query Tasks for Planners:
1. **Connecting to Data Sources:** Link directly to a folder. If you drop a new weekly sales CSV into that folder, Power Query will automatically append it.
2. **Transforming Columns:** Instantly change text dates ("2023-10-01") into true Excel dates, or split "SKU-Color" ("12345-BLU") into two distinct columns.
3. **Unpivoting Data:** Often, systems export data with dates across the columns (Jan, Feb, Mar). This is a "Pivot" structure and is useless for data modeling. Power Query's "Unpivot Other Columns" feature turns this into a flat, tabular format (Column 1: SKU, Column 2: Date, Column 3: Value).
4. **Loading to Data Model:** Load millions of rows directly into the Excel Data Model (Power Pivot) instead of the spreadsheet, bypassing the 1-million-row limit.

---

## The Calculations and Core Functions

### VLOOKUP is Dead; Long Live INDEX/MATCH and XLOOKUP
The VLOOKUP formula is a staple of beginner Excel users, but it is dangerous for planners. 
**Why VLOOKUP Breaks:** VLOOKUP requires a hardcoded column index number. If someone inserts a new column into the raw data, your formula silently returns the wrong data.

**The Solution: INDEX and MATCH**
INDEX/MATCH uses dynamic column finding.
**Syntax:** `INDEX(Return_Range, MATCH(Lookup_Value, Lookup_Range, 0))`

**The Modern Alternative: XLOOKUP**
**Syntax:** `XLOOKUP(Lookup_Value, Lookup_Array, Return_Array, [If_Not_Found])`
`XLOOKUP(A2, 'DC_Inv'!A:A, 'DC_Inv'!D:D, 0)` replaces `#N/A` errors with 0, which is crucial because a missing SKU in the DC means 0 stock, not an error.

### SUMIFS and COUNTIFS (The Allocation Engine)
SUMIFS is arguably the most important function for a retail planner. 
**Syntax:** `SUMIFS(Sum_Range, Criteria_Range1, Criteria1, Criteria_Range2, Criteria2, ...)`

In a real planning model, you do not hardcode criteria:
`SUMIFS(Sales_Data!E:E, Sales_Data!B:B, $A2, Sales_Data!C:C, C$1)`
*Note the strategic use of absolute referencing ($). $A2 locks the column so you can drag the formula right, C$1 locks the row so you can drag the formula down.*

---

## Dynamic Array Formulas

Modern Excel introduces Dynamic Arrays, allowing one formula to spill results into multiple cells. This replaces tedious Pivot Tables for quick reporting.

1. **UNIQUE:** Extracts a distinct list. `=UNIQUE(SalesTable[Store_Name])` instantly generates a list of stores without duplicates.
2. **FILTER:** Replaces the need for complex INDEX/MATCH arrays. `=FILTER(SalesTable, SalesTable[Category]="Cushions")` pulls the entire row of data only for Cushions.
3. **SORT & SORTBY:** `=SORT(UNIQUE(SalesTable[Store_Name]))` gives you an alphabetical, distinct list of stores.

*Use Case in Retail:* You can build a dynamic drop-down list of Store Grades that automatically updates if a new grade ("A+") is added to the master data.

---

## Goal Seek & Solver

Sometimes you know the result you want, but you don't know the input required to get there. 

### Goal Seek (Markdown Optimization)
You have a SKU with a current margin of 55%. You need to clear 1,000 units. You want to know exactly what discount percentage you can offer while maintaining a minimum category margin of 45%. 
- Set Cell: [Total Margin % Cell]
- To Value: 45%
- By Changing Cell: [Discount % Cell]
Goal Seek mathematically forces the discount cell to the exact maximum allowable markdown.

### Solver (OTB Constraints)
Solver is Goal Seek on steroids. It can handle multiple constraints. 
*Scenario:* You have $500,000 OTB. You must buy at least 500 units of Core Cushions, no more than 200 units of Fashion Throws, and maximize total projected margin. Solver will test thousands of purchasing combinations to find the exact PO quantities that fit all constraints.

---

## Data Validation & Conditional Formatting (Visualizing Vitals)

Data visibility is just as important as data accuracy. 

*Worked Example: Inventory Aging Heatmap*
In Module 3.1, we discussed aging inventory. You have a column showing 'Days on Hand' for 5,000 SKUs. You need the problematic SKUs to scream for attention.
1. Highlight the 'Days on Hand' column.
2. Home -> Conditional Formatting -> New Rule -> Formula: `=M2>180` 
3. Format -> Fill -> Red.
Now, any SKU sitting for more than 180 days automatically turns red. 

---

## Executive Perspectives

### How David Operates on Excel
David, Director of Planning, audits Excel models; he does not build them from scratch anymore. When a junior planner submits an allocation file, David checks for one specific crime: **Hardcoded numbers inside formulas**.
If David clicks a cell and sees `=SUM(A1:A10) * 1.05` (representing a 5% growth target), he will reject the file. That 1.05 is hidden. Next week, the target might be 8%, and the planner will forget where that 1.05 is buried. 
David demands that the 5% exists in a clearly labeled 'Inputs' cell (e.g., cell Z1 named 'Growth_Target'), and the formula reads `=SUM(A1:A10) * (1 + $Z$1)`. This is transparency.

### How Sarah Thinks About Excel Output
Sarah, VP of Merchandising, manages a $100 Million category. He does not care about your SUMIFS logic, your raw data dumps, or how elegant your nested IF statements are. 
He only looks at the **Output Tab**. 
Sarah needs the "Executive Summary." He wants high-level aggregates, clear variances to budget (Red/Green conditional formatting), and slicers so he can isolate performance by Region or Category. If Sarah has to scroll past row 50 to find the total, the model is poorly designed.

---

## Strategic Trade-Offs & Risk Matrices

| Decision | Option A | Option B | The Planner's Choice |
| :--- | :--- | :--- | :--- |
| **Handling Complex Logic** | **Nested IF Statements:** Writing a massive `=IF(..., IF(..., IF(...)))` formula. | **Helper Columns:** Breaking the logic into 3 separate columns on the Calc Tab. | **Helper Columns.** A 7-level nested IF is impossible to audit. Helper columns use slightly more file size but are infinitely easier for David to review. |
| **Referencing Data Ranges** | **Exact Ranges:** `A2:A5000` | **Structured Tables / Full Cols:** `Table[Col]` or `A:A` | **Structured Tables (Ctrl+T).** Retail data grows weekly. Hardcoding ranges leads to silent allocation errors. |
| **Handling Missing Data** | **Ignore #N/A:** Letting errors populate the sheet. | **IFERROR Wrapper:** `=IFERROR(XLOOKUP(...), 0)` | **IFERROR or Built-in Zeroes.** An `#N/A` in one cell will corrupt any `SUM` at the bottom of the column. Always handle expected errors gracefully. |

---

## Strategic & Operational Pitfalls

1. **The Hardcoding Sin:** Putting static numbers (like margins, growth rates, or store counts) directly into a formula instead of referencing an input cell.
2. **Circular References:** Creating a formula that refers back to its own cell. This breaks the calculation engine.
3. **File Bloat via Formatting:** Highlighting an entire row (16,000+ columns) or entire column (1M+ rows) to apply a yellow background. Only format the specific range holding data.
4. **Not Using Absolute Referencing ($) Correctly:** Copying a formula down a column and failing to lock the lookup table range.
5. **Averaging Averages:** Calculating the margin percentage for Store A (50%) and Store B (40%), and then writing `=AVERAGE(50%, 40%)` to get the total margin (45%). Always calculate aggregate metrics from total Rupees (Total Profit / Total Sales).

---

## Case Application & Discussion Questions

### 1. Power Query Unpivoting
You receive a CSV with the following structure:
| SKU | Store | Jan_Sales | Feb_Sales | Mar_Sales |
|---|---|---|---|---|
| CUSH-01 | MUM-01 | 150 | 120 | 180 |
| MUG-99 | DEL-05 | 45 | 50 | 60 |

Using Power Query, detail the exact clicks required to unpivot this data into three columns: [SKU, Store, Month, Sales_Qty]. 

### 2. Dynamic Array Implementation
Given this raw data table (`SalesData`):
| Date | Region | Category | Revenue |
|---|---|---|---|
| 01-Oct | North | Textiles | $15,000|
| 02-Oct | South | Hardgoods| $8,000|
| 03-Oct | North | Hardgoods| $12,000|

Write a single `UNIQUE` and `FILTER` formula combination that will output a list of only the Regions that sold "Hardgoods".

### 3. Goal Seek Application
You have the following model for SKU 'Velvet Throw':
- Current Inventory: 500 units
- Cost Price: $20 - Current Retail Price: $50 - Current Margin: 60%
- Proposed Discount %: 0%
- Formula for Projected Margin %: `=((Retail*(1-Discount)) - Cost) / (Retail*(1-Discount))`

You need to clear the inventory at exactly a 35% final margin. Detail the parameters you would enter into the Goal Seek dialogue box (Set Cell, To Value, By Changing Cell).

---

## Connection to Next Module

Now that we have mastered the computational engine of planning (Excel), we need to feed it accurate targets. In **Module 6.3: Planning Systems & Platforms**, we will learn how enterprise software handles what Excel cannot, and how the two systems integrate to drive the business.

**Next Module:** [Module 6.3: Planning Systems & Platforms](Module-6.3_Planning-Systems.md)

---

## Key Takeaways

1. **Excel is an IDE.** Build models with clear Input, Calculation, and Output architectures.
2. **Never use merged cells.** They destroy functionality and data integrity.
3. **Structured Tables (Ctrl+T) are mandatory.** They ensure dynamic range expansion as datasets grow.
4. **Automate pipelines with Power Query.** Stop manually pasting data; build connections to source files and automate cleaning steps.
5. **Use Dynamic Arrays.** Replace complex lookup arrays with FILTER, UNIQUE, and SORT for instant data segmentation.
6. **No hardcoding.** All variables (growth targets, margin minimums) must live in visible input cells, never buried inside formulas.
