<p align="center">
  <a href="https://www.kaggle.com/code/hassanjameelahmed/kingdom-holding-co-analysis-2010-2026" target="_blank">
    <img src="Kingdom Holding Company.png" alt="Kingdom Holding" alt="Kingdom Holding" width="600">
  </a>
</p>
<br>




# Product Requirements Document (PRD)

## Project Overview
This project focuses on the curation and documentation of the **Kingdom Holding Company** historical stock dataset. Kingdom Holding Company is a prominent Saudi Arabian conglomerate listed on the Saudi Stock Exchange (Tadawul). This dataset is optimized for Kaggle and is intended for financial analysts, data scientists, and machine learning enthusiasts interested in time-series forecasting, algorithmic trading, and market trend analysis.

---

## d. SEO-Optimized Project Name and Description
**Project Name:** Kingdom Holding Company Historical Stock Dataset (2010-2026)
**Description:** A comprehensive historical stock price dataset for Kingdom Holding Company (Tadawul: 4280), featuring daily trading data including Open, High, Low, Close prices, and Volume. Perfect for time-series forecasting, algorithmic trading models, and Middle Eastern market analysis.

---

## b. Dataset Columns and Specifications
The dataset consists of the following columns:
1. **Date:** The trading date (Format: MM/DD/YYYY).
2. **Close:** The closing price of the stock on the given trading day.
3. **High:** The highest price the stock reached during the trading day.
4. **Low:** The lowest price the stock reached during the trading day.
5. **Open:** The opening price of the stock at the beginning of the trading day.
6. **Volume:** The total number of shares traded during the day.

---

## c. Top 5 Kaggle Tags
1. `Finance`
2. `Stock Market`
3. `Time Series Analysis`
4. `Saudi Arabia`
5. `Investing`

---

## e. Dataset Coverage
**Coverage:** This dataset covers the daily trading metrics (Open, High, Low, Close, Volume) of Kingdom Holding Company's publicly traded shares over a 16-year period, representing the core trading activity of the company on the Saudi Stock Exchange.

---

## f. Temporal and Geospatial Scope
- **Start Date:** 03/04/2010 (MM/DD/YYYY)
- **End Date:** 01/29/2026 (MM/DD/YYYY)
- **Geospatial Scope:** Riyadh, Saudi Arabia (Market: Saudi Stock Exchange - Tadawul)

---

## g. Data Provenance
**Provenance:** The data originates from financial market aggregators tracking the Saudi Stock Exchange (Tadawul), specifically the ticker 4280.SR. 
**Transformations:** The raw data was compiled and transformed by formatting the date column into a standard MM/DD/YYYY format, aligning the chronological sequence, removing non-trading weekend/holiday data points, and saving the structured data into a standard CSV format for broad compatibility.

---

## h. Dataset Collecting Methodology
**Methodology:** The dataset was collected systematically via financial APIs or historical data extraction tools focused on global stock exchanges. The data extraction targeted end-of-day (EOD) summary statistics. Post-collection, the data underwent a verification process to ensure there were no structural errors, null rows, or mismatched columns, culminating in the final `Kingdom Holding Company.csv` file.

---

## i. Biggest Problems and Challenges
1. **Handling Market Anomalies:** Addressing extreme volatility, stock splits, or dividend distributions which can skew historical time-series data.
2. **Missing Data/Non-Trading Days:** Dealing with gaps in the data caused by weekends, national holidays, or unexpected market closures.
3. **Model Overfitting:** When using this data for forecasting, models can easily overfit to historical noise rather than learning underlying market signals.
4. **Macroeconomic Factors:** The stock price is heavily influenced by external factors (e.g., global oil prices, regional geopolitics) that are not captured within the dataset itself.

---

## j. Source of the Dataset
**Source:** Saudi Stock Exchange (Tadawul) / Yahoo Finance Historical Records.
**Link:** [Yahoo Finance - Kingdom Holding Company (4280.SR)](https://finance.yahoo.com/quote/4280.SR/history)

---

## k. Step-by-Step Problem Development
**Developing a Financial Forecasting Solution:**
1. **Data Ingestion & Inspection:** Import the CSV dataset and verify data types. Ensure the `Date` column is set as a datetime index.
2. **Data Cleaning:** Check for any missing (NaN) values or zero-volume days. Interpolate or forward-fill data if minor gaps exist due to reporting errors.
3. **Exploratory Data Analysis (EDA):** Visualize the closing price over time to identify long-term trends, seasonality, and structural breaks. Plot trading volume to correlate high-activity days with price shifts.
4. **Feature Engineering:** Generate new technical indicators such as Moving Averages (e.g., 50-day, 200-day SMA), Relative Strength Index (RSI), and MACD to provide machine learning models with momentum and trend context.
5. **Model Selection & Training:** Split the data sequentially into training and testing sets. Train time-series specific models like ARIMA/SARIMA, or deep learning models like LSTMs (Long Short-Term Memory networks) on the historical data.
6. **Evaluation & Strategy Formulation:** Evaluate the model's predictive accuracy using metrics like RMSE or MAPE. Finally, use the model's predictions to simulate a trading strategy, calculating potential ROI while factoring in risk management.
