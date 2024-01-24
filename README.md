# Project Name
> Assignment - Advanced Regression_Surprise Housing _Australian market. 
The company uses data analytics to purchase houses at a price below their actual values and flip them on at a higher price.


## Overview
This project aims to predict house prices in the Australian market for Surprise Housing, a US-based housing company. Using data analytics, the company seeks to purchase houses below their actual values and sell them for a profit. 
The focus is on building a regression model to predict house values and identify significant variables influencing these prices.

## Problem Statement
Surprise Housing intends to understand the Australian housing market's pricing dynamics. 
The objective is to model house prices with available variables, helping the management devise strategies for high-return investments.

## Data Preparation
Data Import and Cleaning: Loaded the housing dataset and performed initial inspections. Addressed missing values in columns like 'LotFrontage', 'Alley', and 'PoolQC' using appropriate imputation strategies.
Feature Engineering: Established correlations between features like 'LotFrontage' and 'MSZoning'. Implemented median imputation and created intuitive encodings for categorical variables.
Correlation Analysis: Analyzed the correlation matrix of numerical features, dropping highly correlated pairs to reduce multicollinearity.
Dummy Variable Creation: Generated dummy variables for categorical features, excluding redundant columns to streamline the dataset.

## Analysis
Exploratory Data Analysis (EDA): Conducted box plots and scatter plots to visualize relationships between various features and the target variable 'SalePrice'.
Feature Selection: Applied Recursive Feature Elimination (RFE) to select the most relevant features. Used cross-validation to assess the model's performance.

## Model Development
Data Splitting & Scaling: Divided data into a 70-30 train-test split and applied Min-Max scaling to numerical features.
Linear Regression: First, built a linear regression model, observing overfitting issues indicated by varying R2 scores.
Ridge Regression: Implemented Ridge regression with hyperparameter tuning using GridSearchCV. Determined the optimal alpha value and evaluated the model's performance.
Lasso Regression: Similarly, applied Lasso regression, again using GridSearchCV for alpha tuning. Compared metrics like R2, RSS, and MSE with the Ridge model.


## Conclusion
Model Selection: Chose Lasso Regression as the preferred model due to its slightly better performance in terms of R2 scores and error metrics. Train = 0.897, Test = 0.872
Significant Features: Identified the most influential features impacting house prices, providing insights for strategic decisions in the Australian housing market.

## Dependencies
This analysis utilized libraries such as NumPy, Pandas, Matplotlib, Seaborn, and Scikit-learn for data handling, visualization, and modeling.