# PySpark Housing Data Analysis & ML Pipeline

PySpark is the Python interface for Apache Spark, providing powerful tools to work with huge amounts of data and build efficient data pipelines. While you don't necessarily need big data to benefit from PySpark, its SparkSQL functionality can greatly simplify routine data analysis compared to traditional Pandas workflows, which may require extensive code for data cleaning and transformation.

This repository presents a professional, end-to-end notebook for the California Housing dataset. The dataset provides key information about housing features across various districts in California, including:

- **Geographic Features:** longitude, latitude  
- **Housing Characteristics:** housing_median_age, total_rooms, total_bedrooms, households  
- **Demographic & Economic Features:** population, median_income, median_house_value  

## Table of Contents

- [Introduction](#introduction)
- [Dataset](#dataset)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Results](#results)
- [Next Steps](#next-steps)
- [License](#license)

## Introduction

This notebook demonstrates a complete end-to-end workflow for analyzing the California Housing dataset using PySpark. The goals are to:

- **Perform Exploratory Data Analysis (EDA):**  
  Inspect the dataset by examining its schema, descriptive statistics, missing data, distinct values, and performing aggregations.
  
- **Visualize Data:**  
  Convert small subsets of the data to Pandas DataFrames to create visualizations (e.g., bar charts, heatmaps, histograms, and boxplots) that reveal underlying trends and correlations.
  
- **Engineer Features:**  
  Enhance the dataset by creating new, informative features such as ratios (e.g., rooms per household), logarithmic transformations to reduce skewness, categorical binning (e.g., age categories), and interaction terms.
  
- **Build Machine Learning Pipelines:**  
  Develop regression models (Linear Regression, Random Forest, and Gradient Boosted Trees) using Spark ML. The pipelines include steps like categorical indexing, feature vector assembly, model training, and evaluation.
  
- **Hyperparameter Tuning:**  
  Use CrossValidator with grid search to optimize Random Forest model parameters (e.g., number of trees and maximum depth).
  
- **Model Evaluation:**  
  Assess model performance using RMSE and R² metrics and visualize the predictions against actual values.

## Dataset

The California Housing dataset contains comprehensive information about housing features across various districts in California. The dataset is provided in CSV format and is assumed to reside in the `sample_data` directory for the Google Colab environment.

## Features

**Original Features:**
- `longitude`, `latitude`
- `housing_median_age`
- `total_rooms`, `total_bedrooms`, `households`
- `population`, `median_income`, `median_house_value`

**Engineered Features:**
- **Rooms per Household:** `total_rooms / households`
- **Bedrooms per Room:** `total_bedrooms / total_rooms`
- **Population per Household:** `population / households`
- **Logarithmic Transformations:** Log transformations of `total_rooms`, `total_bedrooms`, and `population`
- **Interaction Terms:** e.g., `housing_median_age * median_income`
- **Polynomial Features:** e.g., `median_income²`
- **Additional Interactions:** e.g., `log_total_rooms * population`


