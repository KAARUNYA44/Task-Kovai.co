
# Technical Report — ARIMA Model for Time Series Forecasting

## 1. Introduction
This project uses **ARIMA (AutoRegressive Integrated Moving Average)** modeling to forecast ridership across multiple transport services such as Local Route, Light Rail, and Rapid Route. The goal is to predict short-term demand and generate actionable insights for operational planning.

---

## 2. Why ARIMA?
ARIMA is ideal for **univariate time series forecasting** where data shows **trend but limited seasonality**. It models relationships between past values (AR), differenced values (I), and past errors (MA).

---

## 3. Model Selection Process
1. **Stationarity Test:** Used **ADF test** to check for stationarity.  
   - If `p-value > 0.05`, applied differencing (d=1 or d=2).
2. **Parameter Identification:** Used **ACF and PACF** plots to determine `p` and `q`.
3. **Model Fitting:** Trained ARIMA(p,d,q) for each variable.
4. **Evaluation:** Compared models based on AIC/BIC and forecast error metrics (MAE, RMSE).

---

## 4. Model Parameters Example (Local Route)
| Parameter | Description | Value |
|------------|--------------|--------|
| p | Auto-Regressive term | 1 |
| d | Differencing term | 1 |
| q | Moving Average term | 1 |
| AIC | Model Score | 231.45 |
| RMSE | Evaluation metric | 512.8 |

---

## 5. Forecasting & Visualization
Generated **7-day forecasts** for each service and visualized actual vs predicted values using matplotlib.  
Forecast confidence intervals show stable upward trends in Local and Rapid Routes.

---

## 6. Evaluation Metrics
| Metric | Formula | Purpose |
|--------|----------|----------|
| MAE | Mean Absolute Error | Measures average magnitude of errors |
| RMSE | Root Mean Square Error | Penalizes larger errors |
| MAPE | Mean Absolute Percentage Error | Provides percentage accuracy |

---

## 7. Conclusion
ARIMA performed well for short-term forecasting.  
For longer-term or strongly seasonal data, **SARIMA** or **Prophet** models can further improve accuracy.  

**Model Suitability:** ARIMA is the best choice for this dataset given its small size and moderate trend pattern.
