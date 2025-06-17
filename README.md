# Forecasting Median Sale Price of U.S. Housing Market Using Holt-Winters Method (Excel)

### 📋 Project Overview

This project focuses on time series forecasting of median sale prices in the U.S. housing market using the Holt-Winters method. The data was sourced from Redfin and analyzed using Microsoft Excel, with the aim of identifying future trends based on seasonal and trend components.

### 🔍 Objective

To forecast the median home sale prices and analyze patterns using Holt-Winters Triple Exponential Smoothing to support data-driven real estate insights.

### 📁 Project Structure

### 🛠️ Tools & File

- Microsoft Excel
- Holt-Winters Triple Exponential Smoothing
- Charting
File : [Median_Sales_Forecast.xlsx](https://github.com/azizahproject/Median-Sales-Housing-Data-Forecasting/raw/refs/heads/main/Median_Sales_Forecast.xlsx)

### 📈 Methodology

1. Seasonality Check: Analyzed for seasonal behavior (monthly data)  
2. Modeling: Applied Holt-Winters method using: Level (α), Trend (β), and Seasonality (γ).
3. Forecasting: Extended forecast 8 months ahead.
4. Evaluation: Compared forecast vs actual using MAPE.
5. Optimization: Used the **Solver tool** in Excel to optimize α, β, and γ parameters to minimize MAPE between forecast and actual values.

> 📎 *All formulas and forecasting logic were built entirely in Excel, including the Solver-based parameter tuning process.*
