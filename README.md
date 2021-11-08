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

- Create Model with Gas dataset to make predictions in Gas Rig Counts



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
