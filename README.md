# Bank Customers Attrition Prediction Presentation
Author: Ndanu Mwatu

![image](https://github.com/NdanuM/Project_Phase_3_Oct_2023/assets/133153210/f98fd4cf-dce0-460a-acd9-a0f7cacf9e4f)
Image by Tumisu from Pixabay


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
2. Decision Trees models
3. Random Forest models

**An iterative approach is followed in the following fashion;**

i. Logistic Regression Modelling
* Establish Baseline Logistic Regression model
* Create Iterative Logistic Regression models - and determine the best one 
ii. Decision Trees Modelling
* Establish Baseline Decision Tree model
    -Create Iterative Decision Tree models - and determine the best one 
iii. Random Forest Modelling
    -Establish Baseline Random Forest model
    -Create Optimal Random Forest Iterative Model - using GridSearchCV
    -Investigate Feature Importances of the Random Forest Models
iv. Evaluate the Overall Best Model

## Results
![image](https://github.com/NdanuM/Project_Phase_3_Oct_2023/assets/133153210/74e8678c-e29c-4e03-b9b3-88822a01c605)
Image by ar130405 from Pixabay

**Logistic Regression Modelling:** 
Best Performing model has;
* Log loss: 0.433
* Parameters: 
       - Scaled data
       - Increased regularization 
       - 'Saga' solver
  
**Decision Trees Modelling:**
Best Performing model has;
* Log loss: 0.406
* Parameters: 
        -Max_depth=6
        -Min_samples_split=91 
        -Min_samples_leaf=16

**Random Forests Modelling:**
Best Performing model has;
* Log loss: 0.36
* Parameters: 
        -Criterion='entropy'
        -Max_depth=9
        -Min_samples_leaf=16
        -Min_samples_split=91
        -n_estimators=100

**Feature Importance for Random Forest Model**

![image](https://github.com/NdanuM/Project_Phase_3_Oct_2023/assets/133153210/42bec559-78a3-4625-94be-1907038920ad)

Age is the feature with highest importance.

**Results: Overall Best Model Evaluation - Optimal Random Forest Model**

Training Precision:  0.866; 
Testing Precision:  0.8591

Training Recall:  0.394; 
Testing Recall:  0.380

Training Accuracy:  0.863; 
Testing Accuracy:  0.864

Training F1-Score:  0.541; 
Testing F1-Score:  0.527

## Conclusions/ Recommendations
1. The client  advised to make use of the overall best model to predict customers that are likely to leave the Bank and target intervention strategies. 

2. This model may not be sufficient to decide on best candidates for provision of loans, thus the client should be cautious in utilising it as such.

3. The client advised to pay attention to age of customers, credit_score, estimated salary and balance as features of importance when designing intervention strategies to retain customers.

## Next Steps
For additional insights, further analysis is proposed in the following areas;
* Further tuning is proposed of the hyperparameters of the best performing model in order to lead to better performance metrics particularly the f1 Score. This further analysis could include use of XGBoost.
* Adjustment of the model's Recall and Precision could be done in line with the focus of the Bank. A further discussion with the Bank to understand their needs and focus is needed e.g. are the intervention measures likely to be too costly, in which case, the client would want a model that is even more precise?




### For More Information
See the full analysis in the Jupyter Notebook.

For additional information contact Mwatu.Ndanu@student.moringaschool.com

### Repository Structure
* Bank_Customers_Attrition_Prediction.ipynb
* Bank_Customers_Attrition_Prediction_Presentation.pdf
* data
* images
* README.md




### References
Images *(that are not visualizations generated from data)* are downloaded from www.pixabay.com
