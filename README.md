# austin-timeseries-forecasting
Collection of visualization and time series forecasting for real estate in Austin, TX
# Project Overview
* Downloaded housing prices around US from year 2000 to current (2023/03) from Zillow's website. 
* Engineered features of the data to be used for EDA and machine learning.
* Deleted other cities and left only Austin, Tx/ Travis County. 
* Used visualzation tools to analyze data. 
* Optimized time series forecasting to forecast housing prices 3 years and 5 years from now.
* Calculated return of investment to indicate the top 5 and last 5 investments by zipcode. 
# Code & Resources Used
Python Version: 3.9.12 | Jupyter Notebook
* Python Packages: pandas, numpy, sklearn, matplotlib, seaborn, statsmodel.api, 
* Code help: https://towardsdatascience.com/time-series-modeling-with-arima-to-predict-future-house-price-9b180c3bbd2f
# Data Collection
Zillow uploads data on their website to the public to use. I specifically used the ZHVI (Zillow Home Value Index) data. 
* Retrieved home values from 01/31/2000 to 03/01/2023.
* Retrieved over 27000 home value data.
* Retrieved data from all 50 states. 
# Data Cleaning
After collecting the data I have made the following changes: 
* Delete rows that were not from Austin, TX.
* Deleted useless columns .
* Dropped all null values.
* Changed all dates into datetime data type.
* Set dates to rows and index for easier use in time series analysis.
# EDA
Here are some of the foundings: 
* Starting from 2021, housing prices increased everywhere in Austin area significantly.
* Housing prices peaked from startin of 2021 to July 2021.
* Zipcode 78746 and 78703 are significantly more expensive than others which are located in the lake area and downtown Austin.

<img width="1007" alt="Screen Shot 2023-04-23 at 2 15 45 PM" src="https://user-images.githubusercontent.com/118776460/233861108-432eb8fa-2fb7-4d11-93ad-36284e42d998.png">
<img width="1004" alt="Screen Shot 2023-04-23 at 2 16 02 PM" src="https://user-images.githubusercontent.com/118776460/233861111-b44415d9-c683-46a4-9f9a-827bb2a56265.png">

# Model Preprocessing
I have checked for seasonal decomposition and stationarity. 
* The first graphs shows that the data has an upward trend along with yearly seasonality.
* The second picture shows that our data is non-stationary because we fail to reject our null hyphothese witha p-value of 0.49 where null hyphothesis is that the data is not stationary. 

<img width="876" alt="Screen Shot 2023-04-23 at 2 17 14 PM" src="https://user-images.githubusercontent.com/118776460/233865810-51854811-8984-46e5-ab63-d8417263c1d6.png">
<img width="757" alt="Screen Shot 2023-04-23 at 3 53 37 PM" src="https://user-images.githubusercontent.com/118776460/233865817-df7449f2-d3c5-4412-abd3-7dab8ac2585d.png">

# Model Building
SARIMA Time Series Model
* Since our data is non-stationary and have a seasonal treand I've decided to use SARMIA.
* Found the best parms of p,d,q,P,D,Q for each zipcode.
* Tested on 3 random zipcode first.
* Forecasted housing prices for 2026 and 2028 as well as the return of investment on each of the year. 
# Foundings
* Top 5 3 Year ROI Zipcodes: 78704, 78734, 78725, 78705, 78732
* Top 5 5 Year ROI Zipcodes: 78734, 78704, 78725, 78705, 78732
* Worst 5 3 Year ROI Zipcodes: 78701, 78726, 78747, 78736, 78653
* Worst 5 5 Year ROI Zipcodes: 78701, 78726, 78747, 78736, 78653
