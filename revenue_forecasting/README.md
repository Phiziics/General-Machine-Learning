# E-commerce A/B Testing with Revenue Forecasting

## Introduction

This project combines experimentation analysis and time series forecasting into one business-focused workflow.

The goal is to measure the impact of an A/B test on user purchase behavior, then connect that uplift to a revenue forecasting pipeline using real retail sales data. Instead of treating A/B testing and forecasting as separate exercises, this project links them into one decision-making system.

This project is useful because real companies often need to answer both of these questions:

1. Did the experiment improve performance?
2. If the experiment works, what does that imply for future revenue?

---

## Project Objective

The project has two connected parts:

1. A/B testing analysis  
   Evaluate whether the test variant performs better than the control variant using experiment funnel metrics.

2. Revenue forecasting  
   Forecast future sales using historical store sales data, promotions, transactions, oil prices, and calendar effects.

The final goal is to use experiment uplift as an input into future revenue scenario analysis.

---

## Datasets Used

### 1. A/B Testing Dataset
Used to analyze variant-level performance and estimate uplift.

Files:
- `control_group.csv`
- `test_group.csv`

Main fields include:
- spend
- impressions
- clicks
- searches
- view content
- add to cart
- purchases

### 2. Store Sales Forecasting Dataset
Used to build the revenue forecasting pipeline.

Files:
- `train.csv`
- `test.csv`
- `transactions.csv`
- `oil.csv`
- `holidays_events.csv`
- `stores.csv`

Main forecasting target:
- daily total sales

Supporting drivers:
- promotions
- transactions
- oil prices
- holidays
- calendar features

---

## Project Structure

```python
revenue_forecasting/
│
├── config/
├── data/
│   ├── 01-raw/
│   ├── 02-preprocessed/
│   ├── 03-features/
│   └── 04-predictions/
│
├── entrypoint/
├── notebooks/
│   ├── 01_data_pull_and_validation.ipynb
│   ├── 02_eda.ipynb
│   ├── 03_feature_engineering.ipynb
│   ├── 04_baseline_and_time_series.ipynb
│   ├── 05_ml_models.ipynb
│   ├── 06_ab_testing_and_scenario_analysis.ipynb
│   └── 07_dashboard_and_business_recommendation.ipynb
│
├── src/
│   └── pipelines/
├── app/
├── tests/
├── models/
├── reports/
└── README.md