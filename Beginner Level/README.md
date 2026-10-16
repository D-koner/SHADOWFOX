# Superstore Sales Analysis

An Excel-based retail sales analysis project completed for the ShadowFox
Data Analyst internship task. The project uses the Sample Superstore
dataset to examine sales trends, profitability, product categories,
regional performance, customer segments, discounts, and shipping
performance.

## Project Objectives

-   Clean and validate the dataset while preserving the raw data.
-   Calculate key performance indicators (KPIs).
-   Analyze sales and profitability using Excel PivotTables.
-   Build charts and a dashboard to communicate findings.
-   Document actionable business insights and recommendations.

## Dataset Overview

The commonly distributed Sample Superstore dataset covers orders from
2014 to 2017 and includes fields such as:

-   Order ID, Order Date, Ship Date, Ship Mode
-   Customer ID, Customer Name, Segment
-   Country, City, State, Postal Code, Region
-   Product ID, Category, Sub-Category, Product Name
-   Sales, Quantity, Discount, Profit

**Data note:** Confirm the exact row count in the final workbook. The
commonly distributed version contains 9,994 rows, but the working file
used during this project showed 9,993 records in some PivotTables. The
README should reflect the final cleaned workbook rather than assume a
row count.

## Tools Used

-   Microsoft Excel
-   Excel Tables and formulas
-   PivotTables and PivotCharts
-   Dashboard formatting and slicers (where configured)

## Data Cleaning

The workbook separates the original data from the cleaned data. The
cleaning workflow includes:

-   Reviewing repeated `Order ID` + `Product ID` combinations before
    removing any records.
-   Checking date and numeric data types.
-   Reviewing blanks and inconsistent values in Region, State, Category,
    and Sub-Category.
-   Checking Postal Code formatting and leading zeros.
-   Creating helper columns:
    -   Order Year
    -   Order Month
    -   Ship Days
    -   Profit Margin %
    -   Discount Band
-   Recording the process in a `Data Cleaning Notes` worksheet.

## Key Performance Indicators

The working workbook produced the following results:

  KPI                             Result
  --------------------- ----------------
  Total Sales             \$2,296,919.49
  Total Profit              \$286,409.08
  Profit Margin                   12.47%
  Distinct Orders                  5,009
  Total Quantity                  37,871
  Average Order Value           \$458.56
  Average Discount                15.62%

These figures are based on the working workbook used during analysis.
Recheck them against the final saved file before submission, especially
if the data has been updated or records were removed.

## Analysis and Visualizations

The Excel workbook includes PivotTable-based analysis for:

1.  Monthly sales and profit trends
2.  Sales and profit by category
3.  Top and bottom sub-categories by profit
4.  Sales, profit, and profit margin by region
5.  Sales contribution by customer segment
6.  Top states by sales
7.  Sales, profit, and profit margin by discount band
8.  Order count and average ship days by ship mode

## Key Findings

Based on the current working workbook:

-   Total sales are approximately \$2.30 million and total profit is
    approximately \$286.4 thousand.
-   Technology generated the highest total profit among the three main
    categories, followed by Office Supplies.
-   Furniture had a comparatively low profit margin.
-   The discount band above 20% recorded a negative aggregate profit in
    the analysis.
-   The West region recorded the highest sales and profit, while Central
    had the lowest regional profit margin.
-   Tables, Bookcases, and Supplies showed negative profit in the
    sub-category analysis.

These are descriptive observations from the current workbook. They do
not prove that discounts caused losses, and seasonal patterns should be
verified by comparing quarters across multiple years.

## Business Recommendations

1.  **Review Furniture profitability:** Investigate product costs,
    pricing, and discount levels for low-margin and loss-making
    sub-categories.
2.  **Review high-discount transactions:** Evaluate whether discounts
    above 20% are generating enough profitable sales, while accounting
    for product mix.
3.  **Build on strong categories:** Explore opportunities in Technology
    and Office Supplies while monitoring margins.
4.  **Investigate regional differences:** Examine why Central has a
    lower profit margin and identify practical improvements.
5.  **Validate seasonality:** Compare quarterly sales and profit across
    years before planning seasonal campaigns.
6.  **Monitor shipping performance:** Compare order volumes and average
    shipping days across ship modes.

## Repository Structure

Suggested structure:

``` text
SHADOWFOX/
├── README.md
│
└── Beginner Level/
    ├── Cleaned_Data.xlsx
    ├── Dashboard.png
    ├── Dashboard.xlsx
    ├── KPIs.xlsx
    ├── README.md
    └── Raw_Data.xlsx
```

Only include screenshots or additional data files that are actually
present in the repository. Before publishing raw data, confirm that
redistribution is permitted.

## How to Use the Workbook

1.  Download `Superstore_Data_Analysis.xlsx`.
2.  Open it in Microsoft Excel.
3.  Review the  `Cleaned_Data` worksheet.
4.  Explore the `KPIs`, PivotTable worksheets, and `Dashboard`.
5.  Refresh PivotTables after modifying the source data, if necessary.

PivotCharts and slicers may behave differently in spreadsheet
applications other than Microsoft Excel.

## Author

Dipayan Koner

## Analysis Date

October 2026

## Disclaimer

This project is intended for educational purposes. Findings are based on
the workbook's current data and should be validated before being used
for real business decisions.
