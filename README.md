# Sales-Forecast
# Time Series Analysis and Forecasting with ARIMA

## Overview
This project analyzes monthly sales data for **Furniture** and **Office Supplies** using time series analysis techniques. By leveraging ARIMA and its seasonal extension (SARIMAX), the project forecasts future sales, providing valuable insights to support inventory management and strategic planning.

## Key Features
- **Data Preprocessing & Exploration:**  
  - Loading and cleaning the dataset.
  - Converting date columns to datetime format.
  - Aggregating daily data into monthly sales.
  - Visualizing time series trends and seasonal components.

- **Stationarity Testing:**  
  - Performing the Augmented Dickey-Fuller (ADF) test.
  - Applying differencing when necessary to achieve stationarity.

- **Modeling & Forecasting:**  
  - Building ARIMA/SARIMAX models to capture both short-term dynamics and seasonal patterns.
  - Forecasting the next 12 months for each category.
  - Evaluating model performance using RMSE and diagnostic tests.

- **Business Insights:**  
  - Deriving actionable insights for inventory management.
  - Formulating sales strategies based on forecasted trends.
 
## ARMA Model Overview
The **ARMA(p, q)** model, which combines **Autoregressive (AR)** and **Moving Average (MA)** components, is defined as:

\[
Y_t = c + \sum_{i=1}^{p} \phi_i Y_{t-i} + \sum_{j=1}^{q} \theta_j \epsilon_{t-j} + \epsilon_t
\]

Where:
- \( Y_t \) is the time series at time \( t \).
- \( c \) is a constant term.
- \( \phi_i \) represents the coefficients of the **AR** terms.
- \( \theta_j \) represents the coefficients of the **MA** terms.
- \( p \) is the number of lagged values (**AR order**).
- \( q \) is the number of lagged error terms (**MA order**).
- \( \epsilon_t \) is white noise.

### ARIMA Model Extension
The **ARIMA(p, d, q)** model extends ARMA by including an **Integration (I)** term:

\[
(1 - B)^d Y_t = c + \sum_{i=1}^{p} \phi_i Y_{t-i} + \sum_{j=1}^{q} \theta_j \epsilon_{t-j} + \epsilon_t
\]

Where:
- \( d \) is the degree of differencing applied to achieve stationarity.
- \( B \) is the **backshift operator**, where \( B Y_t = Y_{t-1} \).

The **SARIMA (Seasonal ARIMA) model** extends ARIMA by adding seasonal components, making it useful for time series with repeating patterns over fixed intervals.
