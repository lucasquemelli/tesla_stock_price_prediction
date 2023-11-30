# Tesla Stock Price Prediction

<code><img width="100%" src="https://github.com/lucasquemelli/tesla_stock_price_prediction/blob/main/Images/tesla.jpeg"></code>

# 1. Business Problem

**Introduction**

---

Tesla, Inc. is an American electric vehicle and clean energy company based in Palo Alto, California. Tesla's current products include electric cars, battery energy storage from home to grid-scale, solar panels and solar roof tiles, as well as other related products and services.

Time series forecasting method is the process of making scientific predictions based on the analysis of historical data points. Time series forecasting involves building models to make informed and strategic decisions, which can help with future analysis and forecasts. Time series models may not always give exact predictions. 

Time series analysis involves analyzing historical data by developing models to help you understand the cause of a particular event. It can help you understand the reasons for the outcomes of certain historical events. Forecasting takes the analysis models and uses that knowledge to extrapolate and predict future events. Some models used for time series forecasting and analysis are moving average, exponential smoothing, and ARIMA.

```From statsmodels.tsa.arima.model``` we may ```import``` the ```ARIMA``` model for time series analysis. **ARIMA is an acronym for AutoRegressive Integrated Moving Average** and is **used for stationary time series** that have no predictable patterns in the long term. Before using the ARIMA model, we must identify if the data is stationary or non – stationary. We used the ADF (Augmented Dickey-Fuller) Test By using the following module: 

```from statsmodels.tsa.stattools import adfuller```

We checked out the closing price of the stock. **The p-value obtained after running the ADF test must be less than 0.05(tested significance value) for the data to be stationary**. Data was non-stationary, then we used LSTM model to predict Tesla stock price.

**Purpose**

---

To predict Tesla (TSLA) stock price based on daily data over 8 years.

**NOTE**: this is a shorter project, since to predict stock price we use daily data. For a interval of 8 year we only have around 2000 data points. That's too little to perform multiple analysis. But it is enough to develop a Machine Learning model.
