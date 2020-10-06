# Walmart M5 Time Series Challenge
Purposed solution for Kaggle M5 challenge with different approaches.

### The challenge
This challenge consists in predicting the sales for the next 15 days for 10 Walmart stores accross 3 different states for a big
variety of items.

### Data

We have available around 2 years of historical data of units sold, prices and calendar events.

### Approach

I've decided to try 5 different approaches:

- ARIMA - Auto Regression Integration Moving Average is a basic composition of statistical models to do Time Series Predictions.
- SARIMAX - Same as above approach but also considering (S)easonality and e(X)onorous features, such as  holidays, vacations or 
other single events that may alter the regular behavious of a time series.
- Prophet - Time Series modeling developed by Facebook, Prophet is an easy to use and interpretable tool to approach a 
time series problem.
- LGBM/XGB - A regular (not TS) ML approach to a time series problem.


### Conclusion

The time series approaches with statistical models have to model each combination of store/item which 
represents more than 30.000 time series. Even if we make a simple ARIMA model, it 
takes a lot of time to build the time series, tune and predict for all these combinations. 

This way, LGBM turned out to be the best approach because of its time consumption; even though it is not how
we usually face Time Series, with this ML model I've obtained significant results.


<introduce a table with comparisons in metrics and training/predicting times> 
