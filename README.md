# Forecasting Electricity Production: Kaggle Competition
This repository is  a Kaggle competition wich the aim  is to create a model that is uniquely capable of monitoring and analysing weather data to produce a plant-level production forecast. <br>
[Kaggle Competition: Renewable Energy Production Forecaster](https://www.kaggle.com/competitions/renewable-energy-production-forecaster/)

### Developed by:
- Juan Felipe Vásquez Uribe
- Santiago Rojas Posada
- Aylla Joani Mendonca de Oliveira

---
## Problem Description 

This project addresses a regression problem where the goal is to predict photovoltaic electricity generation using only meteorological, astronomical, and radiation-related variables. The dataset provides:
- Historical photovoltaic power generation
- Meteorological measurements
- Solar geometry (astronomical variables)
- Radiation-related variables

Based on these inputs, the objective is to train a model capable of predicting electricity generation for the same calendar dates but at a different plant or geographical location.Therefore, this is not a classical time series forecasting problem, since the model does not rely on past power values to predict future values. Instead, the model must learn the relationship between instantaneous environmental conditions and plant power output.

In essence, the model should learn that photovoltaic power generation depends primarily on:
- Solar radiation
- Cloud coverage
- Sun position
- Temperature
- Atmospheric conditions

The competition allows the use of external data sources. However, the exact plant location is not explicitly provided. Its approximate location can be inferred using astronomical variables such as sunrise and sunset times. A rough estimation suggests the plant is located around *48°N–51°N latitude*, likely somewhere in Central Europe (e.g., Germany or Poland), since winter days in January show relatively short daylight periods.

---
## Project Workflow

The project was developed through four sequential stages, each documented in a dedicated Jupyter Notebook.

### 1. Exploratory Data Analysis (EDA)

The first stage focused on understanding the dataset and analyzing the behavior of the available variables.
This included studying meteorological, astronomical, and radiation-related features, identifying missing data patterns, detecting anomalies, and evaluating feature distributions and correlations.

### 2. Baseline Model Benchmarking
After basic data preprocessing and feature transformation, multiple machine learning models were tested to establish baseline performance.
At this stage, no hyperparameter tuning was performed. The objective was to compare different algorithms and identify the most promising candidates based on evaluation metrics.The three best-performing models were selected:
* Random Forest
* Extreme Gradient Boosting (XGBoost)
* Light Gradient Boosting Machine (LightGBM)

### 3. Feature Engineering & Model Optimization
In this stage, each selected model was optimized independently.
A dedicated preprocessing and feature engineering pipeline was designed for each model, including: Feature selection, Feature transformations, Handling of missing valuesand Model-specific preprocessing
Hyperparameters were then tuned to minimize prediction error while controlling overfitting and ensuring good generalization performance.

### 4. Ensemble Learning

Once the three optimized models were finalized, ensemble strategies were applied to improve predictive performance. Two ensemble approaches were implemented:
- Averaging Ensemble: Final predictions were obtained by averaging the outputs of the three base models.

- Stacking Ensemble: A meta-model was trained using the predictions of the three base models as input features, allowing it to learn how to optimally combine their strengths.

----
## Project Scope
The main purpose of this project is educational, focusing on basic Machine Learning concepts and workflow.

