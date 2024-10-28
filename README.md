In this code, we have used the solar irradiance and earth skin temperature data of ten years (2012 - 2021) to predict the expected average solar cell efficiency for each month in 2022. We used ARIMA, seasonal ARIMA, and LSTM to create the required time series models. We calculated the RMSE (Root Mean Square Error) for each method compared with efficiency calculated from actual data for 2022.

![image](https://github.com/user-attachments/assets/421e786c-944a-4db8-853f-14c1746051b5)

We can see that the Seasonal ARIMA model and LSTM model with 12 outputs (single stage prediction) give the best results. The ARIMA model does not capture the seasonality in the data, so it does not give good results. The LSTM model with 1 output (12 step prediction) gives the worst results despite having very low training losses. This is because we add the predictions back into the data at each stage and this causes errors to accumulate.

 The solar irradiance and earth skin temperature data was obtained from the LARC Power Project NASA website.

We chose the Sun Power E20/435 solar cell for our analysis, and from the data sheet obtained the following parameters: 
 
![image](https://github.com/user-attachments/assets/ef37ce37-2832-4e17-a0c5-7141c941897e)


