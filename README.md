# Crop-Yield-Prediction
This project builds a machine learning pipeline to predict agricultural crop yield using historical yield data, climate variables, and extreme weather indicators. Multiple models are implemented and compared to evaluate predictive performance.

# Project Overview

Accurate crop yield prediction is essential for:

Food security planning
Agricultural policy development
Climate impact analysis

This project integrates data from:

FAOSTAT (Crop Yield)
NASA (Climate Data)
World Bank (Extreme Weather Indicators)
and applies machine learning models to predict yield across selected countries.

# Dataset Description
1. FAOSTAT Yield Data
Features:
Area (Country)
Year
Crop
Yield

3. NASA Climate Data
Daily observations aggregated yearly:
Avg_Temp
Max_Temp
Min_Temp
Total_Rainfall

5. World Bank Extreme Weather Data
Feature:
Extreme_Rain

# Data Preprocessing

The pipeline includes:

Filtering selected countries:
India
Pakistan
Palestine
Cleaning and type conversion
Aggregating daily climate data → yearly
Handling missing values using:
Group-wise mean imputation
Outlier removal (1st–99th percentile)
Feature engineering:
Temp_Range = Max_Temp - Min_Temp
Merging datasets:
Climate data merged by Area + Year
Extreme rainfall treated as a static country-level feature
# Machine Learning Models

The following models are implemented:

Linear Regression, Random Forest Regressor, XGBoost Regressor, Neural Network 

# Evaluation Metrics

Models are evaluated using:

MAE (Mean Absolute Error), RMSE (Root Mean Squared Error), R² Score
# Visualizations

The project includes:

Predicted vs Actual Yield, Error Distribution Plot, Feature Importance

# Libraries
Python, Pandas & NumPy, Scikit-learn, XGBoost, TensorFlow / Keras, Matplotlib & Seaborn

# Summary
This project predicts crop yield using climate and extreme weather data. It combines datasets from FAOSTAT, NASA, and the World Bank, and applies machine learning models to evaluate how environmental factors affect agricultural productivity.

# How to Run
1. Open the project notebook in Google Colab.
2. Upload the required datasets when prompted:
    faostat_yield.csv
    nasa_climate.csv
    worldbank_extreme_events.csv
3. Run all cells in order from top to bottom.
4. The code will automatically:
    Load and preprocess the data
    Merge datasets
    Train machine learning models
    Evaluate performance metrics (MAE, RMSE, R²)
5. View results and model comparison outputs in the final sections of the notebook.
