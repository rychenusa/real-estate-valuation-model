# Real Estate Rental Price Prediction

Machine learning pipeline for predicting **apartment rental prices** using property attributes and regional socioeconomic indicators.

This repository contains the workflow developed for a **UCLA Math 148 capstone project**, including dataset construction, exploratory data analysis, and regression model development.

The base rental listings dataset comes from the UCI Machine Learning Repository.

---

## Overview

The goal of this project is to estimate apartment rental prices by combining listing-level features with external datasets capturing **economic, geographic, and environmental factors**.

The workflow includes:

- multi-source dataset construction  
- exploratory data analysis (EDA)  
- feature engineering  
- regression model development and evaluation  

The final dataset integrates housing listings with county-level indicators such as income, unemployment, crime rates, climate, and disaster risk.

---

## Data Sources

The project combines the apartment listings dataset with several external data sources.

**Rental Listings**

Apartment listings dataset from the UCI Machine Learning Repository  
https://archive.ics.uci.edu/dataset/555/apartment+for+rent+classified

**Socioeconomic Data**

County-level unemployment and median household income data (USDA).

**Risk and Environmental Data**

FEMA National Risk Index providing county-level disaster risk scores.

**Climate Data**

Average county temperature data from NOAA.

**Crime Data**

FBI Uniform Crime Reports (2017–2019).

**Geographic and Demographic Data**

ZIP code demographics and geographic mapping datasets for selected western U.S. states.

These sources are merged to construct a unified dataset used for modeling.

---

## Project Workflow

### 1. Dataset Construction

`data_merged.Rmd`

Aggregates and merges the external datasets with the apartment listings dataset to produce the cleaned modeling dataset:

```
no_nas_master_dataset.csv
```

---

### 2. Exploratory Data Analysis

`EDA_compiled.ipynb`

Explores the compiled dataset to understand feature distributions and relationships.

The analysis includes:

- summary statistics and missing value checks  
- outlier detection  
- correlation analysis  
- visualization of feature distributions  

---

### 3. Model Development

`M148_model_development.ipynb`

Trains regression models to predict apartment rental prices.

The modeling pipeline includes:

- preprocessing and feature encoding  
- train/test split  
- hyperparameter tuning with GridSearchCV  
- evaluation using Mean Squared Error (MSE) and R²  
- comparison of predicted vs. actual rental prices  

---

## Running the Analysis

Ensure the merged dataset is available:

```
no_nas_master_dataset.csv
```

Run the notebooks in the following order:

1. `data_merged.Rmd`  
2. `EDA_compiled.ipynb`  
3. `M148_model_development.ipynb`
