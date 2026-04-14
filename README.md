# ADSP 31006 – Time Series Analysis and Forecasting

**University of Chicago**  
**Instructor:** Arnab Bose  
**Term:** Winter 2026  

**Team Members:** Arima Avengers 
- Arthur Acker  
- Aren Mizuno  
- Rohan Muralidhar  

---

## 📖 Overview
This repository contains my final project for *ADSP 31006: Time Series Analysis and Forecasting*, a course focused on modeling and forecasting time-dependent data using statistical and computational methods.

Time series analysis is both a science and an art of making informed predictions based on historical data. This course emphasized theoretical foundations of time series models, hands-on implementation in statistical software, and communicating results effectively to different audiences.

Key areas of focus included:
- Modeling temporal patterns such as trends, seasonality, and volatility  
- Applying statistical forecasting models to real-world data  
- Evaluating model performance and assumptions  
- Presenting analytical insights clearly and effectively  

---

## Final Project
**Description:**  
This project investigates whether incorporating macroeconomic indicators, market indices, and volatility modeling improves Bitcoin price forecasting compared to a univariate baseline.

We use daily Bitcoin price data (BTC-USD) along with financial and macroeconomic variables, including:
- SPY (S&P 500 ETF)  
- QQQ (Nasdaq-100 ETF)  
- Federal Funds Rate (DFF)  
- 10-Year Treasury Yield (DGS10)  
- CPI (inflation)  
- Unemployment Rate  

Data spans **2016–2026** and is sourced from financial APIs such as Yahoo Finance and FRED.

---

### Methodology (from `Bitcoin_TS_Final.Rmd`)

- Performed **data preprocessing and feature engineering**:
  - Log transformations and log-returns  
  - Differencing to achieve stationarity  
  - Forward-filling to align mixed-frequency data  

- Conducted **statistical testing**:
  - ADF and KPSS tests for stationarity  
  - ARCH tests for volatility clustering  

- Built and compared multiple forecasting models:
  - **SARIMA** (univariate baseline)  
  - **VAR** (multivariate relationships)  
  - **VAR + GARCH** (time-varying volatility)  
  - **BSTS** (Bayesian structural time series with trend and regressors)  

- Evaluated models using:
  - RMSE and residual diagnostics  
  - Out-of-sample forecasting (test period: mid-2025 → 2026)  

---

### Key Findings

- Bitcoin returns exhibit strong **volatility clustering**, validating GARCH modeling  
- **Macroeconomic variables did NOT significantly predict BTC returns** (no Granger causality)  
- Adding complexity (VAR + GARCH) did not improve forecasts without predictive signals  
- **BSTS significantly outperformed SARIMA**, reducing forecast error by ~56%  
- BTC appears largely driven by **crypto-specific dynamics**, not traditional macro factors  

---

### Project Deliverables

- `Bitcoin_TS_Final.Rmd`  
  → Full R-based analysis including data processing, modeling, and evaluation  

- `Bitcoin_TS_Final.pptx`  
  → Presentation summarizing methodology, results, and insights (used for final class presentation)  

---

## Skills & Concepts Demonstrated

- Time series modeling: **ARIMA, SARIMA, VAR, GARCH, BSTS**  
- Financial data analysis and volatility modeling  
- Stationarity transformations (log returns, differencing)  
- Statistical testing (ADF, KPSS, ARCH)  
- Multivariate time series analysis  
- Forecast evaluation (RMSE, residual diagnostics)  
- Working with real-world financial and macroeconomic datasets  
- Communicating technical insights through data visualization and presentations  

---
