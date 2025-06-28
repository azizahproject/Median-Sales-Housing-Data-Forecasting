# 🏠Forecasting Median Sale Price of U.S. Housing Market Using Holt-Winters Method (Excel)

---

<img width="516" alt="image" src="https://github.com/user-attachments/assets/513133aa-cef4-4f7d-9fb9-89398d3b39cd" />

📁 Data Raw and Forecast

## 📌Project Background
I created this forecast as both a practice project and a portfolio piece to apply Time Series Analysis (Forecasting) skill. This project aims to forecast the median sales price of houses in the U.S. for the next 8 months. The goal is to provide insights that can assist homebuyers, real estate developers, or policymakers in making data-driven decisions based on housing market trends.

## 🔍Objective
The dataset provided by Redfin clearly exhibits both seasonality and trend over time. Therefore, the Holt-Winters Exponential Smoothing method was chosen, as it effectively accommodates both components in time series forecasting.

## 🧠 Methodology

Tool: Microsoft Excel

Model: Holt-Winters (Triple Exponential Smoothing)

Input: Monthly time series data of median housing prices

Forecast Horizon: 8 months (May 2025 to December 2025)


<img width="467" alt="image" src="https://github.com/user-attachments/assets/e3a1f2ee-1f5a-4282-9731-391b2b6b1b84" />


## 📊 Market Narrative & Insights

Based on monthly median sale price data, several consistent seasonal patterns and growth behaviors can be identified:

### 1. Lowest Prices at the Beginning of the Year
Each year, the housing market tends to see its lowest price points in **January**. This aligns with slower buyer activity during winter. However, January prices **increase year over year**, indicating long-term price growth in the housing market.

### 2. Annual Peak During Mid-Year
The **highest prices occur in June or July**, aligning with peak home-buying seasons. These mid-year highs are **consistently higher than the previous year**, confirming a strong upward trend in the market.

### 3. Year-End Recovery Pattern
Following a price drop after the summer months, prices usually **rebound by December**. Interestingly, **December prices are typically slightly higher than January of the following year**, suggesting strong momentum going into the next cycle.

### 4. Resilience During the COVID-19 Pandemic
Despite global uncertainty during **2020–2021**, home prices **did not decline**. Instead, they **continued to rise**, signaling the housing market's resilience—driven by tight supply, strong demand, and low mortgage rates.

---

## 💡 Conclusion

These trends reveal a clear pattern:  
- Early year = low prices  
- Mid-year = price peaks  
- End of year = recovery  

Understanding these patterns is essential when applying time series forecasting methods like Holt-Winters. The seasonal strength of the housing market provides a strong foundation for accurate forecasting and strategic decision-making for buyers, sellers, and investors alike.
