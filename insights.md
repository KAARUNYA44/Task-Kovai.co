Actionable Insights (Expanded)
1. Local Route Demand Rising — Increase Fleet Availability

Observation:
Analysis of the Local Route data shows a clear upward trend in passenger counts over recent months. The ARIMA model’s 7-day forecast predicts approximately a 12–15% increase in daily ridership.

Evidence in Data:
The rolling mean and differenced trend line confirm consistent positive growth with low volatility.

Action:
Deploy additional buses during morning (7–10 AM) and evening (5–8 PM) rush hours to reduce congestion and improve punctuality on high-demand routes.

2. Light Rail Showing Consistent Demand — Maintain Current Scheduling

Observation:
Light Rail service exhibits a stationary pattern with minor fluctuations. The ARIMA(0,1,2) model shows minimal error and forecasts nearly flat growth.

Evidence in Data:
The ADF test after differencing indicated stationarity (p < 0.05). Forecast residuals hover near zero, confirming stability.

Action:
Continue current operations and maintenance schedules. Resource allocation can remain constant, focusing on service reliability rather than capacity expansion.

3. Rapid Route Experiencing Weekday Surges — Apply SARIMAX for Scheduling Optimization

Observation:
SARIMAX identified a strong weekly seasonality (s = 7), with passenger peaks occurring mid-week (Wednesday–Friday) and drops during weekends.

Evidence in Data:
Seasonal differencing improved the ADF statistic from -2.11 to -4.89 and reduced RMSE by 9%.

Action:
Add additional vehicles during high-demand weekdays. Use dynamic driver scheduling: fewer drivers on Mondays/Tuesdays and more on Thursdays/Fridays. Introduce predictive scheduling to anticipate mid-week congestion.

4. School Routes Are Stable but Time-Sensitive — Optimize Morning Start Times

Observation:
The School service shows a consistent flat trend with low variance, typical of academic calendar dependency.

Evidence in Data:
Forecasts show less than 3% week-to-week variance. No visible seasonality detected.

Action:
Maintain current service levels but use time-based optimization. Align first trip departures with actual school start times to reduce idle waiting time and fuel use.

5. Weekly Travel Cycle Identified — Use for Predictive Planning

Observation:
Aggregated data across all services revealed a recurring mid-week pattern with ridership peaking on Wednesdays and Thursdays.

Evidence in Data:
ACF and seasonal decomposition plots show clear periodicity at a lag of 7 days.

Action:
Integrate this insight into an automated scheduling system. For example, a dashboard could alert operations: “Expected peak tomorrow — deploy additional resources.” This real-time planning helps reduce passenger wait times and improve service reliability.

6. Overall Trend — Gradual Recovery Post-2021

Observation:
Compared with earlier data (2020–2021), total service counts have more than tripled by late 2023.

Evidence in Data:
Cumulative line chart shows sustained positive slope, suggesting recovery after the pandemic period.

Action:
Plan future expansions, such as adding new routes or increasing vehicle count, based on the sustained growth in demand, especially for Local and Rapid routes.