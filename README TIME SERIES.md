
##Introduction
I wanted to explore data science techniques on time series forecasting that would be helpful for businesses in areas like sales or demand forecast.

Since I love the concept of bike sharing as a mode of transport that is both good for the environment (no pollution) and also a good form of exercise, I decided to practice on a dataset of San Francisco bike sharing available from Kaggle (https://www.kaggle.com/benhamner/sf-bay-area-bike-share)

I define the daily demand of bike trips as the sum of all trips started at every station for each day.

##Approach
### This is the workflow I took:

Perform exploratory data analysis for missing values, correct data type and outlier data
Perform any necessary data cleaning and data munging
Transform the data into a time series of daily frequency
Check the time series for stationarity and/or seasonality trends and perform any necessary transformation
Identify the parameters for a suitable SARIMA model and evaluate the performance of the model
Incorporate exogenous variables to build a SARIMAX model and evaluate its performance
Explore alternative models like regression and compare against SARIMAX models
Summary of Findings
As can be expected from common sense, predicting the bike demand over a shorter forecast period gives better results than over a longer period
Incorporating weather attributes as exogenous variables helped to improve the performance of the SARIMAX model, even for longer forecast period
Unfortunately, the residuals of the model did not show randomness or no autocorrelation (Ljung-Box test failed to accept the null hypothesis) hence the SARIMAX model failed to model all the trends inherent in the series
Random Forest Regressor performed slightly better than the SARIMAX models.
Although the improvement was mariginal, the advantage of Random Forest Regressor is that it is able to highlight the importance of each predictor, hence it is possible to identify the most importance features for forecasting
Data source: https://www.kaggle.com/benhamner/sf-bay-area-bike-share
