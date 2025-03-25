# MLAI11.1
ML/AI assignment 11.1

Used Car Price Modeling – Assignment 1.11
Overview
This project explores a dataset of used vehicle listings with the goal of identifying which features most influence a car's price. The original dataset included numerous columns with missing or inconsistent data. To simplify the analysis and focus on interpretability, we selected only the numeric features most likely to impact price: year and odometer.

Data Preparation
Loaded and inspected a dataset of over 426,000 used vehicle listings

Dropped all rows with missing values for a clean dataset

Selected the following columns for modeling:

price (target variable)

year (vehicle year)

odometer (vehicle mileage)

Modeling Approach
A simple multivariate linear regression was performed using:

Independent variables: year, odometer

Target variable: price

The dataset was split into:

80% training

20% testing

Results
Metric	Value
MAE	$9,512.28
MSE	178,889,826.49
The mean absolute error suggests that, on average, predictions are within ~$9,500 of the actual price. The high mean squared error is expected due to a wide range of car prices and possible outliers in the data.

Feature Importance
Based on the coefficients of the linear regression model:

year had a positive impact on price — newer cars tend to be more expensive.

odometer had a negative impact on price — more mileage generally decreases value.

This aligns with common expectations in the used car market.

Next Steps (if continuing)
Handle outliers (e.g., cars priced at $0 or over $100K)

Reintroduce selected categorical variables with one-hot encoding

Experiment with more complex models (e.g., random forest) for non-linear relationships

