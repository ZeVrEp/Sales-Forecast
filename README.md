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
 
  - ## ARIMA Model Overview
**ARIMA** stands for *Autoregressive Integrated Moving Average* and is denoted as ARIMA(p, d, q):

- **p:** Order of the Autoregressive (AR) component.
- **d:** Degree of differencing needed for stationarity.
- **q:** Order of the Moving Average (MA) component.

### ARIMA Model Formula
The general ARIMA(p, d, q) model is given by:
\[
\phi(B)(1 - B)^d y_t = \theta(B) \epsilon_t
\]
Where:
- \( y_t \) is the observed time series at time \( t \).
- \( B \) is the backshift operator.
- \( \phi(B) = 1 - \phi_1 B - \phi_2 B^2 - \dots - \phi_p B^p \) represents the AR component.
- \( \theta(B) = 1 + \theta_1 B + \theta_2 B^2 + \dots + \theta_q B^q \) represents the MA component.
- \( \epsilon_t \) is white noise.
