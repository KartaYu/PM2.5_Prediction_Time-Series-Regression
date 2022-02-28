# PM2.5 Prediction Of Hsinchu| Time Series Regression
### Data Source
- Link : 空氣監測品質網 <https://airtw.epa.gov.tw/CHT/Query/His_Data.aspx>
- Using October and November air quality data to predict December value.
### Data preprocessing
1. Fill missing data
    * fill with mean of previous value and next value
2. Transpose Dataframe
![image](https://github.com/KartaYu/PM2.5_Prediction_Time-Series-Regression/blob/main/Pic/transpose.png)
4. Data split and prediction target
    * Using all feature labels to predict next hour result.
    * Only using PM2.5 label to predict next hour result.
    * Using all feature labels to predict six hours later result.
    * Only using PM2.5 label to predict six hours later result.
 ### Model
 1. LinearRegression
 2. XGBRegressor
 ### Evaluation
 - Result of LinearRegression
    * MAE of using all feature labels to predict next hour result : 2.835
    * MAE of using PM2.5 label to predict next hour result : 2.522
    * MAE of using all feature labels to predict six hours later result : 6.131
    * MAE of using PM2.5 label to predict six hours later result : 4.579
 - Result of XGBRegressor
    * MAE of using all feature labels to predict next hour result : 2.664
    * MAE of using PM2.5 label to predict next hour result : 2.676
    * MAE of using all feature labels to predict six hours later result : 4.756
    * MAE of using PM2.5 label to predict six hours later result : 4.910
![image](https://github.com/KartaYu/PM2.5_Prediction_Time-Series-Regression/blob/main/Pic/MAE.png)
