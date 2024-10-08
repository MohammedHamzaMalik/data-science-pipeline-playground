# Car Price Prediction Project

## Introduction
This document provides a comprehensive overview of the machine learning project aimed at predicting car prices based on various features. The process involves data exploration, feature engineering, model training, evaluation, and selection of the best-performing model.

## Data Exploration

### Correlation Matrix
We begin with an analysis of the correlation between numerical features in the dataset using a heatmap.

This correlation matrix helps identify relationships between features and the target variable, price.
Feature Selection

Based on the correlation analysis, we select the following features for model training:

- wheelbase
- carlength
- carwidth
- curbweight
- cylindernumber
- enginesize
- horsepower
- boreratio
- price

### Feature Engineering

Feature engineering is a critical step that involves transforming and creating features to improve model performance. This includes:

- Encoding Categorical Variables: We apply one-hot encoding to convert categorical variables into a numerical format suitable for modeling.

- Scaling Numerical Features: Features are scaled to ensure they contribute equally to model training, improving convergence speed and accuracy.

Model Training

We explore multiple regression models to identify the best-performing one:

- Random Forest Regressor
- Gradient Boosting Regressor
- XGBoost Regressor

For each model, we evaluate performance using error metrics such as MAE, MSE, RMSE, and R² Score.

### Model Evaluation

We compare the performance of all trained models based on the calculated error metrics.
### Summary of Results

After evaluating all models, we identify XGBoost as the best performer based on:

- Lowest Test MAE
- Lowest Test RMSE
- Highest Test R² Score

### Saving the Model

To ensure the trained model can be reused, we save it using joblib