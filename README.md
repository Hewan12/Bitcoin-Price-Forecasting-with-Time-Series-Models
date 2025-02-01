# Bitcoin Price Forecasting with Time Series Models

## Overview

This project aims to forecast Bitcoin prices using various time series models, including ARIMA, SARIMA, and LSTM (Long Short-Term Memory). The goal is to evaluate and compare the performance of these models based on their RMSE (Root Mean Square Error) values, with a focus on achieving accurate price predictions.

## Table of Contents

- [Overview](#overview)
- [Models Used](#models-used)
   - [LSTM](#lstm)
   - [ARIMA](#arima)
   - [SARIMA](#sarima)
- [Dataset](#dataset)
- [Evaluation Metrics](#evaluation-metrics)
- [Results](#results)
- [Visualizations](#visualizations)
- [Contact](#contact)

## Models Used

### LSTM

LSTM (Long Short-Term Memory) is a type of Recurrent Neural Network (RNN) designed to learn and remember long-term dependencies in data. It is particularly useful for capturing complex, nonlinear patterns in time series data.

**Model Specifications:**
- LSTM is highly effective for time series forecasting tasks where long-term dependencies and nonlinear patterns are present.
- The model can handle sequential data and learn complex relationships between past and future values, which is often seen in financial time series like Bitcoin prices.

### ARIMA

ARIMA (AutoRegressive Integrated Moving Average) is a classical statistical model used for forecasting time series data. It is particularly effective for non-seasonal data that shows a linear trend.

**Model Specifications:**
- ARIMA is suitable for univariate time series data that exhibits clear trends and no seasonal variations.
- The model assumes stationarity in the data, meaning the properties of the data do not change over time.

### SARIMA

SARIMA (Seasonal ARIMA) extends ARIMA by adding seasonal components, making it suitable for time series data with seasonal patterns.

**Model Specifications:**
- SARIMA is ideal for data that exhibits both trends and seasonality.
- The model incorporates seasonal differencing, seasonal AR and MA terms, and seasonal periodicity to account for seasonal variations.
  
## Dataset

The dataset used in this project contains historical Bitcoin price data, with features like the closing price, date, and trading volume. The data was sourced from a publicly available Bitcoin price dataset on Kaggle and spans several years.

**Dataset Characteristics:**
- **Source:** [Kaggle: Bitcoin Historical Data](https://www.kaggle.com/datasets/mianbilal12/bitcoin-historical-data)
- **Features:** Date, Open, High, Low, Close, Volume, Market Cap
- **Time Period:** The dataset includes daily Bitcoin prices from 2014 to 2024.
- **Size:** The dataset contains over 3,725 data points, corresponding to daily prices over a period of 10 years.

**Preprocessing Steps:**
- The dataset is cleaned by removing missing or erroneous values.
- The features are normalized to ensure better performance of the LSTM model.
- Data is split into training (95%) and testing (5%) sets for model evaluation.

## Evaluation Metrics

To evaluate the performance of the models, we used the **Root Mean Square Error (RMSE)**, a common metric for measuring the accuracy of regression models. RMSE measures the average magnitude of the errors between predicted and actual values.

**Formula:**
\[
RMSE = \sqrt{\frac{1}{N} \sum_{i=1}^{N} (y_i - \hat{y}_i)^2}
\]
Where:
- \( y_i \) is the actual value
- \( \hat{y}_i \) is the predicted value
- \( N \) is the total number of predictions

## Results

### RMSE Values:
- **LSTM RMSE:** 2277.43 (lowest error and highest prediction accuracy)
- **ARIMA RMSE:** 9652.53 (higher error than LSTM)
- **SARIMA RMSE:** 10035.62 (highest error among the three)

### Model Comparison:
- **LSTM** provides the most accurate forecast, with the lowest RMSE value, indicating it outperforms both ARIMA and SARIMA.
- **ARIMA** and **SARIMA** have higher RMSE values, suggesting that they are less effective at capturing the complex, nonlinear patterns present in Bitcoin price data.

## Visualizations

The following visualizations are included in the project:

- **Heatmaps for Confusion Matrices**:
  - These heatmaps visualize the performance of the models by showing the confusion matrices. The color intensities indicate the number of correct and incorrect predictions made by the models. You can assess model accuracy by looking for high values along the diagonal (correct predictions) and low values in off-diagonal cells (incorrect predictions).

- **LSTM Model**:
  - This plot compares the predicted Bitcoin prices from the LSTM model with the actual prices from the test data. By examining this visualization, we can see how closely the model's forecast matches real price movements over time. The closer the predicted values are to the actual values, the better the model's performance.

- **ARIMA Forecast vs Actual Prices**:
  - This plot compares the predicted Bitcoin prices from the ARIMA model with the actual prices. Similar to the LSTM plot, we can evaluate the accuracy of the ARIMA model by observing how closely the forecast aligns with the true values. Any large deviations from the actual prices suggest areas where the ARIMA model is less accurate compared to LSTM.

- **SARIMA Forecast vs Actual Prices**:
  - This plot compares the predicted Bitcoin prices from the SARIMA model with the actual prices. Similar to the LSTM plot, we can evaluate the accuracy of the SARIMA model by observing how closely the forecast aligns with the true values. Any large deviations from the actual prices suggest areas where the SARIMA model is less accurate compared to LSTM and ARIMA models.


## Conclusion

The LSTM model is the best option based on the RMSE values.

### Why LSTM is Best:
- **Nonlinear Modeling:** LSTM can handle complex, nonlinear patterns in time series data, which ARIMA and SARIMA may not capture effectively.
- **Sequential Memory:** LSTM's ability to learn long-term dependencies in data makes it more suited for tasks where past trends impact future values.
- **Lower RMSE:** The much lower RMSE value for LSTM indicates significantly better performance in forecasting compared to statistical models.

By leveraging LSTM, we are able to achieve superior accuracy in Bitcoin price prediction, making it the most suitable model for this task.

Thank you for checking out this project! If you have any questions or suggestions, feel free to reach out.

## Contact

You can reach me through the following channels:

- Hewan Leul
- LinkedIn: [your-linkedin-profile](www.linkedin.com/in/hewanleul12)
