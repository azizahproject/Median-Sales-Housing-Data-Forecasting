# Forecasting Median Sale Price of U.S. Housing Market Using Holt-Winters Method (Excel)

## 📋 Project Overview

This project focuses on time series forecasting of median sale prices in the U.S. housing market using the Holt-Winters method. The data was sourced from Redfin and analyzed using Microsoft Excel, with the aim of identifying future trends based on seasonal and trend components.

## 🔍 Objective

To forecast the median home sale prices and analyze patterns using Holt-Winters Triple Exponential Smoothing to support data-driven real estate insights.

## 🛠️ Tools & File

- Microsoft Excel
- Holt-Winters Triple Exponential Smoothing
- Charting

File : [Median_Sales_Forecast.xlsx](https://github.com/azizahproject/Median-Sales-Housing-Data-Forecasting/raw/refs/heads/main/Median_Sales_Forecast.xlsx)

## 📈 Methodology

1. Seasonality Check: Analyzed for seasonal behavior (monthly data).  
2. Modeling: Applied Holt-Winters method using: Level (α), Trend (β), and Seasonality (γ).
3. Forecasting: Extended forecast 8 months ahead.
4. Evaluation: Compared forecast vs actual using MAPE.
5. Optimization: Used the **Solver tool** in Excel to optimize α, β, and γ parameters to minimize MAPE between forecast and actual values.

> 📎 *All formulas and forecasting logic were built entirely in Excel, including the Solver-based parameter tuning process.*

## 🔍 Step-by-Step Implementation

This section explains the complete step-by-step implementation of the Holt-Winters method in Excel, from exploring the raw data to evaluating model performance.

---

### 1. Visualizing the Original Data

<img width="468" alt="Image" src="https://github.com/user-attachments/assets/7603d321-b984-4d7c-9065-c06a56a11139" />

- A line chart was created to observe the **median sale price** from January 2012 to April 2025.
- The chart shows both **upward trend** and **seasonal fluctuations**, indicating that the **Holt-Winters Triple Exponential Smoothing (Additive)** model is suitable for forecasting.

---

### 2. Initializing Values

- **Seasonal Index (Initial)**:  
  - Calculated from the **first full year (2012)** by dividing each month's value by the average of all 12 months in that year.

    <img width="255" alt="Image" src="https://github.com/user-attachments/assets/91603d7e-9e9b-4c20-8912-7b36b6997781" />
  - Seasonal index for each month is stored for use in later calculations.

    <img width="710" alt="Image" src="https://github.com/user-attachments/assets/3fd5bb0c-7f4d-42bc-afb2-2eb725b928ee" />

- **Initial Level (ℓ₀)** and **Initial Trend (b₀)**:  
  - Set in **January 2013**:
    <img width="515" alt="Image" src="https://github.com/user-attachments/assets/cc54f915-760e-45ed-9de4-954ba439b495" />
    <img width="709" alt="Image" src="https://github.com/user-attachments/assets/c3ad4769-7926-4f01-a7f0-d5885197614f" />

---

### 3. Calculating Seasonal Value (January 2013)

- Using the additive seasonal formula:  
  \[
  s_t = \gamma (y_t - \ell_t) + (1 - \gamma)s_{t-L}
  \]
- For January 2013, \( s_t \) is calculated using the initialized level.

---

### 4. Updating Level and Trend (February 2013)

- Level update:  
  \[
  \ell_t = \alpha (y_t - s_{t-L}) + (1 - \alpha)(\ell_{t-1} + b_{t-1})
  \]

- Trend update:  
  \[
  b_t = \beta (\ell_t - \ell_{t-1}) + (1 - \beta)b_{t-1}
  \]

- Seasonal update:  
  \[
  s_t = \gamma (y_t - \ell_t) + (1 - \gamma)s_{t-L}
  \]

---

### 5. Forecasting (Feb 2013 – April 2025)

- Forecast for \( m \) steps ahead:  
  \[
  \hat{y}_{t+m} = \ell_t + mb_t + s_{t-L+m}
  \]
- All values are calculated using Excel formulas applied row-by-row, including seasonal index wrap-around using `MOD`.

---

### 6. Extended Forecast (May 2025 – December 2025)

- Extended 8-month forecast beyond existing data using the latest known:
  - \( \ell_t \), \( b_t \), and repeated seasonal pattern.
- No actual values exist for this period — this is **pure forecast** for forward planning.

---

### 7. Calculating Forecast Error

- **Mean Absolute Percentage Error (MAPE)** was used to evaluate the model:  
  \[
  \text{MAPE} = \frac{1}{n} \sum_{t=1}^{n} \left| \frac{y_t - \hat{y}_t}{y_t} \right| \times 100\%
  \]

- Other errors (optional): MAE, RMSE.

---

### 8. Optimizing Alpha, Beta, Gamma

- **Excel Solver** was used to minimize MAPE by adjusting:
  - \( \alpha \): Level smoothing factor
  - \( \beta \): Trend smoothing factor
  - \( \gamma \): Seasonal smoothing factor

- Solver runs until the best parameter combination is found for **lowest possible error**.

---

> ✅ All computations were done in **Microsoft Excel**, using structured formulas, absolute cell referencing, and Solver for optimization.

