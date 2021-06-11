# Project 2: 
# DSI-US-6 Project 2 Regression Challenge
## Predict the price of homes at sale for the Aimes Iowa Housing dataset

## Table of Contents:

### Part 1

1. Background
1. Problem Statement
1. Executive Summary
1. Data Cleaning
    1. Data Dictionary
1. Exploratory Data Analysis
1. Features Selection
    1. Quantitative
    1. Qualitative
    1. Summary
    
### Part 2
7. Modeling
    1. Base Case
1. Fine Tuning
    1. Model 1
    1. Model 2
    1. Model 3
    1. Model 4
    1. Model 5
    1. Final Model
1. Conclusion and Recommendations
1. References and Data Sources

## 1. Background

We are given a Kaggle challenge to build a regression model based on the Ames housing data to **predict** the **sale price** for each house in Aimes Iowa. The data given include a train dataset with sales price in it and a test dataset without sales price in it.

---
## 2. Problem Statement

To create a regression model that will predict the sale price for each house in Aimes Iowa. Using the train set to build the model and using the test set to test the RMSE score achieve by the model. The aim is to achieve the lowest RMSE on the test dataset. 

---
## 3. Executive Summary

From the RMSE of the different models, our best model is Model 5 which have a RMSE score of 22873 on our holding set and 24842 on the Kaggle Test set. This model is a Ridge Regression model with 19 features, polynomised the continuous and ordinate data to a order of 2 and one hot encode the nominal data. 

Our strategy on the EDA was to categorised the features into quantitative and qualitative data and then into similar characteristics like sizes and quality etc. For each group, we try to filter out the features which have little or no correlation with the SalePrice and also those which are not effective is categorizing the SalePrice into different ranges. We also look at the interaction between the features and if they are correlated with one another. 

We discover that year built, ground living area, total rooms of the house and value of miscellanous features impact the Sale price greatly. Newer, bigger ground living area and higher total rooms increase the Sale price. Surprisingly lot area doesn't add alot more value to the Sale price as much as the ground living area. Excellent external quality and overall quality also add value to the SalePrice. Bigger garage area and bulit-in garage type and new sale type also contribute greatly to increase the SalePrice. Homeowners who are looking to increase their sale price can renovate a built in garage and improve the quality of their exterior material. The neighbourhoods with higher SalePrice are Stone Brook and Northridge

From our base model,we notice that our predicted y underpredict for the range y more than 300,000. Also when we were doing EDA, a portion of the features show heteroskedasticity so we suspect interaction between the features which we try to linearise by using log y and adding polynominal features of order 2. We also used Ridge Regression to regularize the extra features in set 2. Both these help to reduce our RSME scores greatly.

---
## Data Dictionary

https://www.kaggle.com/c/dsi-us-6-project-2-regression-challenge/data

---
## Models and RMSE Score

| Model    |              | RMSE  | Features | Linear Model | Hyper Parameter | Preprocessing |     |        |       |
|---------:|--------------|-------|----------|--------------|-----------------|:-------------:|-----|--------|-------|
|          |              |       |          |              |                 | Poly          | OHE | Target | Log y |
| Baseline | Train        | 29983 | 1        | LR           |                 |               | Y   |        |       |
|          | Hold         | 32617 |          |              |                 |               |     |        |       |
| Model 1  | Train        | 25514 | 1        | LR           |                 |               | Y   |        | Y     |
|          | Hold         | 27129 |          |              |                 |               |     |        |       |
| Model 2  | Train        | 25037 | 1        | LR           |                 | Y             | Y   |        |       |
|          | Hold         | 26179 |          |              |                 |               |     |        |       |
| Model 3  | Train        | 26141 | 1        | Lasso        | 65.38           | Y             | Y   |        |       |
|          | Hold         | 26178 |          |              |                 |               |     |        |       |
| Model 4  | Train        | 25495 | 1        | Ridge        | 11.89           | Y             | Y   |        |       |
|          | Hold         | 26019 |          |              |                 |               |     |        |       |
| Model 5  | Train        | 22180 | 2        | Ridge        | 33.7            | Y             | Y   |        |       |
|          | Hold         | 22873 |          |              |                 |               |     |        |       |
|          | Train + Hold | 22018 |          |              | 27.364          |               |     |        |       |
|          | Test         | 24842 |          |              |                 |               |     |        |       |
