# Excel Sales Data Cleaning

A beginner data-cleaning project: turning a messy sales table into an analysis-ready dataset using Excel.

## Problem
The raw sales data had inconsistent formats and quality issues that would break any analysis (wrong totals, failed lookups, duplicate columns). The goal was to clean it, document every change, and add a Revenue column for later analysis.

## Dataset
- Small practice dataset of 7 sales transactions
- Columns: Transaction_ID, Date, Customer_Name, Region, Product, Quantity, Price_GBP, Status
- Source: [add where the file came from]

## Issues found and how I fixed them

| Column | Issue | Fix |
|---|---|---|
| Date | Mixed formats (dd/mm/yyyy, m/d/yyyy, dd-Mon-yy), stored as text, one missing value | Converted to real dates, left the missing value blank |
| Customer_Name | Leading space, title and initial ("Mr. D. Brown"), "NA" value | TRIM; missing values labelled "Unknown" |
| Region | Inconsistent capitalisation ("manchester") | PROPER and TRIM |
| Product | Typo ("Moniter") | Find and Replace to "Monitor" |
| Price_GBP | Mix of text and numbers with £ signs and commas | Removed symbols, converted to numbers, formatted as £ |
| Status | Column duplicated | Verified both matched with EXACT, deleted one |

## New column
- **Revenue** = Quantity x Price_GBP

## Skills practised
TRIM, PROPER, SUBSTITUTE, VALUE, IF, EXACT, Find and Replace, number and date formatting, documenting data issues.

## Files
- `sales_raw.xlsx`: original data, never edited
- `sales_clean_v1.xlsx`: cleaned dataset, with an `Issues` sheet listing every change

## What I would do with more data
Apply the same cleaning rules to a larger real-world dataset, then build pivot tables and a one-sheet dashboard (revenue by region, product and month).

## Next steps
- [ ] Repeat the process on a larger UK retail dataset
- [ ] Re-do the cleaning in SQL and Python (Pandas) to compare approaches
- [ ] 
