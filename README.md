# Oil-Gas-Drilling-Activity-Prediction
Drilling Activity Prediction: Oil and Gas operations are dramatically affected by supply, demand and several other factors that compromise the operational planning of resources. To overcome this challenge, predictive analytics could be applied to forecast rotary rig count inside United States using time-series data.

The Project is divided into the following Jupyter Notebook Files:

1. Obtain Data from EIA
- Obtain data from EIA (Energy Information Administration API)
- Build DataFrame with data obtained from EIA


2. Exploratory Data Analysis
- Data Overview
- Reindex dataframe
- Oil Variables Feature Engineering
- Gas Variables Feature Engineering
- Select Features for forecasting model
- Final Pre-processing Activities
Note: Variables we want to Predict: **Oil Rig Count** and **Gas Rig Count** separately


3. Data Modeling

3.1 Data Modeling - VAR model
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


3.2 Data Modeling - VARMA model
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


3.3 Data Modeling - SARIMA model
- Import dataset and resample to monthly data
- Use oil dataset to predict oil rig count:
    - Find what hyperparameters to be used in the model (p,d,q)
    - Train/test split
    - Create ARIMA model and fit with data
    - Generate Forecast and compare against Test set
    - Evaluation Measures
    - Refit the model with 100% of data and make REAL Forecasting
 - Create ARIMA model with Gas dataframe to predict Gas Rig Count
