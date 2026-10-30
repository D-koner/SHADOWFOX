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

Add the screenshot folder only if you include dashboard screenshots.
Include the source dataset only when redistribution is permitted.

## How to Use

1.  Download `Superstore_Data_Analysis.xlsx` from this repository.
2.  Open it in Microsoft Excel.
3.  Review the `Data Cleaning Notes` and `Cleaned_Data` worksheets.
4.  Explore the `KPIs`, PivotTable analysis worksheets, and `Dashboard`.
5.  Refresh PivotTables if you modify the underlying data.

Some Excel features, including PivotCharts and slicers, may behave differently in spreadsheet applications other than Microsoft Excel.

# INTERMEDIATE LEVEL

# E-commerce Sales and Customer Analysis

A Python-based data analysis project completed as part of the ShadowFox Data Analyst internship task. The project explores sales trends, customer purchasing behaviour, product performance, and regional revenue using the Online Retail II dataset.

## Project Objectives

- Clean and prepare the raw transaction dataset.
- Calculate key business performance indicators (KPIs).
- Analyze monthly revenue trends and repeat purchases.
- Identify top-performing products and countries.
- Visualize business patterns and derive actionable insights.

## Tools Used

- Python
- Pandas and NumPy
- Matplotlib and Seaborn
- Jupyter Notebook in VS Code
- CSV and Excel

## Dataset

The dataset contains e-commerce transaction details, including:

`Invoice`, `StockCode`, `Description`, `Quantity`, `InvoiceDate`, `Price`, `Customer ID`, and `Country`.

A `Revenue` column is calculated using Quantity × Price.

Please ensure that sharing the original dataset is permitted before committing it to a public repository.

## Data Preparation

The data preparation workflow includes:

- Checking missing values and duplicate records.
- Converting date and numerical columns to appropriate data types.
- Removing exact duplicate records.
- Calculating transaction revenue.
- Excluding returns, non-positive sales quantities and prices, and cancellation invoices from the sales-only analysis.
- Exporting the processed dataset to CSV.

## KPIs

The project calculates the following KPIs:

- Total Revenue
- Total Orders
- Unique Customers
- Total Units Sold
- Average Order Value
- Average Revenue per Customer

## Analysis and Visualizations

The analysis covers:

1. Monthly revenue trends
2. Customer purchase frequency and repeat purchase rate
3. Top 10 products by revenue
4. Product revenue, units sold, and order count
5. Country-wise revenue and order performance
6. Revenue contribution from the top 10 countries

## Key Findings

The notebook generates numerical results to identify:

- Highest and lowest revenue months.
- Repeat customer purchasing behaviour.
- Products contributing the most revenue.
- Countries with the highest sales contribution.
- Potential opportunities for customer retention and business growth.

Final findings and recommendations should be based on the actual results generated by the notebook.

## Repository Contents

```text
SHADOWFOX/
└── Intermediate Level/
    ├── KPIs/
    │   ├── business_kpis.csv
    │   ├── country_analysis.csv
    │   ├── monthly_revenue.csv
    │   └── product_analysis.csv
    ├── Intermediate_Level.ipynb
    ├── Raw_Sales.xlsx
    ├── cleaned_sales.csv
    ├── requirements.txt
    └── README.md
```

## How to Use

1. Download or clone this repository.
2. Open the `Intermediate Level` folder in VS Code.
3. Install the required libraries using `pip install -r requirements.txt`.
4. Open `Intermediate_Level.ipynb` and select the appropriate Python kernel.
5. Run the notebook cells in order to reproduce the cleaning, analysis, and KPI calculations.
6. Review the exported CSV files in the `KPIs` folder.

**Note:** Revenue represents the included positive sales transactions under the project's filtering rules and may not equal net revenue after returns or profit after costs.


## Project Overview

The **HR Analytics Dashboard** is an interactive data analytics project developed using Microsoft Power BI as part of the **ShadowFox Data Analyst Internship – Advanced Level**.

The project analyzes employee attrition patterns and workforce characteristics using the IBM HR Analytics Employee Attrition dataset. It helps identify factors associated with employee turnover by examining departments, job roles, age groups, tenure, overtime, income, job satisfaction, and distance from home.

The dashboard provides interactive visualizations and detailed analysis to support data-driven HR decision-making.

## Objectives

- Analyze overall employee attrition and workforce distribution.
- Identify departments and job roles with higher attrition rates.
- Understand the relationship between overtime and employee attrition.
- Analyze attrition across different age and tenure groups.
- Explore income, education, job satisfaction, and distance-from-home patterns.
- Build an interactive dashboard for exploring HR workforce data.

## Dataset

**Dataset:** IBM HR Analytics Employee Attrition & Performance

**Records:** 1,470 employees

**Original features:** 35 columns

The dataset includes employee information such as:

- Age and Gender
- Department and Job Role
- Monthly Income
- Years at Company
- Job Satisfaction
- OverTime
- Distance From Home
- Education
- Attrition status

The dataset was cleaned and transformed using Power Query before dashboard development.

## Tools and Technologies

| Tool | Purpose |
|---|---|
| Microsoft Power BI | Dashboard development and visualization |
| Power Query | Data cleaning and transformation |
| DAX | Measures and KPI calculations |
| Microsoft Excel / CSV | Dataset inspection |
| Git and GitHub | Version control and project hosting |

## Data Cleaning and Transformation

The following operations were performed using Power Query:

1. Removed unnecessary columns such as EmployeeCount, StandardHours, and Over18.
2. Created an Attrition Flag column to represent employee attrition numerically.
3. Created Age Band categories.
4. Created Tenure Band categories.
5. Created Income Band categories.
6. Created Distance Band categories.
7. Created Promotion Gap Band categories.
8. Added numerical sort columns for categorical bands.
9. Checked column quality, missing values, and data consistency.

## Key Performance Indicators (KPIs)

The dashboard includes six primary KPI cards:

| KPI | Value |
|---|---:|
| Total Headcount | 1,470 |
| Attrition Count | 237 |
| Attrition Rate | 16.12% |
| Average Tenure | 7.01 years |
| Average Monthly Income | 6,504 |
| Average Job Satisfaction | 2.73 |

## Dashboard Structure

### Page 1 – Executive Overview

The Executive Overview provides a summary of employee attrition and workforce performance.

**Key visualizations:**

- Attrition Rate by Department
- Attrition Rate by Job Role
- Attrition Count by Age Band
- Attrition Count by Tenure Band
- Overtime vs Attrition
- Job Satisfaction vs Attrition

**Interactive filters:**

- Department
- Gender
- Job Level
- Business Travel

### Page 2 – Deep Dive / Drill-down

The Deep Dive page provides detailed analysis of factors associated with employee attrition.

**Key visualizations and features:**

- Decomposition Tree for analyzing Attrition Count
- Average Monthly Income by Education and Attrition
- Attrition Rate by Distance Band
- Employee Detail Table
- Job Role-based Drill-through
- Page Navigation and Back Button

## Key Insights

1. The organization has 1,470 employees, of whom 237 have left, resulting in an overall attrition rate of approximately 16.12%.
2. The Sales department has a higher attrition rate than Research & Development and Human Resources.
3. Employees working overtime have a substantially higher attrition rate than employees who do not work overtime.
4. Attrition patterns vary across age groups and tenure categories.
5. Attrition rates differ across job roles, making role-specific analysis important.

For detailed findings, recommendations, and numerical comparisons, refer to [`docs/insights.md`](docs/insights.md).

## Business Recommendations

Based on the analysis, the following actions can be considered:

- Investigate the reasons behind higher attrition in departments with elevated turnover.
- Review overtime frequency and workload distribution.
- Improve employee engagement and career development opportunities.
- Develop targeted retention strategies for higher-risk job roles.
- Monitor employee satisfaction and workforce retention indicators.

These recommendations are exploratory and should be validated with additional organizational information.

## Project Limitations

- The dataset is fictional and may not represent actual organizational workforce behavior.
- The dataset does not contain a suitable date column for time-series attrition analysis.
- The analysis identifies associations rather than proving causation.
- Additional employee feedback and organizational data would be required for deeper investigation.

## Project Folder Structure

```text
SHADOWFOX/
│
└── Advanced Level/
    │
    ├── Cleaned_Data.xlsx
    │
    ├── Dashboard.jpeg
    │
    ├── Deep Dive.pbix
    │
    ├── Executive Overview.pbix
    │
    ├── README.md
    │
    └── Raw_Data.csv
```

## How to Use the Project

1. Download or clone this repository.
2. Open `HR_Analytics_Dashboard.pbix` using Microsoft Power BI Desktop.
3. Navigate between the Executive Overview and Deep Dive pages.
4. Use the slicers to filter employee information.
5. Explore the Decomposition Tree to investigate attrition patterns.
6. Use Job Role drill-through to examine detailed employee records.

## Conclusion

This project demonstrates the use of data cleaning, transformation, DAX measures, interactive visualization, and analytical storytelling to investigate employee attrition.

It provides a structured approach to identifying workforce patterns and translating analytical findings into actionable HR recommendations.

---

**Project:** ShadowFox Data Analyst Internship – Advanced Level

**Domain:** Data Analytics | HR Analytics | Business Intelligence

**Tools:** Power BI | Power Query | DAX | GitHub

---

*Developed as part of the ShadowFox Data Analyst Internship Program.*

