# Forecasting Electricity Production: Kaggle Competition
This repository is  a Kaggle competition wich the aim  is to create a model that is uniquely capable of monitoring and analysing weather data to produce a plant-level production forecast. <br>
[Kaggle Competition: Renewable Energy Production Forecaster](https://www.kaggle.com/competitions/renewable-energy-production-forecaster/)

### Developed by:
- Juan Felipe Vásquez Uribe
- Santiago Rojas Posada
- Aylla Joani Mendonca de Oliveira

## Project Scope

The main purpose of this project is educational, focusing on basic Machine Learning concepts and workflow. The development follows these main steps:

1. **Exploratory Data Analysis (EDA):**
   Analyze the dataset to understand the business problem and identify key patterns in the data.

2. **Model Development:**
   Train and evaluate three different predictive models independently: Random Forest, XGBoost, and LightGBM.
   Each model includes its own data preprocessing, feature engineering, and hyperparameter tuning process.

3. **Model Comparison and Ensemble:**
   Compare the performance of the three models and build an ensemble model combining their predictions.

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

