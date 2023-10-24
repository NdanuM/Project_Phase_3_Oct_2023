# Bank Customers Attrition Prediction Presentation
<img src="image_investment-5318530_1280.jpg" width="400" height="50" align="left">

Author: Ndanu Mwatu

## Overview
This project focuses on solving a business problem using classification models through  an iterative approach. 

## Business  Problem
ABC Multinational Bank is concerned over high customer attrition rates. They seek a solution via a classification model to predict customer turnover - in order to apply mitigation measures beforehand.

## Data Understanding
This project uses account holders’ data for  ABC Multinational Bank customers, downloaded from Kaggle.
It comprises of 10,000 rows and 12 feature columns including; credit score, country, age, balance, estimated salary and churn (the target variable).

## Preprocessing/ Preparation of Data
This stage includes;
Defining X (predictors) and y (target); Splitting the data into training and test sets; Checking for missing values; One hot encoding categorical data  and Normalizing/standardizing numeric features.

Data leakage: Preprocessing is done after splitting the data into train and test sets -  to prevent data leakage.

## Data Modeling and Evaluation
3 types of models are built as listed below;
1. Logistic regression models
2.Decision Trees models
3. Random Forest models

**An iterative approach is followed in the following fashion;**
i. Logistic Regression Modelling
    -Establish Baseline Logistic Regression model
    -Create Iterative Logistic Regression models - and determine the best one 
ii. Decision Trees Modelling
    -Establish Baseline Decision Tree model
    -Create Iterative Decision Tree models - and determine the best one 
iii. Random Forest Modelling
    -Establish Baseline Random Forest model
    -Create Optimal Random Forest Iterative Model - using GridSearchCV
    -Investigate Feature Importances of the Random Forest Models
iv. Evaluate the Overall Best Model

## Results
