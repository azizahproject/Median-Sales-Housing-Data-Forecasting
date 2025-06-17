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

- **Declare α, β, and γ **:
  - α = 0.5
  - β = 0.5
  - γ = 0.5

- **Seasonal Index (Initial)**:  
  - Calculated from the **first full year (2012)** by dividing each month's value by the average of all 12 months in that year.

    <img width="135" alt="Image" src="https://github.com/user-attachments/assets/ac51ec8d-1cbd-4982-8526-46a7647252bf" />
  - Seasonal index for each month is stored for use in later calculations.

    <img width="708" alt="Image" src="https://github.com/user-attachments/assets/4a369a91-ef69-484f-98af-8d663e765f76" />

- **Initial Level (L13)** and **Initial Trend (T13)**:  
  - Set in **January 2013**:

    <img width="516" alt="Image" src="https://github.com/user-attachments/assets/8990ec0a-8b8a-4280-a385-135273f93b74" />

    <img width="707" alt="image" src="https://github.com/user-attachments/assets/9bb30b31-433c-4619-8659-5dfb6d489ca1" />


---

### 3. Calculating Seasonal Value (Jan 2013 - April 2025)

- Using seasonal formula:
  
  <img width="197" alt="Image" src="https://github.com/user-attachments/assets/2bfdc7ff-296a-4cf4-b2a9-07e3578a7ee8" />
  
  *Dropdown that formula until end the data (April 2025).*

---

### 4. Updating Level and Trend (Feb 2013 - April 2025)

- Level update:
  
  <img width="296" alt="image" src="https://github.com/user-attachments/assets/0eb21c69-bbdc-460c-baad-44cc1711ad15" />
  
  *Dropdown that formula until end the data (April 2025).*


- Trend update:
  
  <img width="163" alt="image" src="https://github.com/user-attachments/assets/2f7f4dab-5d77-4f98-bb49-0d5bfbe34459" />
  
 *Dropdown that formula until end the data (April 2025).*


---

### 5. Forecasting (Feb 2013 – April 2025)

- Forecast:
  
  <img width="297" alt="image" src="https://github.com/user-attachments/assets/3cb6c641-b1b5-49d4-8275-de8b669874ec" />

  *Dropdown that formula until end the data (April 2025).*


---

### 6. Extended Forecast (May 2025 – December 2025)

- Extended 8-month forecast:
  - \( \ell_t \), \( b_t \), and repeated seasonal pattern.

---

### 7. Calculating Forecast Error

- Column **Error**:
  
  <img width="161" alt="image" src="https://github.com/user-attachments/assets/4a5a4ff4-901f-4dbc-8820-6d6ce62a4a35" />

  *Dropdown that formula until end the data (April 2025).*

- Column **|Error|**

  <img width="89" alt="image" src="https://github.com/user-attachments/assets/1497653d-8534-4ae0-817c-d8c85606ad9f" />

  *Dropdown that formula until end the data (April 2025).*

  Mean Absolute Deviation (MAD):
  <img width="140" alt="image" src="https://github.com/user-attachments/assets/91981bd7-429b-49b4-9fc4-5f156afc0064" />

- Column **Error²**
  


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

