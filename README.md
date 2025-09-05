# Instacart Customer Value Analysis

Exploring behavioral drivers of customer value using SQL and Python, with actionable insights for marketing and retention.

## Executive Summary

This project analyzes Instacart’s open dataset (~3M+ records) to understand what drives customer value. Using SQL for large-scale data extraction and Python for analysis/visualization, I demonstrate how basket size, order frequency, and reorder rate correlate with value, and identify heterogeneity.

Heterogeneity findings show multiple “pathways to value” (e.g., frequent small orders vs. infrequent large baskets), highlighting the need for segmentation rather than one-size-fits-all loyalty strategies, which could improve retention and lifetime value.

## Key Findings

* **Basket size**, **order frequency**, and **reorder rate** are all positively associated with customer value.
* **Heterogeneity is high** — customers achieve value through different behavioral patterns.
* Low-value clusters include one-off users with low reordering, while super-users show higher frequency, basket sizes and reorder rates (though with high variability)
* **Actionable insight**: Segmentation and tailored engagement would likely outperform generic incentives.

## Technical Highlights

* **SQL**: Data cleaning & transformation with CTEs, joins, aggregations. Worked with ~3M+ rows of transaction data efficiently
* **Python (Pandas, Matplotlib, Seaborn)**: Correlation analysis, exploratory visualizations, and feature engineering.
* **Scalability**: Efficiently handled millions of rows via DuckDB SQL integration.

## Repository Structure

```markdown
├── .gitignore
├── customer_value_exploration   # Jupyter notebook with step-by-step analysis
├── LICENSE
├── requirements.txt             # Python dependencies
└── README.md                    # Project overview
```

## Limitations & Future Work

This was an exploratory, correlational analysis. Limitations include:
* Lack of unit, spend and demographic data: 'value' was approximated by product counts, not revenue.
* Correlations don’t establish causality.

Next steps:
* Enrich dataset with spend/demographics for stronger metrics.
* Run clustering to identify behavioral customer segments.
* Build predictive models (e.g., regression, churn prediction).
* Time-series analysis to study customer lifecycle behavior.
