# Operations Analytics - Session 3: Forecasting with Trends and Seasonality

This session explains how to forecast demand when data contains **trends** or **seasonal patterns**, two common characteristics of real-world business data.

---

# 1. Trend and Seasonality

### Trend

A trend exists when data consistently increases or decreases over time.

**Examples**

* US retail sales generally increase over the years.
* E-commerce sales show a long-term upward trend.
* Yellowstone National Park visitors increased over decades.

### Seasonality

Seasonality occurs when patterns repeat at regular intervals.

**Examples**

* Diwali sales in India
* Thanksgiving sales in the US
* Chinese New Year sales
* Ski equipment sales during winter
* Airline passenger traffic during vacation months

A seasonal pattern repeats every year, quarter, month, week, etc.

---

# 2. Forecasting Data with Trends

Three approaches can be used:

1. Moving Averages
2. Linear Regression
3. Exponential Smoothing with Trend Adjustments

---

# 3. Why Moving Averages Fail with Trends

Moving averages work well for stationary data but perform poorly when trends exist.

### Increasing Trend Example

| Period | Demand |
| ------ | ------ |
| 1      | 10     |
| 2      | 20     |
| 3      | 30     |
| 4      | 40     |
| 5      | 50     |

### MA(2)

Forecast for Period 5:

[
(30+40)/2 = 35
]

Actual demand = 50

Forecast lags behind trend.

### MA(3)

[
(20+30+40)/3 = 30
]

Even further behind.

### MA(4)

[
(10+20+30+40)/4 = 25
]

Lag becomes worse.

### Key Insight

**The more observations included in a moving average, the greater the lag behind a trend.**

For increasing trends:

* Forecasts are too low.

For decreasing trends:

* Forecasts are too high.

---

# 4. Linear Regression for Trend Forecasting

A better method is fitting a straight trend line.

Regression model:

D_t=a+bt

Where:

* (D_t) = Forecast demand
* (a) = Intercept
* (b) = Slope (trend)
* (t) = Time period

---

# 5. Ordinary Least Squares (OLS)

OLS fits the line that minimizes forecast errors.

Specifically, it minimizes:

[
\text{Mean Squared Error (MSE)}
]

The fitted line becomes the best trend estimate.

---

# 6. Yellowstone National Park Example

Data:

* Annual visitors from 1904–2014
* Strong increasing trend

### 50-Year Trend Line

Using data from 1965–2014:

[
D_t=-53,525,580+28,248t
]

Forecast for 2017:

[
D_{2017}=3,450,636
]

Expected visitors:

**3,450,636 visitors**

---

### 30-Year Trend Line

Using data from 1985–2014:

[
D_t=-57,401,021+30,191t
]

Forecast for 2017:

[
D_{2017}=3,494,226
]

Expected visitors:

**3,494,226 visitors**

---

# 7. Understanding Seasonality

Seasonality is a recurring pattern.

Example:

| Season | Demand Pattern |
| ------ | -------------- |
| Winter | Low            |
| Spring | Moderate       |
| Summer | High           |
| Fall   | Moderate       |

National park visitors are much higher in summer than winter.

---

# 8. Multiplicative Seasonal Factors

Seasonal factors measure how strong a season is compared to average demand.

Notation:

[
C_i
]

Where:

* (C_i) = Seasonal factor for season i

### Interpretation

#### If

[
C_i=1.25
]

Demand is 25% above average.

#### If

[
C_i=0.75
]

Demand is 25% below average.

### Important Rule

Sum of all seasonal factors must equal the number of seasons.

Example:

4 seasons:

[
C_1+C_2+C_3+C_4=4
]

---

# 9. Four-Step Method for Seasonal Forecasting

---

## Step 1: Calculate Sample Mean

Use all observations.

Example dataset:

Average demand:

[
14.33
]

---

## Step 2: Calculate Seasonal Averages

Average all observations belonging to the same season.

### Fall

[
(16+15+14)/3=15
]

### Winter

[
(7+6+6)/3=6.33
]

Result:

| Season | Average |
| ------ | ------- |
| Fall   | 15      |
| Winter | 6.33    |
| Spring | 12      |
| Summer | 24      |

---

## Step 3: Calculate Seasonal Factors

Formula:

[
\text{Seasonal Factor}
======================

\frac{\text{Season Average}}
{\text{Overall Mean}}
]

### Fall

[
15/14.33=1.05
]

### Winter

[
6.33/14.33=0.44
]

### Spring

[
0.84
]

### Summer

[
1.67
]

Final Seasonal Factors:

| Season | Factor |
| ------ | ------ |
| Fall   | 1.05   |
| Winter | 0.44   |
| Spring | 0.84   |
| Summer | 1.67   |

Check:

[
1.05+0.44+0.84+1.67=4
]

---

# 10. Interpretation of Seasonal Factors

### Winter = 0.44

Demand is only:

44% of average demand.

### Summer = 1.67

Demand is:

167% of average demand.

Thus:

* Winter is weak.
* Summer is strong.

---

# 11. De-seasonalization

Remove seasonal effects from the data.

Formula:

[
\text{Deseasonalized Value}
===========================

\frac{\text{Original Observation}}
{\text{Seasonal Factor}}
]

Example:

If Winter demand = 7

and Winter factor = 0.44

[
7/0.44=15.91
]

Apply this to every observation.

Result:

A **de-seasonalized series** that behaves like stationary data.

---

# 12. Forecasting Seasonal Data

### Process

Step 1:
Create de-seasonalized series.

Step 2:
Forecast using a stationary-data method such as Moving Average.

Step 3:
Multiply by the appropriate seasonal factor.

---

# 13. Forecast Example

Forecast Winter 2015 using MA(4).

De-seasonalized values from 2014:

* 13.33
* 13.64
* 14.29
* 14.37

Average:

[
(13.33+13.64+14.29+14.37)/4
===========================

13.91
]

De-seasonalized forecast:

**13.91**

Winter seasonal factor:

[
0.44
]

Final forecast:

[
13.91\times0.44
===============

6.11
]

### Winter 2015 Forecast

**6.11**

---

# 14. Airline Load Factor Example

Data Source:
US domestic airline markets.

### Load Factor

[
\frac{\text{Passengers}}
{\text{Available Seats}}
]

Example:

80% Load Factor means:

80% of seats are occupied.

### Observations

* Airlines became more crowded over time.
* Data showed both trend and seasonality.

---

### Airline Seasonal Analysis

Sample Mean:

[
79.44
]

January Average:

[
72.6
]

January Seasonal Factor:

[
72.6/79.44
==========

0.91
]

June Average:

[
85
]

June Seasonal Factor:

[
85/79.44
========

1.06
]

This indicates:

* January demand below average.
* June demand above average.

After calculating all monthly factors:

* Seasonal factors sum to 12 (months).
* Data can be de-seasonalized and forecasted.

---

# Key Takeaways

1. Moving averages lag behind trends.
2. More periods in a moving average create greater lag.
3. Linear regression is preferred when a trend exists.
4. Regression model:

[
D_t=a+bt
]

5. OLS finds the best trend line by minimizing MSE.
6. Seasonality is a repeating pattern in demand.
7. Seasonal factors measure strength relative to average demand.
8. Sum of seasonal factors equals the number of seasons.
9. De-seasonalization removes seasonal effects.
10. Forecast seasonal data by:

    * De-seasonalizing
    * Forecasting
    * Re-applying seasonal factors
11. Short-term forecasts are generally more reliable than long-term forecasts.
12. Tracking forecast errors helps identify forecast bias and improve model selection.

Source:
