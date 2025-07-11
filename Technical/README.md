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
4. Evaluation: Compared forecast vs actual using RMSE.
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

- **Declare α, β, and γ**:
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

  <img width="340" alt="image" src="https://github.com/user-attachments/assets/7cc95fb2-1ca6-4f96-a5d4-956b532b784a" />

  *Dropdown that formula until end the data (December 2025).*


---

### 7. Calculating Forecast Error

- Column **Error**:
  
  <img width="161" alt="image" src="https://github.com/user-attachments/assets/4a5a4ff4-901f-4dbc-8820-6d6ce62a4a35" />

  *Dropdown that formula until end the data (April 2025).*

- Column **|Error|**

  <img width="89" alt="image" src="https://github.com/user-attachments/assets/1497653d-8534-4ae0-817c-d8c85606ad9f" />

  *Dropdown that formula until end the data (April 2025).*

  **Mean Absolute Deviation (MAD)**:
  
  <img width="157" alt="image" src="https://github.com/user-attachments/assets/f84e0e45-10f3-41ed-bdaa-f9141b97fc13" />

- Column **Error²**
  **Mean Squared Error (MSE)**:

  <img width="148" alt="image" src="https://github.com/user-attachments/assets/4122e714-78b1-4f35-a63b-90883ab05748" />

  **Root Mean Squared Error (RMSE)**:

  <img width="92" alt="image" src="https://github.com/user-attachments/assets/66a4592c-ae7a-4bfb-8512-0ca77dd41aef" />

  
- Column **Absolute %Error**

  <img width="221" alt="image" src="https://github.com/user-attachments/assets/1ecc9205-618a-42a9-8628-4f2250d0f728" />

  **Mean Absolute Percentage Error (MAPE)**:

  <img width="217" alt="image" src="https://github.com/user-attachments/assets/a475427d-c6f1-4f17-aee9-4bcc7f00d1b2" />

  

---

### 8. The Forecast Result

Using α, β, and γ:
- α = 0.5
- β = 0.5
- γ = 0.5

The forecast results are plotted below:

<img width="522" alt="image" src="https://github.com/user-attachments/assets/c94e95f8-0aab-42bb-ae62-66e559aa49c3" />

To evaluate the model’s performance, I calculated the errors between the actual and forecasted values from February 2013 to April 2025.

<img width="336" alt="image" src="https://github.com/user-attachments/assets/65176b32-a554-4154-aaac-d008f917a196" />

**📉 RMSE: 25342.07644**

Those errors indicates that while the model captures some trend and seasonality, there is room for improvement through parameter optimization.


---

### 9. Optimizing Alpha, Beta, Gamma

- **Excel Solver** was used to minimize RMSE by adjusting:
  - α: Level smoothing factor
  - β: Trend smoothing factor
  - γ: Seasonal smoothing factor

  <img width="960" alt="image" src="https://github.com/user-attachments/assets/397ea265-99e4-4a57-8b8d-9cf0f43f54c7" />

- Solver runs until the best parameter combination is found for **lowest possible error**.

  <img width="336" alt="image" src="https://github.com/user-attachments/assets/335d9cae-6d16-4881-885e-8b1fa6f4ffae" />

- The forecast results after optimizing are plotted below:

  <img width="523" alt="image" src="https://github.com/user-attachments/assets/ef4507c0-63a0-4fed-a161-e2b58bdb321f" />

### 10. Compare Acrual vs Forecasting vs Forecasting after Optimize

<img width="433" alt="image" src="https://github.com/user-attachments/assets/8c84c97d-fdb0-4039-b58f-c0a5402d8571" />

The comparison results show that the forecast after parameter optimization produces a smaller error. This is also reflected in the RMSE value, which decreased after tuning.

The Solver feature in Excel was particularly helpful in finding the optimal parameter values (alpha, beta, gamma) that minimized the forecasting error.

---

> ✅ All computations were done in **Microsoft Excel**, using structured formulas, absolute cell referencing, and Solver for optimization.

