# Telco Customer Churn Analysis

Exploratory data analysis of a telecommunications company's customer base to understand why customers leave and which factors are most associated with churn.

## Overview

Customer churn is costly for subscription businesses. This project analyzes the Telco Customer Churn dataset to identify the customer segments, contract types, services, and billing patterns linked to higher churn, and turns the findings into practical retention recommendations.

## Dataset

The dataset is the IBM Telco Customer Churn sample dataset (file: `WA_Fn-UseC_-Telco-Customer-Churn.csv`), available publicly on Kaggle. Each row is a customer, and the columns fall into four groups:

- **Demographics:** gender, senior citizen status, partner, dependents
- **Services:** phone, internet, online security, streaming, tech support, and others
- **Account information:** contract type, payment method, monthly charges, total charges, tenure
- **Target variable:** Churn (Yes/No)

## Methodology

1. **Import libraries** and configure plotting defaults
2. **Load and explore** the data (shape, data types, unique values, summary statistics)
3. **Clean and preprocess**
   - Detected hidden missing values in `TotalCharges` (blank strings instead of nulls) and converted the column to numeric
   - Converted `SeniorCitizen` from 0/1 to No/Yes for consistency
   - Checked for duplicate rows and duplicate customer IDs
   - Dropped the customer ID column and created a tenure group feature
4. **Exploratory data analysis**
   - Target variable distribution
   - Univariate analysis of numerical and categorical features
   - Bivariate analysis: churn vs demographics, services, account information, and numerical features
   - Churn by tenure group
   - Correlation analysis
   - Revenue impact analysis and a summary dashboard
5. **Insights and recommendations**

## Key Findings

- Overall churn rate is about 26.5%.
- Contract type is the strongest factor: month-to-month customers churn at about 42.7%, compared with about 11.3% for one-year and about 2.8% for two-year contracts.
- Fiber optic customers churn at about 41.9%, compared with about 19.0% for DSL customers.
- New customers (0-12 months of tenure) churn at about 47.7%. Churned customers had an average tenure of about 18 months, versus about 38 months for retained customers.
- Churned customers pay more per month on average ($74.44 vs $61.27).
- Electronic check users show the highest churn among payment methods (about 45.3%); automatic payment methods are much lower.
- Customers with fewer additional services churn more.
- Senior citizens churn at about 41.7%, compared with about 23.6% for non-seniors.

## Recommendations

1. Introduce onboarding and engagement programs for customers in their first 12 months.
2. Offer incentives to move customers from month-to-month plans to longer contracts.
3. Investigate pricing and service quality for fiber optic plans.
4. Encourage automatic payment enrollment with discounts.
5. Bundle services such as security, backup, and support to increase retention.
6. Develop retention programs aimed at senior customers.
7. Proactively engage customers with high monthly bills.

## Tools

- Python
- pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

## How to Run

```bash
git clone https://github.com/mgxziq/telco-customer-churn-analysis.git
cd telco-customer-churn-analysis
pip install pandas numpy matplotlib seaborn jupyter
jupyter notebook Telco_Customer_Churn_Analysis.ipynb
```

Make sure `WA_Fn-UseC_-Telco-Customer-Churn.csv` is in the same folder as the notebook.

## Repository Structure

```
.
├── Telco_Customer_Churn_Analysis.ipynb
├── WA_Fn-UseC_-Telco-Customer-Churn.csv
└── README.md
```

## Author

Mohammed Akram Anwar
GitHub: [mgxziq](https://github.com/mgxziq)
