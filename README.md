# SHADOWFOX

# BEGINNER LEVEL
# Sample Superstore Data Analysis

An Excel-based data analysis project completed as part of the ShadowFox
Data Analyst internship task. The project explores sales, profit,
customer segments, product categories, discounts, regions, and shipping
performance using the Sample Superstore dataset.

## Project Objectives

-   Clean and organize the source dataset.
-   Calculate key performance indicators (KPIs).
-   Analyze sales and profitability using PivotTables.
-   Build an Excel dashboard with charts.
-   Summarize findings as business insights.

## Tools Used

-   Microsoft Excel
-   Excel Tables, formulas, PivotTables, PivotCharts, and dashboard
    formatting

## Dataset

The dataset contains order, customer, product, sales, discount,
shipping, and profit information. The main fields include:

`Order ID`, `Order Date`, `Ship Date`, `Ship Mode`, `Customer ID`,
`Customer Name`, `Segment`, `Country`, `City`, `State`, `Postal Code`,
`Region`, `Product ID`, `Category`, `Sub-Category`, `Product Name`,
`Sales`, `Quantity`, `Discount`, and `Profit`.

Please ensure that sharing the original dataset is permitted before
committing it to a public repository.

## Data Preparation

The workbook keeps the raw data separate from the cleaned data. The
cleaning workflow includes:

-   Reviewing repeated `Order ID` + `Product ID` combinations before
    deciding whether they are duplicates.
-   Checking date and numeric data types.
-   Reviewing blanks and inconsistent values in categorical fields.
-   Checking Postal Code formatting.
-   Adding helper columns for Order Year, Order Month, Ship Days, Profit
    Margin, and Discount Band.
-   Recording the cleaning steps in a Data Cleaning Notes worksheet.

## KPIs

The workbook calculates these KPIs:

-   Total Sales
-   Total Profit
-   Profit Margin
-   Total Orders (distinct Order IDs)
-   Total Quantity
-   Average Order Value
-   Average Discount

The current workbook results are approximately:

  KPI                           Result
  --------------------- --------------
  Total Sales             2,296,919.49
  Total Profit              286,409.08
  Profit Margin                 12.47%
  Distinct Orders                5,009
  Total Quantity                37,871
  Average Order Value           458.56
  Average Discount              15.62%

These values reflect the workbook version used for the analysis. Results
may differ if the dataset is updated or cleaned differently.

## Analysis and Visualizations

The workbook includes PivotTable-based analysis for:

1.  Monthly sales and profit trend
2.  Sales and profit by category
3.  Top and bottom sub-categories by profit
4.  Sales, profit, and margin by region
5.  Sales contribution by customer segment
6.  Top states by sales
7.  Sales, profit, and margin by discount band
8.  Order volume and average shipping days by ship mode

## Key Findings

Based on the current workbook:

-   Total sales are approximately 2.30 million, with total profit of
    approximately 286.4 thousand.
-   Technology has the highest total profit among the three main
    categories, followed by Office Supplies.
-   Furniture has a comparatively low profit margin.
-   The discount band above 20% records a negative aggregate profit in
    this analysis.
-   The West region has the highest sales, while the Central region has
    the lowest profit margin among the four regions.
-   Tables, Bookcases, and Supplies show negative profit in the
    sub-category analysis.

These are descriptive findings from the dataset; they do not by
themselves establish causation. Seasonal patterns should be verified by
comparing quarters across years.

## Repository Contents

Suggested repository structure:

``` text
shadowfox-superstore-data-analysis/
├── Superstore_Data_Analysis.xlsx
├── README.md
└── screenshots/
    └── dashboard.png
```

Add the screenshot folder only if you include dashboard screenshots.
Include the source dataset only when redistribution is permitted.

## How to Use

1.  Download `Superstore_Data_Analysis.xlsx` from this repository.
2.  Open it in Microsoft Excel.
3.  Review the `Data Cleaning Notes` and `Cleaned_Data` worksheets.
4.  Explore the `KPIs`, PivotTable analysis worksheets, and `Dashboard`.
5.  Refresh PivotTables if you modify the underlying data.

Some Excel features, including PivotCharts and slicers, may behave
differently in spreadsheet applications other than Microsoft Excel.

them for real business decisions.
