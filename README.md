# Mercari-price-suggestion
A Kaggle competition Mercari Price suggestion Challenge, where I ranked in under the top 6 percentile.
Please view below link to see how I tackled the problem.
https://akarshan-1711.medium.com/regression-to-suggest-selling-price-7218d35cad15

## Overview
Welcome to the Mercari Price Suggestion Challenge repository! This repository contains the code and documentation for predicting prices of items listed on Mercari based on various features provided in the dataset. This competition was hosted on Kaggle, and the goal was to develop a model that suggests the right price for sellers to list their products.

## Contents

1. [Introduction](#introduction)
2. [Exploratory Data Analysis (EDA)](#eda)
3. [Feature Extraction](#feature-extraction)
4. [Modeling](#modeling)
   - Ridge Regression
   - LightGBM
5. [Hyperparameter Tuning](#hyperparameter-tuning)
6. [Deployment](#deployment)
7. [Conclusion and Future Work](#conclusion-and-future-work)
8. [References](#references)

## Introduction
The Mercari Price Suggestion Challenge involves predicting the prices of products listed on Mercari, a marketplace where sellers can list items and potential buyers can purchase them. The dataset provided includes textual descriptions, categorical information, and other attributes related to the items. The challenge is to build a regression model that accurately predicts the price based on these features.

## EDA
The Exploratory Data Analysis (EDA) section explores the dataset to understand its structure, distributions, and relationships between variables. Key insights gained from EDA include:
- Distribution of price (log-transformed)
- Analysis of categorical variables like item condition, category, and brand
- Relationships between features and target variable (price)

## Feature Extraction
Feature extraction involves deriving new features from the existing dataset to improve model performance. Key steps in feature extraction include:
- Handling high categorical data using frequency encoding and noise injection
- Utilizing text data (name and item description) for feature engineering
- Imputing missing values and creating new features based on textual and categorical data

## Modeling
### Ridge Regression
Ridge Regression was chosen as a linear model due to its effectiveness with non-sparse data like text features. It was utilized both in preliminary feature extraction stages and final ensembling.

### LightGBM
LightGBM, a gradient boosting framework, was employed for its efficiency with large datasets and ability to handle categorical features without extensive preprocessing. It was the primary model for final predictions.

## Hyperparameter Tuning
Hyperparameter tuning was performed to optimize model performance for both Ridge Regression and LightGBM. Techniques used include:
- GridSearchCV for Ridge Regression
- Optuna for LightGBM, a Bayesian optimization framework, to find optimal hyperparameters

## Deployment
Deployment involves taking the trained model and making it ready for production use. Steps include:
- Serializing the trained model using pickle
- Creating a simple web service or script for predicting prices
- Deploying the model to a cloud platform or server

## Conclusion and Future Work
In conclusion, the project achieved competitive results in the Mercari Price Suggestion Challenge, achieving scores under the top 6 percentile on Kaggle. Future work could involve:
- Further improving model performance through advanced feature engineering
- Exploring ensemble methods and stacking to combine different models
- Enhancing deployment pipeline for real-time predictions

## References
- [Kaggle Mercari Price Suggestion Challenge](https://www.kaggle.com/c/mercari-price-suggestion-challenge)
- [Optuna Documentation](https://optuna.readthedocs.io/en/stable/index.html)
- [LightGBM Documentation](https://lightgbm.readthedocs.io/en/latest/)

This README.md file provides an overview of the project, methodology, and next steps. For detailed code and notebooks, please refer to the corresponding directories in this repository.

