# E-commerce A/B Testing with Revenue Forecasting

## Introduction

This project combines experimentation analysis and time series forecasting into one business-focused workflow.

The goal is to evaluate whether an A/B test variant improves purchase behavior, then translate that uplift into revenue forecasting scenarios using real store sales data. Instead of treating experimentation and forecasting as separate tasks, this project links them into one decision-support pipeline.

This project is designed to answer two connected business questions:

1. Did the experiment improve performance?
2. If the experiment works, what does that imply for future revenue?

---

## Project Objective

The project has two connected parts:

### A/B Testing Analysis
Evaluate whether the test variant performs better than the control variant using funnel metrics and statistical testing.

### Revenue Forecasting
Forecast future sales using historical store sales data, promotions, transactions, oil prices, holidays, and calendar effects.

### Scenario Translation
Use experiment uplift as an input into future revenue scenarios:
1. control
2. conservative uplift
3. base uplift
4. optimistic uplift

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
│   ├── 06_statistical_testing_and_ab_style_analysis.ipynb
│   └── 07_dashboard_and_business_recommendation.ipynb
│
├── src/
│   └── pipelines/
├── app/
├── tests/
├── models/
├── reports/
└── README.md