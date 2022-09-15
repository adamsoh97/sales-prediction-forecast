# Sales Prediction & Forecasting for Brazilian E-Commerce Public Dataset by Olist

This project aims to determine sales prediction and forecast through time-series analysis techniques on the platform. We shall demonstrate the application of time series by focusing on toy sales in this project.

Dataset Link: https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce

## Result

#### Prediction of time series models

![image](https://user-images.githubusercontent.com/72193228/190415652-7fa42395-d0ca-429d-a331-469e638f0b2e.png)

<p align="justify"> In general, all models can pick up the trend of the data and provide prediction trends similar to the original data. Except for the second XGBoost model, all models did not pick up the adaptation on the peak value in the original data. One thing that is observed in the prediction diagram is the prediction produced by the second XGBoost model highly matches the plotting of the original data. However, this advantage is not shown in the first XGBoost model which the prediction has a lower value than the original data. For ARIMA models, both models produced decent predictions by fitting themselves within the original data. </p>

#### Forecast of time series models

![image](https://user-images.githubusercontent.com/72193228/190415692-2af6a158-8dc0-401c-a6e0-552cc46f1366.png)

<p align="justify"> Figure above shows the forecast of the models up to 100 days. By looking at the forecast, the first ARIMA model cannot capture the trend of the data as it provides the lowest forecast value at a constant pace. It did not reflect the changes in sales every day. While the other three models successfully capture the trend of the data, the second ARIMA model has constantly increased forecast value and comes to a constant after November 2018. Moreover, both XGBoost models have a similar irregular pattern with the lower forecast value in the first XGBoost model. </p>

#### Performance metrics of time series models

![image](https://user-images.githubusercontent.com/72193228/190415790-bb7e5103-9019-4b44-9cd0-63351b26d93a.png)

<p align="justify"> Table above concludes the performance metrics of all four models. Based on the results in the table above, the second XGBoost model outperforms with the lowest MSE and RMSE values. The second XGBoost model has the nearest predictions to the original data, and this explains the good performance in the prediction and forecasting. XGBoost models have lower MSE and RMSE compared to ARIMA, which makes XGBoost a better algorithm for predicting sales. By comparing both ARIMA models, it is observed that the first ARIMA model has slightly lower MSE, RMSE and AIC compared to the second ARIMA model. With the first-degree differencing in the second ARIMA model, it picks up the trend better compared to the first ARIMA model which does not experience differencing. </p>

Overall, XGBoost with a learning rate of 0.05 outperforms the best time series model for sales forecasting.
