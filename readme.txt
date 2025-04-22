While being at Code Academy Berlin (CAB), I explored into Time Series algorithms on my own. 
This happened out of a professional interest in demand planning.

I connected my experiment with data from Project 04 ('Bike_Share') at CAB. I aggregated the data for three years (2021-2023) by station and day/week. 

I then split the data into train (2021 & 2022) and test data (2023). 

Most algorithms struggled with prediction of turnover and imbalance by station. In general I had better results when using the station data which was aggregated by week (rather than day).

Best results came from:
SARIMAmodel = SARIMAX(train, order=(2, 1, 2), seasonal_order=(2, 1, 2, 52))
RSME between 0.42 (Turnover) and 1.77 (Imbalance)

The folders 'Daily_Station_Data' and 'Weekly_Station_Data' include more sample stations if you want to use the provided templates 'time_series_Daily/Weekly....ipnyb' for other than the selected stations.
