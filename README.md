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
* Starting from 2021, housing prices increased everywhere in Austin area significantlly.
* Housing prices peaked from startin of 2021 to mid 
<img width="1007" alt="Screen Shot 2023-04-23 at 2 15 45 PM" src="https://user-images.githubusercontent.com/118776460/233861108-432eb8fa-2fb7-4d11-93ad-36284e42d998.png">
<img width="1004" alt="Screen Shot 2023-04-23 at 2 16 02 PM" src="https://user-images.githubusercontent.com/118776460/233861111-b44415d9-c683-46a4-9f9a-827bb2a56265.png">


# Model Building
I have built two decision tree to see the process of rules that are associated with the specified recovery score which are over 40% and over 90%.
I also split the data into train and test sets with a test size of 33%.
# Model Performance
I have used a loop to find the best criterion and max depth for the two model. 
* Over 40% Model: 0.94
* Over 90% Model: 0.87

<img width="578" alt="Screen Shot 2023-02-27 at 9 24 37 AM" src="https://user-images.githubusercontent.com/118776460/227013030-f73b1748-8e88-4f9d-9bb6-8d787741fbd4.png">
