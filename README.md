# Exploring Paths to Customer Value - A SQL-Driven Analysis Using Instacart Data
Challenging myself to perform analysis using SQL only. An exploratory analysis of shopping data showing multiple behavioural routes to high customer value. 

## Purpose:

This project was primarily a way to practice advanced analytics on a large, realistic dataset. Using Instacart’s open dataset (~3M+ records), I explored behavioural patterns related to customer engagement, and value proxies. All transformation from raw data to aggregated metrics was executed purely in SQL (visualisations in Python) using CTEs and efficient joins.

## Executive summary: 

Using product count / month (average products purchased per month) as a proxy for customer value, I show how basket size, order frequency, and reorder rate vary across users of different average monthly value. The analysis reveals distinct behavioural “pathways to value” - for example, frequent small orders vs. infrequent large baskets - emphasising the need for segmentation rather than generic retention strategies.

## Key Findings

* **Basket size**, **order frequency**, and **reorder rate** are all positively associated with customer value (average monthly products purchased)
* **Heterogeneity is high** - customers achieve value through different behavioral patterns.
* Low-value clusters include one-off users with low reordering, while super-users show higher frequency, basket sizes and reorder rates (though with high variability)
* **Practical implications**: Segmentation and tailored engagement would likely outperform generic incentives.

## Technical Highlights

* **SQL**: Data cleaning & transformation with CTEs, joins, aggregations. Worked with ~3M+ rows of transaction data efficiently
* **Python (Pandas, Matplotlib, Seaborn)**: Correlation analysis, exploratory visualizations.
* **Scalability**: Efficiently handled millions of rows via DuckDB SQL integration.

## Repository Structure

```markdown
├── .gitignore
├── LICENSE
├── README.md                    # Project overview
├── customer_value_exploration   # Jupyter notebook with step-by-step analysis
└── requirements.txt             # Python dependencies
```

## Limitations & Future Work

This was an exploratory, correlational exercise in SQL. Limitations include:
* Lack of unit, spend and demographic data: 'value' was approximated by product counts, not revenue.
* Correlations don’t establish causality.

Theoretical next steps for a full analysis:
* Enrich dataset with spend/demographics for stronger metrics.
* Run clustering to identify behavioral customer segments.
* Build predictive models (e.g., regression, churn prediction).
* Time-series analysis to study customer lifecycle behavior.

