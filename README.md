# Enhanced Shortwave Radiation Prediction Using Machine Learning Models and Meteorological Parameters

## Overview

Shortwave radiation plays a crucial role in Earth's energy balance, impacting weather patterns, climate modeling, and renewable energy forecasting. This project aims to enhance the prediction accuracy of shortwave radiation by leveraging advanced machine learning (ML) algorithms trained on meteorological parameters such as temperature, humidity, cloud cover, wind speed, and atmospheric pressure.

## Objectives

- Improve the accuracy of shortwave radiation predictions using ML techniques.
- Analyze the relationship between meteorological variables and solar radiation.
- Compare performance of multiple ML models including linear and nonlinear methods.
- Develop a scalable and reproducible framework for deployment in environmental forecasting systems.

## Dataset

The dataset includes hourly meteorological observations from ground-based stations and satellite-derived radiation values.

**Features:**
- Air Temperature (°C)
- Relative Humidity (%)
- Wind Speed (m/s)
- Cloud Cover (oktas or %)
- Atmospheric Pressure (hPa)
- Solar Zenith Angle (degrees)
- Precipitation (mm)

**Target:**
- Downwelling Shortwave Radiation (W/m²)

Data sources:
- RAMA Buoy
- International satellite cloud climatology project (isscp)
- Moored Buoy
- Reanalysis

## Methodology

### 1. Data Preprocessing
- Handling missing values using interpolation and imputation.
- Feature scaling using standardization or normalization.
- Feature engineering (e.g., time of day, day of year, etc.).

### 2. Machine Learning Models
- **Linear Regression**
- **Random Forest Regressor**
- **Gradient Boosting Machines (XGBoost)**
- **Support Vector Regression (SVR)**
- **Deep Neural Networks (DNNs)**

### 3. Evaluation Metrics
- Root Mean Squared Error (RMSE)
- Mean Absolute Error (MAE)
- R² Score
- Residual Analysis

### 4. Cross-Validation
- k-Fold Cross-Validation (k = 5 or 10)
- Grid Search for hyperparameter tuning

## Results

| Model                | RMSE (W/m²) | MAE (W/m²) | R² Score |
|---------------------|-------------|------------|----------|
| Linear Regression    | 75.2        | 58.3       | 0.72     |
| Random Forest        | 43.7        | 31.2       | 0.89     |
| XGBoost              | 39.5        | 29.1       | 0.91     |
| SVR                  | 54.6        | 40.7       | 0.84     |
| Deep Neural Network  | 37.9        | 28.5       | 0.92     |

## Key Findings

- Tree-based and deep learning models significantly outperform linear models.
- Cloud cover and solar zenith angle are the most important predictors.
- Feature selection and ensemble learning further improve model robustness.

## Implementation

Codebase includes:
- `data_preprocessing.py` – Data cleaning and transformation
- `model_training.py` – Training and evaluation routines
- `visualization.ipynb` – Interactive plots and EDA
- `predictor.py` – Inference script for real-time use

To run:
```bash
pip install -r requirements.txt
python model_training.py
