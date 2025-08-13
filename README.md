# Oil-Gas-Drilling-Activity-Prediction
Drilling Activity Prediction: Oil and Gas operations are dramatically affected by supply, demand and several other factors that compromise the operational planning of resources. To overcome this challenge, predictive analytics could be applied to forecast rotary rig count inside United States using time-series data.

The Project is divided into the following Jupyter Notebook Files:

## [`1. Obtain Data from EIA`](./Obtain%20Data%20from%20EIA.ipynb)
- Obtain data from EIA (Energy Information Administration API)
- Build DataFrame with data obtained from EIA

![EIA dataset](https://github.com/antoniodagnino/Oil-Gas-Drilling-Activity-Prediction/assets/76269794/8f2c8786-d2d6-4e52-8459-4e3bf8971f15)


## [`2. Exploratory Data Analysis`](./Exploratory%20Data%20Analysis.ipynb)
- Data Overview
- Reindex dataframe
- Oil Variables Feature Engineering
- Gas Variables Feature Engineering
- Select Features for forecasting model
- Final Pre-processing Activities
Note: Variables we want to Predict: **Oil Rig Count** and **Gas Rig Count** separately


![Rig Count](https://github.com/antoniodagnino/Oil-Gas-Drilling-Activity-Prediction/assets/76269794/2af18ea1-55a9-4c25-8dca-d87dbcbb18fc)



## 3. Data Modeling

**[`3.1 Data Modeling - VAR model`](./Data%20Modeling%20-%20VAR.ipynb)**
- Load datasets and resample to monthly frequency
- Use oil dataset to make predictions in oil rig count variable:
    - Train/test split
    - VAR Model Hyperparameter selection
    - Fit the model
    - Invert Transformation
    - Generate forecast values and plot results
    - Evaluation Metrics
    - Fit the model again but with 100% of the data
    - Forecast real future values
- Use Gas dataset to predict Gas rig count

  ![VAR](https://github.com/antoniodagnino/Oil-Gas-Drilling-Activity-Prediction/assets/76269794/7c105e8a-5863-4fab-86a5-94439be09333)




**[`3.2 Data Modeling - VARMA model`](./Data%20Modeling%20-%20VARMA.ipynb)**
- Load datasets and resample to monthly frequency
- Use oil dataset to make predictions on Oil Rig Count:
    - Get second order differencing data frame (stationary features dataframe) 
    - Train/test split
    - VARMA Model Hyperparameter selection
    - Fit the model
    - Invert Transformation
    - Generate forecast values and plot results
    - Evaluation Metrics
    - Fit the model again but with 100% of the data
    - Forecast real future values
- Use gas dataset to make predictions on Gas Rig Count

![VARMA](https://github.com/antoniodagnino/Oil-Gas-Drilling-Activity-Prediction/assets/76269794/beda195e-7bff-4038-91cd-df928e5e3a8e)


**[`3.3 Data Modeling - ARIMA model`](./Data%20Modeling%20-%20ARIMA.ipynb)**
- Import dataset and resample to monthly data
- Use oil dataset to predict oil rig count:
    - Find what hyperparameters to be used in the model (p,d,q)
    - Train/test split
    - Create ARIMA model and fit with data
    - Generate Forecast and compare against Test set
    - Evaluation Measures
    - Refit the model with 100% of data and make REAL Forecasting
 - Create ARIMA model with Gas dataframe to predict Gas Rig Count

![ARIMA](https://github.com/antoniodagnino/Oil-Gas-Drilling-Activity-Prediction/assets/76269794/431e3206-974e-4057-b914-9327e14dcf12)


**[`3.4 Data Modeling - Holt Winters model`](./Data%20Modeling%20-%20Holt%20Winters%20Method.ipynb)**
- Import dataset and resample to monthly data
- Use oil dataset to predict oil rig count:
    - Train/test split
    - Create Exponential Smoothing model and fit with data
    - Generate Forecast and compare against Test set
    - Evaluation Measures
    - Refit the model with 100% of data and make REAL Forecasting   
 - Create Exponential Smoothing model with Gas dataframe to predict Gas Rig Count


![Holt Winters](https://github.com/antoniodagnino/Oil-Gas-Drilling-Activity-Prediction/assets/76269794/27ebb41f-0a85-42b9-8bcf-bee2a10517ff)



**[`BONUS Data Modeling - RNN model`](./Data%20Modeling%20-%20RNN.ipynb)**
- Load datasets and resample to monthly frequency
- Use oil dataset to make predictions in oil rig count variable:
- Tune Data: To adjust re-train models and check performances
- ETS Decomposition: Identify Trend, Seasonality and Error
- Train/test split
- Scale and Transform data
- TimeSeries Generator
- Create RNN for OIL DF
- EarlyStopping
- Evaluation Batch
- Inverse Transformed data
- Plot Test Set Vs Predictions
- Evaluation Metrics (Pending)
- Create Model with Gas dataset to make predictions in Gas Rig Counts
