# Timeseries Forecasting

### Goal
•	In this project I tried to predict December 2019 sales using the historical daily sales data (From January 2017 to December 2019).  
 
### Description
* There are two separate script files, one for the ARMA model (Autoregressive - moving average) and the other for the various machine learning algorithms. 

* I seperated them since they have different processing steps.

### Workflow
* Dataset is pre-processed, handled missing values
* For the ARIMA model, to check stationarity, Augmented Dickey-Fuller test is applied.
* Autocorrelation/Partial autocorrelation plots are created and parameters of (p,d,q) are determined wrt to them
    
* For the machine learning models, since there are no features, I created 6 new features from the time stamps.
    * A feature for year
    *	A feature for month of year 
    *	A feature for week of the year
    *	A feature for day of the month
    *	A feature for day of the week
    *	A feature for whether it is weekend or not

* Tried various machine learning models and decided to use Random Forest model based on the RMSE score of them.
* Then I trained the model again but this time with the whole dataset (to predict the December sales)


### Libraries Used
*	numpy, pandas
*	sklearn
* statsmodel
