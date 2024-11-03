# -Time-Series-Predictive-Model-for-Sales-Forecasting
Python | Time Series | Arima Model


#Time Series Forecasting for Sales Data

#Overview

This project aims to forecast future sales data using a time series approach. The model uses the Seasonal AutoRegressive Integrated Moving Average (SARIMA) method to predict monthly sales for a given product over the next 12 months. The dataset contains historical monthly sales data for a set of products, and the goal is to create a reliable forecast that can be used for future planning and decision-making.

#Steps Involved

Data Preprocessing: The dataset, which contains sales data for different products, is read from a CSV file. The 'Date' column is converted into a datetime format and set as the index. The sales data is then resampled to monthly intervals, filling any missing values with zeros.

Stationarity Testing: The Augmented Dickey-Fuller (ADF) test is applied to the sales data to check for stationarity. If the data is not stationary (p-value > 0.05), differencing is applied to make the data suitable for time series analysis.

Autocorrelation and Partial Autocorrelation Analysis: The AutoCorrelation Function (ACF) and Partial AutoCorrelation Function (PACF) plots are used to determine the appropriate values of p (AR order) and q (MA order) for the SARIMA model.

Parameter Fine-Tuning: A grid search is performed to identify the best combination of parameters (p, d, q) based on the Akaike Information Criterion (AIC). The goal is to minimize the AIC value, which helps in selecting the best-fitting model.

Model Fitting: The SARIMA model is fitted to the training data using the optimal parameters obtained from the grid search. The SARIMAX function from the statsmodels library is used for this purpose.

Forecasting: The model is used to generate a 12-month forecast of future sales. The forecasted results are visualized, along with confidence intervals to represent the uncertainty in the predictions.

#Requirements

Python 3.6+

Pandas

NumPy

Matplotlib

Statsmodels

Scikit-learn
