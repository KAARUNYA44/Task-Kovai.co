# Transport Service Forecasting — Time Series Analysis (ARIMA & SARIMAX)

## Project Overview
This project performs **time-series forecasting** and **data analysis** on transportation ridership data across:
- Local Route  
- Light Rail  
- Peak Service  
- Rapid Route  
- School  

The goal is to forecast the **next 7 days** of demand using **ARIMA** and **SARIMAX** models and generate **actionable insights** for transport planning.

---

## Objectives
1. **Data Analysis & Insights** – Identify patterns, trends, and anomalies in transport ridership.  
2. **Forecasting** – Predict short-term (7-day) ridership for all service types.  
3. **Model Comparison** – Evaluate **ARIMA vs SARIMAX** performance on trend and seasonal data.  
4. **Visualization & Reporting** – Create interpretable visualizations and concise insight reports.  

---

## Tech Stack
- **Language:** Python  
- **Libraries:** pandas, numpy, matplotlib, statsmodels, pmdarima  
- **Models:** ARIMA & SARIMAX (Seasonal ARIMA with Exogenous Variables)

---

## Methodology
1. **EDA & Cleaning:** Handle missing values, fix date format, remove outliers.  
2. **Stationarity Check:** Verify with Augmented Dickey-Fuller (ADF) test.  
3. **Differencing:** Apply differencing to make series stationary.  
4. **Parameter Selection:** Use **ACF/PACF** to determine ARIMA `(p,d,q)` and SARIMAX seasonal `(P,D,Q,s)` parameters.  
5. **Model Fitting:** Train both **ARIMA** and **SARIMAX** models for each service.  
6. **Forecasting:** Generate 7-day predictions with 95% confidence intervals.  
7. **Evaluation:** Compute MAE, RMSE, and MAPE to assess accuracy.  
8. **Visualization:** Plot forecast vs actual data and highlight trends.  

---

## Model Selection Summary
| Model | Use Case | Strength |
|--------|-----------|-----------|
| **ARIMA** | Non-seasonal ridership data | Simple and effective for short-term trends |
| **SARIMAX** | Seasonal or cyclic demand (e.g., weekly patterns) | Captures trend + seasonality, more robust for recurring demand |

---

## How to Run

### Step 1: Clone Repository
```bash
git clone https://github.com/<your-username>/transport-forecast.git
cd transport-forecast

###Step 2: Install Dependencies
pip install -r requirements.txt

###step 3:Run Notebook

Launch Jupyter Notebook:
jupyter forecast.ipynb