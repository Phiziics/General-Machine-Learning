# E-commerce A/B Testing with Revenue Forecasting

## Introduction

This project combines A/B testing, time series forecasting, machine learning, and scenario analysis into one business-focused workflow.

The goal is to evaluate whether an experimental variant improves purchase-related behavior, then translate that uplift into revenue forecasting scenarios using real store sales data.

## Business Problem

Companies often face two related questions:

1. Did the experiment improve performance?
2. If the experiment works, what does that imply for future revenue?

This project answers both questions by connecting experiment results to forecasted business impact.

## Datasets

### A/B Testing Dataset
Used to compare control and test performance across:
- impressions
- clicks
- add to cart
- purchases
- spend

### Store Sales Forecasting Dataset
Used to forecast future revenue using:
- historical sales
- promotions
- transactions
- oil prices
- holidays
- calendar effects

## Workflow

### Notebook 1
Data pull and validation

### Notebook 2
Exploratory data analysis

### Notebook 3
Feature engineering

### Notebook 4
Baseline and classical time series forecasting

### Notebook 5
Machine learning forecasting models

### Notebook 6
A/B statistical testing and scenario analysis

## Methods Used

### A/B Testing
- funnel comparison
- uplift calculation
- Welch t-tests
- p-value interpretation

### Forecasting
- naive baseline
- seasonal naive baseline
- moving average baseline
- SARIMAX
- Prophet
- tuned Prophet variants
- Linear Regression
- Random Forest
- XGBoost

### Feature Engineering
- calendar features
- lag features
- rolling statistics
- oil smoothing
- holiday flags

## Results

### Classical Forecasting
Prophet outperformed SARIMAX and the baseline models.

### Tuned Prophet
The multiplicative Prophet model achieved the strongest RMSE, while the default Prophet configuration remained strongest on MAE and MAPE.

### Key Modeling Insight
Weekly seasonality was strong, and residual analysis showed that peak-demand days remained the hardest periods to predict.

### A/B Testing
The experiment workflow produced purchase-related uplift metrics that were used to create conservative, base, and optimistic revenue scenarios.

## Business Outcome

This project translates experiment uplift into forecasted revenue planning cases:
- control
- conservative uplift
- base uplift
- optimistic uplift

This makes the analysis useful for rollout planning instead of stopping at experiment readout alone.

## Repo Structure

```text
revenue_forecasting/
├── data/
│   ├── 01-raw/
│   ├── 02-preprocessed/
│   ├── 03-features/
│   └── 04-predictions/
├── notebooks/
├── models/
├── reports/
└── README.md