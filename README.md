# Time-Series-Forecasting-with-Zeros


The .csv file contains production volume for a period of 235 weeks. The goal is to build a model to predict the next 10 weeks of productions.


Based on the forecasts, functional teams can work together to propose strategies related to sales, marketing, inventory & product development.


This notebook contains:

- some exploratory analysis and seasonal decomposition of the time series
- strategies to deal with zeros in the data:
    - do nothing
    - replace with NaN
        - fbprophet handles NaN automatically, while auto.arima doesn't
    - remove zeros
        - potentially not feasible since total periods of zero vary year by year
        - would affect yearly the seasonality of the series
- forecasting:
    - train test split
    - visualizations of predictions vs. observations
    - packages used for modeling:
        - pmdarima (auto.arima): grid search to determine best paramters
        - fbprophet: provides a much faster implementation
    - model evaluation

- potential for improvements:
    - take into account ACF, PACF & stationarity when tuning parameters of SARIMAX
    - take into account domain knowledge or business contexts
