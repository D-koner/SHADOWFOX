# Intermediate Level — E-commerce Sales and Customer Analysis

## 1. Project Overview

This project focuses on analyzing e-commerce sales data to understand revenue trends, customer purchasing behaviour, product performance, and regional sales distribution.

The objective is to transform raw transaction data into meaningful business insights through data cleaning, exploratory data analysis (EDA), KPI calculations, data visualization, and recommendation-oriented reporting.

The project was developed using Python in Visual Studio Code (VS Code), with Pandas and NumPy for data processing and Matplotlib and Seaborn for visualization.

## 2. Objectives

The main objectives of this project are to:

- Clean and prepare raw sales transaction data for analysis.
- Calculate key business performance indicators (KPIs).
- Analyze monthly revenue trends and identify peak and low-performing periods.
- Examine customer purchasing frequency and repeat purchase behaviour.
- Identify products that contribute significantly to revenue.
- Compare revenue performance across countries.
- Present findings through structured datasets, charts, and business recommendations.
- Support data-driven business decision-making.

## 3. Tools and Technologies

| Tool / Library | Purpose |
|---|---|
| Python | Data analysis and processing |
| Visual Studio Code | Development environment |
| Jupyter Notebook | Interactive analysis and documentation |
| Pandas | Data cleaning, manipulation, aggregation, and analysis |
| NumPy | Numerical operations |
| Matplotlib | Data visualization |
| Seaborn | Statistical visualization |
| OpenPyXL | Reading Excel files |
| CSV / Excel | Data storage and exchange |
| Git and GitHub | Version control and project sharing |

## 4. Project Structure

```text
Intermediate Level/
│
├── KPIs/
│   ├── business_kpis.csv
│   ├── country_analysis.csv
│   ├── monthly_revenue.csv
│   └── product_analysis.csv
│
├── Intermediate_Level.ipynb
├── Raw_Sales.xlsx
├── cleaned_sales.csv
├── requirements.txt
└── README.md
```

### Folder and File Description

- **KPIs/** — Contains exported business metrics and analysis summaries.
- **business_kpis.csv** — Stores the calculated business performance indicators.
- **country_analysis.csv** — Contains country-wise revenue, order, and customer summaries.
- **monthly_revenue.csv** — Stores monthly revenue totals for trend analysis.
- **product_analysis.csv** — Contains product-level revenue, units sold, and order counts.
- **Intermediate_Level.ipynb** — Contains the Python code, data preparation steps, analysis, and visualizations.
- **Raw_Sales.xlsx** — The original Excel dataset used as the source for the analysis.
- **cleaned_sales.csv** — The processed sales dataset used for the analysis.
- **requirements.txt** — Lists the Python libraries required to reproduce the analysis.
- **README.md** — Documents the project, methodology, outputs, and conclusions.

## 5. Dataset Description

The project uses an e-commerce transaction dataset containing sales information at the invoice-line level.

The dataset includes fields such as:

| Column | Description |
|---|---|
| Invoice | Invoice or transaction identifier |
| StockCode | Product identifier |
| Description | Product description |
| Quantity | Number of units purchased or returned |
| InvoiceDate | Date and time of the transaction |
| Price | Price per unit |
| Customer ID | Customer identifier |
| Country | Country associated with the transaction |
| Revenue | Calculated transaction-line value |

The `Revenue` column is calculated as:

`Revenue = Quantity × Price`

The dataset is analyzed at the transaction-line level. An invoice can contain multiple product lines, so the number of rows should not be interpreted as the number of orders.

## 6. Data Cleaning and Preparation

Data cleaning was performed using Pandas to improve data consistency and prepare the dataset for business analysis.

The main steps included:

1. Loading the raw Excel dataset into a Pandas DataFrame.
2. Inspecting the dataset dimensions, column names, data types, and summary statistics.
3. Identifying missing values and duplicate records.
4. Removing exact duplicate rows.
5. Converting transaction dates to a consistent datetime format.
6. Converting quantity and price fields to numeric data types.
7. Converting customer identifiers to a suitable nullable integer type.
8. Removing records with invalid dates or missing required numerical values.
9. Calculating transaction-line revenue using quantity and unit price.
10. Creating a sales-only dataset by excluding non-positive quantities, non-positive prices, and invoices identified as cancellations according to the project filtering rules.
11. Exporting the processed sales data to `cleaned_sales.csv`.

### Data Handling Considerations

- The original dataset was preserved separately from the cleaned dataset.
- Negative quantities may represent returns and were excluded from the sales-only analysis rather than automatically being treated as positive sales.
- Records without customer IDs cannot be reliably attributed to individual customers and should be excluded from customer-level metrics.
- The sales-only dataset represents positive sales transactions under the defined filtering rules; it should not automatically be interpreted as net revenue after returns.
- Missing values and excluded records should be documented when reporting final results.

## 7. Key Performance Indicators (KPIs)

The following KPIs were calculated to summarize business performance.

### 7.1 Total Revenue

The sum of transaction-line revenue across the included sales records.

**Formula:**

`Total Revenue = Sum of Quantity × Price`

### 7.2 Total Orders

The number of distinct invoice identifiers in the sales dataset.

**Formula:**

`Total Orders = Number of Unique Invoice IDs`

### 7.3 Unique Customers

The number of distinct, identified customers represented in the sales records.

**Formula:**

`Unique Customers = Number of Distinct Customer IDs`

### 7.4 Total Units Sold

The total number of units represented by the included positive-quantity sales records.

**Formula:**

`Total Units Sold = Sum of Quantity`

### 7.5 Average Order Value (AOV)

The average sales revenue per distinct invoice.

**Formula:**

`AOV = Total Revenue / Total Orders`

### 7.6 Average Revenue per Customer

The average sales revenue associated with each identified customer.

**Formula:**

`Average Revenue per Customer = Identified-Customer Revenue / Unique Customers`

These metrics provide an overview of sales performance, customer activity, and transaction value.

## 8. Exploratory Data Analysis

The project examines business performance from four main perspectives.

### 8.1 Monthly Revenue Analysis

Monthly revenue is aggregated from transaction dates to identify changes in sales performance over time.

The analysis aims to identify:

- Highest and lowest revenue months.
- Monthly fluctuations in sales.
- Potential seasonal patterns.
- Periods that may require further business investigation.

**Business relevance:** Monthly revenue trends can support sales planning, inventory management, staffing decisions, and the evaluation of seasonal demand.

### 8.2 Customer Behaviour Analysis

Customer purchase frequency is calculated using the number of distinct invoices associated with each identified customer.

The analysis includes:

- Total identified customers.
- Customers with multiple purchases.
- Repeat purchase rate.
- Customer-level revenue contribution.
- Highest-revenue customers.

The repeat purchase rate is calculated as:

`Repeat Purchase Rate = Repeat Customers / Identified Customers × 100`

A repeat customer is defined as a customer with at least two distinct sales invoices during the observed dataset period.

**Business relevance:** These metrics can help identify customer purchasing patterns and opportunities for targeted retention campaigns. They do not independently establish long-term customer loyalty.

### 8.3 Product Performance Analysis

Product-level performance is evaluated using aggregated sales data.

The analysis includes:

- Total revenue by product.
- Total units sold by product.
- Number of distinct invoices containing each product.
- Top-performing products by revenue.

**Business relevance:** Product analysis can support inventory planning, product assortment decisions, and the identification of products that contribute substantially to revenue.

Revenue is not equivalent to profit. Product profitability cannot be determined without suitable cost or margin information.

### 8.4 Regional Performance Analysis

Sales performance is grouped by country to compare revenue contribution and transaction activity.

The analysis includes:

- Revenue by country.
- Number of distinct orders by country.
- Number of identified customers by country.
- Highest-revenue countries.
- Revenue concentration among leading countries.

**Business relevance:** Regional analysis can help identify important markets and areas for further investigation. Expansion recommendations should also consider delivery costs, demand, competition, and other market conditions.

## 9. Data Visualization

Charts are used to communicate analytical results in an accessible format.

The project includes or is designed to include the following visualizations:

1. **Monthly Revenue Trend** — A line chart showing revenue changes over time.
2. **Customers by Number of Orders** — A chart showing customer purchase frequency.
3. **Top 10 Products by Revenue** — A horizontal bar chart comparing product revenue.
4. **Top 10 Countries by Revenue** — A horizontal bar chart comparing regional performance.

These visualizations support trend identification, comparison, and business interpretation.

## 10. Business Insights and Recommendations

The final recommendations should be based on the actual numerical results produced by the notebook.

Potential recommendations to evaluate include:

| Analysis Area | Potential Business Action |
|---|---|
| Monthly revenue | Prepare inventory and staffing plans for consistently high-demand periods. |
| Repeat purchases | Test targeted customer follow-up campaigns and measure their effect on subsequent orders. |
| Customer revenue | Investigate purchasing patterns among high-value customers and evaluate retention opportunities. |
| Product performance | Monitor the availability of important revenue-generating products. |
| Regional performance | Investigate opportunities in underperforming markets using demand and cost information. |
| Revenue concentration | Assess the risks associated with dependence on a limited number of products, customers, or markets. |

These actions should only be presented as final recommendations when the analysis provides supporting evidence. Potential explanations for observed patterns should be distinguished from verified causes.

## 11. Limitations

The findings are subject to several limitations:

- Missing customer identifiers limit the completeness of customer-level analysis.
- Excluding returns and cancellations means the sales-only revenue measure may differ from net revenue.
- Revenue does not measure profitability because product costs and operating expenses are not included.
- The observed transaction period limits conclusions about long-term retention.
- Seasonal patterns cannot establish their underlying causes without additional information.
- Historical purchasing behaviour does not guarantee future customer activity.
- Country-level comparisons may be affected by differences in customer counts, order sizes, and operating costs.

These limitations should be considered before making business decisions based on the results.

## 12. How to Run the Project

### Prerequisites

Install Python and Visual Studio Code, then install the Python and Jupyter extensions.

### Step 1: Open the project

Open the `Intermediate Level` folder in VS Code.

### Step 2: Create a virtual environment

Run the following command in the VS Code terminal:

```bash
python -m venv .venv
```

Activate it on Windows PowerShell:

```powershell
.\.venv\Scripts\Activate.ps1
```

### Step 3: Install dependencies

```bash
python -m pip install -r requirements.txt
```

### Step 4: Open the notebook

Open `Intermediate_Level.ipynb` and select the `.venv` Python kernel.

### Step 5: Run the analysis

Execute the notebook cells in order, beginning with imports and dataset loading and continuing through data cleaning, KPI calculations, EDA, and exports.

Ensure that any dataset paths and output directories in the notebook match the current project structure.

## 13. Conclusion

This project demonstrates an end-to-end workflow for e-commerce sales analysis, from raw data inspection and preparation to KPI calculation and business-oriented exploration.

By examining revenue trends, repeat purchase behaviour, product performance, and regional differences, the analysis provides a foundation for evidence-based business recommendations.

The project emphasizes not only numerical summaries and charts but also the interpretation of results, documentation of assumptions, and recognition of analytical limitations.

## 14. Future Improvements

Potential extensions include:

- Customer segmentation using RFM (Recency, Frequency, Monetary) analysis.
- Cohort-based customer retention analysis.
- Month-over-month and year-over-year growth comparisons.
- Return and cancellation analysis.
- Profitability analysis when cost data becomes available.
- Interactive dashboards using Power BI or Tableau.
- Automated generation of summary reports.
- Publishing the completed project on GitHub with documented findings and visual outputs.

---

**Project Level:** Intermediate

**Project Domain:** Data Analytics / E-commerce Business Intelligence

**Environment:** Python, VS Code, Jupyter Notebook

**Primary Deliverable:** A cleaned sales dataset, KPI summaries, analytical notebook, visualizations, and business recommendations.

