# Operations Analytics - Session 2: Forecasting with Moving Averages and Forecast Error Measurement

Forecasting uses historical data to predict future demand and support better business decisions. This session focuses on descriptive statistics, moving averages, forecasting methods, and measuring forecast accuracy.

The foundation of forecasting begins with **descriptive statistics**. The two most important measures are the **sample mean** and **sample standard deviation**. The sample mean is the arithmetic average of all observations and represents the expected future demand. The sample standard deviation measures how much the demand varies around the average. In the demand dataset of 100 observations, the sample mean was **52.81** and the sample standard deviation was **13.73**.

To describe forecasts, a notation system is used. A forecast made in period *t* for a future period is represented as *F*. A **one-step-ahead forecast** predicts the next period’s demand, while a **multi-step forecast** predicts several periods into the future.

The session then introduces **stationary time series data**, where there is no noticeable trend or seasonal pattern. In stationary data, future observations resemble past observations. Demand can be viewed as a constant average value plus random variation. For such data, two common forecasting methods are Moving Averages and Exponential Smoothing.

The primary method discussed is the **Moving Average (MA)** method. A moving average forecast is simply the arithmetic average of the most recent *n* observations. For example, MA(10) uses the last 10 demand values to forecast the next period. As new data arrives, the oldest observation is removed and the newest observation is added, causing the averaging window to “move,” which gives the method its name.

Using the last 10 observations, the demand data produced a mean of **49.60** and a standard deviation of **10.28**. Using the last 20 observations, the mean became **51.95** and the standard deviation **9.62**. When demand is approximately normally distributed, the sample mean can be directly used for prediction. However, the standard deviation must be adjusted to account for forecasting uncertainty. This adjusted value becomes the predictive standard deviation used for future demand estimation. As more historical data becomes available, the adjustment becomes smaller, making predictions more reliable.

The Moving Average method has several advantages. It is easy to understand, simple to compute, and provides stable forecasts. However, it has limitations. It ignores older observations completely, assigns equal importance to all recent observations, and performs poorly when trends exist because forecasts tend to lag behind actual changes.

To overcome the equal-weight limitation, **Exponential Smoothing** is introduced conceptually. Unlike Moving Averages, it assigns greater weight to recent observations and lower weight to older ones, making forecasts more responsive to changes.

Since forecasts are rarely perfect, forecast accuracy must be measured. The session introduces three important error metrics:

* **MAD (Mean Absolute Deviation):** Average absolute forecasting error.
* **MSE (Mean Squared Error):** Average squared forecasting error.
* **MAPE (Mean Absolute Percentage Error):** Average percentage forecasting error.

Using MA(10), the results were MAD = **8.90**, MSE = **113.15**, and MAPE = **19.72%**. Using MA(20), the results improved to MAD = **7.66**, MSE = **92.61**, and MAPE = **17.29%**. Since all error measures decreased, MA(20) provided a better forecast for this dataset.

Finally, the session discusses **forecast bias**, which occurs when forecasts consistently overestimate or underestimate actual demand. Monitoring forecast errors helps identify such bias and choose the most appropriate forecasting model.
