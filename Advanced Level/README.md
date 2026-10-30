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
