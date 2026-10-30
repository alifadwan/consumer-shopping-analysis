# Consumer Shopping Analysis

## Project Overview

This project explores consumer shopping preferences and purchasing behaviour using **Microsoft Power BI**. It examines shopping preferences, shopping frequency, spending, income, age and technology-savviness across three preference groups: Store, Online and Hybrid.

This is a beginner data analytics portfolio project focused on data preparation, business-question analysis, DAX measures and dashboard development.

> **Dataset Note:** The workbook used for this project is a synthetic/dummy dataset. The findings describe only the records in this dataset and should not be treated as representative of real consumers.

## Dashboard Overview

![Consumer Shopping Analysis Dashboard](screenshots/06-Final%20Dashboard.png)

The final dashboard contains four KPI cards:

- Total Records
- Average Technology Savviness
- Average Monthly Online Orders
- Average Monthly Store Visits

It also contains six analytical visuals:

1. Shopping Preference Distribution
2. Average Spending: Online vs. In-Store
3. Average Monthly Shopping Frequency
4. Average Monthly Income by Shopping Preference
5. Average Technology Savviness by Shopping Preference
6. Average Age by Shopping Preference

## Business Questions

The analysis was guided by six business questions:

1. Which shopping preference is most common in the dataset?
2. How do average monthly online orders compare with average monthly store visits?
3. How does average technology-savviness score differ by shopping preference?
4. How does average recorded online spending compare with average recorded in-store spending?
5. Does average age differ across shopping preference groups?
6. How does average monthly income differ across shopping preference groups?

## Tools and Technologies

- **Microsoft Power BI** – Data modelling, DAX measures and dashboard development.
- **Power Query** – Data preparation, column selection and data quality checks.
- **DAX (Data Analysis Expressions)** – Calculations and aggregations for the dashboard.

## Data Preparation

The original Excel workbook contained 25 columns and 11,789 records.

Eight relevant columns were selected for the analysis:

| Column | Description |
|---|---|
| `age` | Consumer age |
| `monthly_income` | Recorded monthly income |
| `monthly_online_orders` | Number of monthly online orders |
| `monthly_store_visits` | Number of monthly physical store visits |
| `avg_online_spend` | Average recorded online spending |
| `avg_store_spend` | Average recorded in-store spending |
| `tech_savvy_score` | Technology-savviness score |
| `shopping_preference` | Preferred shopping method |

The selected columns were reviewed in Power Query, including their data types and column quality. The selected fields showed 100% valid values at the time of review.

## DAX Measures

Seven DAX measures were created for the analysis:

```dax
Total Records = COUNTROWS('Shopping Analysis')

Avg Online Orders = AVERAGE('Shopping Analysis'[monthly_online_orders])

Avg Store Visits = AVERAGE('Shopping Analysis'[monthly_store_visits])

Avg Online Spend = AVERAGE('Shopping Analysis'[avg_online_spend])

Avg Store Spend = AVERAGE('Shopping Analysis'[avg_store_spend])

Avg Tech Savvy Score = AVERAGE('Shopping Analysis'[tech_savvy_score])

Avg Monthly Income = AVERAGE('Shopping Analysis'[monthly_income])
```

## Key Findings

### 1. Shopping Preference Distribution

Store was the most common shopping preference, accounting for 10,244 records (86.9%).

- Store: 10,244 records (86.9%)
- Online: 1,176 records (10.0%)
- Hybrid: 369 records (3.1%)

### 2. Shopping Frequency

Average monthly online orders (24.7) were higher than average monthly store visits (9.5).

### 3. Technology Savviness

Online-preferring records had the highest average technology-savviness score, followed by Hybrid and Store.

- Online: 6.58
- Hybrid: 5.80
- Store: 5.40

The overall average technology-savviness score was approximately 5.53.

### 4. Spending Comparison

Average recorded in-store spending was slightly higher than average recorded online spending.

### 5. Age Comparison

Average age was relatively similar across the three shopping preference groups.

- Online: 49.79
- Store: 48.64
- Hybrid: 47.87

### 6. Monthly Income

Average recorded monthly income was highest among Hybrid-preferring records, followed by Store and Online.

## Limitations and Considerations

- The dataset is synthetic/dummy data and is not representative of the general population.
- Income and spending units and definitions have not been independently verified. No specific currency should be assumed.
- The dataset is heavily weighted towards Store preference (86.9%). Comparisons involving Online and Hybrid groups should be interpreted with this imbalance in mind.
- Averages are useful for comparing groups but do not show the full distribution of values.
- The findings describe patterns in the dataset and do not establish causation.
- Duplicate records were not conclusively ruled out because no confirmed unique consumer identifier was identified.

## Project Structure

```text
consumer-shopping-analysis/
│
├── Consumer Shopping Analysis.pbix
├── README.md
└── screenshots/
    ├── 01-Dataset.png
    ├── 02-Power Query Steps.png    
    ├── 03-Data Quality.png
    ├── 04-Report Starting Point.png
    ├── 05-Dashboard First Draft.png
    └── 06-Final Dashboard.png
```

The original Excel workbook should only be included in a public repository if its licence and redistribution terms permit it.

## Future Improvements

The current dashboard is considered the final version for this project. Further changes should only be made if a major issue is identified, such as an incorrect calculation, misleading visual or broken interaction.

Potential future enhancements include documenting the dataset source and licence, adding useful slicers if they fit the dashboard layout, and expanding the analysis with additional business questions.