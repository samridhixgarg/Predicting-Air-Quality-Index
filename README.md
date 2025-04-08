# Predicting-Air-Quality-Index
AIR QUALITY INDEX
# Air Quality Prediction Using Machine Learning

This project predicts PM2.5 concentrations based on time-based features (Year, Month, Day, Hour) using a machine learning model. It also maps the predicted PM2.5 values to their respective AQI (Air Quality Index) categories based on Indian air quality standards.

## Dataset

The dataset contains hourly air quality measurements, including:
- Timestamp
- Year
- Month
- Day
- Hour
- PM2.5 levels

## Problem Statement

The goal is to build a machine learning model that:
1. Predicts PM2.5 levels using time-based features
2. Converts predicted PM2.5 into AQI categories

This can help in forecasting air quality trends and providing early warnings for high pollution periods.

## Methodology

1. **Data Cleaning**
   - Converted Timestamp to datetime format
   - Dropped missing PM2.5 values
   - Selected relevant features: Year, Month, Day, Hour

2. **Feature Scaling**
   - Applied `StandardScaler` to standardize the input features

3. **Model Training**
   - Trained and evaluated two models:
     - Linear Regression (Baseline)
     - Random Forest Regressor (Primary)

4. **Evaluation Metrics**
   - Mean Absolute Error (MAE)
   - Mean Squared Error (MSE)
   - R² Score

## Results

| Model              | MAE   | MSE    | R² Score |
|-------------------|-------|--------|----------|
| Linear Regression | 19.83 | 584.76 | 0.05     |
| Random Forest     |  2.72 |  21.79 | 0.96     |

Random Forest significantly outperformed Linear Regression and was chosen as the final model.

## AQI Mapping

PM2.5 values are mapped to Indian AQI categories:

| PM2.5 Range (μg/m³) | AQI Category |
|---------------------|--------------|
| 0–30                | Good         |
| 31–60               | Satisfactory |
| 61–90               | Moderate     |
| 91–120              | Poor         |
| 121–250             | Very Poor    |
| 250+                | Severe       |

## Prediction Example

For the datetime [2025, 1, 15, 18], the predicted PM2.5 value was:


