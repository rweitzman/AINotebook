# Gold Price Analysis & Forecasting Report

## 1. Introduction
This report provides an analysis and forecasting of gold prices using various statistical and machine learning models. The dataset spans from 1950 to the present, focusing on monthly gold prices.

This has been completely updated from module 17, as I have used a vastly different data set, which required a much different method of data exploration, etc, to be able to come to a conclusion as to what the forecasted price would be. 

## 2. Data Overview

### 2.1 Data Summary
- **Date Range:** From the earliest date in the dataset to the latest.
- **Shape of Data:** `70 x 2`.

### 2.2 Data Conversion
- **Date Conversion:** The 'Date' column was converted to datetime format and set as the index of the DataFrame.

### 2.3 Descriptive Statistics
- **Average Gold Price:** $416.56
- **25th Percentile:** $447.07
- **Maximum Price:** $1840.81

## 3. Exploratory Data Analysis

### 3.1 Visual Analysis
- **Boxplot by Year:** Shows the distribution of gold prices across different years.
- **Boxplot by Month:** Illustrates how gold prices vary by month.
- **Month Plot:** Provides a visual representation of gold prices over months since 1950.
- **Yearly Trend:** Plots the average gold price per year.
- **Quarterly Trend:** Displays the average gold price per quarter.
- **Decade Trend:** Illustrates the average gold price per decade.

### 3.2 Coefficient of Variation (CV)
- **High CV in 1978:** Approximately 25%, indicating high risk.
- **Low CV in 2020:** Around 5%, suggesting a more stable investment.

## 4. Forecasting Models

### 4.1 Model Comparison

#### 4.1.1 Linear Regression
- **MAPE:** `26.28%` (For the test data)
- **Plot:** Shows linear regression predictions against actual prices.

#### 4.1.2 Naive Prediction
- **MAPE:** `16.30%` (For the test data)
- **Plot:** Displays naive forecasts compared to actual prices.

#### 4.1.3 Simple Average
- **MAPE:** `71.81%` (For the test data)
- **Plot:** Shows simple average forecasts against actual prices.

#### 4.1.4 Moving Average
- **Models:** 2-point, 3-point, 5-point, and 7-point moving averages.
- **MAPE Values:**
  - 2-point: `4.13%`
  - 3-point: `5.35%`
  - 5-point: `9.38%`
  - 7-point: `9.59%`

#### 4.1.5 Simple Exponential Smoothing (SES)
- **Best Alpha:** 0.3
- **MAPE:** `16.25%` (For the test data)
- **Plot:** Shows SES predictions for different alpha values.

#### 4.1.6 Double Exponential Smoothing (DES)
- **Best Alpha:** 0.3
- **Best Beta:** 0.3
- **MAPE:** `7.76%` (For the test data)
- **Plot:** Illustrates DES predictions for optimal alpha and beta values.

#### 4.1.7 Triple Exponential Smoothing (TES)
- **Model Configuration:** Additive trend and seasonal components.
- **MAPE:** `10.37%` (For the test data)
- **Plot:** Demonstrates TES forecasts with appropriate seasonal adjustments.

### 4.2 Forecasted Prices
The following are the forecasted gold prices for the coming years:

| Date       | Forecasted Price |
|------------|-------------------|
| 2020-12-01 | $1277.52          |
| 2021-12-01 | $1386.67          |
| 2022-12-01 | $1422.54          |
| 2023-12-01 | $1443.25          |

## 5. Summary
### 5.1 Model Performance
- **Best Performing Model:** Based on the lowest MAPE.
- **Comparison:** An overview of which models performed better and why.

### 5.2 Recommendations
- **Investment Insight:** Based on the volatility (CV) and forecasting accuracy.
- **Model Selection:** Suggest the most reliable forecasting model for future gold price predictions.

link to Juypter notebook: [here](https://github.com/rweitzman/AINotebook/blob/main/Gold_prices_Time_series_Forecasting.ipynb)

