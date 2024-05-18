# Churn Prediction Phase_3_Project

## Introduction
This project aims to predict customer churn in a telecom company using machine learning techniques. Customer churn refers to the loss of customers over a specified period. Identifying churn allows businesses to take proactive measures to retain customers and improve customer satisfaction.

## Table of Contents
- [Introduction](#Introduction)
- [Features](#Features)
- [Data](#data)
- [Model Training and Evaluation](#model-training-and-evaluation)
- [Results](#results)
- [For more Information](#For-more-Information)


## Features
Churn Prediction: Predict whether a customer will churn based on their demographics, account information, and usage patterns.
Model Evaluation: Compare multiple models and select the best one based on performance metrics.
Data Preprocessing: Handle missing values, categorical variables

## Data
The dataset was obtained from https://www.kaggle.com/datasets/becksddf/churn-in-telecoms-dataset

It contains customer data with the following attributes:

- state: The state of the customer,

- account length: The length of the account in days or months,

- area code: The area code of the customer's phone number,

- phone number: The phone number of the customer,

- international plan: Whether the customer has an international plan or not,

- voice mail plan: Whether the customer has a voicemail plan or not,

- number vmail messages: The number of voicemail messages the customer has,

- otal day minutes: Total minutes of day calls,

- total day calls: Total number of day calls,

- total day charge: Total charge for the day calls,

- total eve minutes: Total minutes of evening calls,

- total eve calls: Total number of evening calls,

- total eve charge: Total charge for the evening calls,

- total night minutes: Total minutes of night calls,

- total night calls: Total number of night calls,

- total night charge: Total charge for the night calls,

- total intl minutes: Total minutes of international calls,

- total intl calls: Total number of international calls,

- total intl charge: Total charge for the international calls,

- customer service calls: Number of times the customer called customer service,

- churn: Whether the customer churned or not (True/False).

#### Data processing
The data was evaluated for missing values and duplicates
The columns international plan and Voice mail plan were converted from string to boolean after which a correlation between the varibles were established to assist is feature selection. Below is a correlation matrix showing the relationship between the features.
![image](https://github.com/Bkiambuthi/Phase_3_Project/assets/67098705/60936a86-2048-4f68-a222-4b3b602ad2fa)


## Model Training and Evaluation
#### Models Used
I explored various machine learning models to predict the customer churn:

##### Logistic Regression:
A linear model used for binary classification that predicts the probability of the target variable belonging to a particular class.
Suitable for understanding the impact of predictor variables.

##### Decision Tree:
A non-linear model that splits the data into subsets based on the value of input features, leading to a tree-like structure of decisions.
Easy to interpret and visualize.

##### K-Nearest Neighbors (KNN):
A non-parametric model that classifies instances based on the majority class among the k-nearest neighbors.
Effective for small datasets and non-linear decision boundaries.

##### Random Forest:
An ensemble model that creates multiple decision trees using different subsets of data and features, and averages their predictions.
Robust to overfitting and provides high accuracy.

#### Training Process
##### Data Splitting:
- The dataset was split into training and testing sets using an 75-25 split to ensure that the model's performance could be evaluated on unseen data.
- The training and test data sets for the independent variables were standardised using z-score normalization.
- Each model was trained using the standardised training data.

#### Evaluation Metrics
I used below metrics to assess the performance of the models:

##### Accuracy:
Measures the proportion of correctly classified instances out of the total instances.
Useful for getting a general sense of performance but can be misleading with imbalanced datasets.
##### Recall (Sensitivity):
Measures the model's ability to identify all relevant instances (true positives).
Important for minimizing false negatives, especially in churn prediction where retaining customers is crucial.
##### Precision:
Measures the proportion of positive identifications that are actually correct.
Important for minimizing false positives to avoid unnecessary retention efforts.
##### F1 Score:
The harmonic mean of precision and recall, providing a balanced measure of both metrics.
Useful for assessing models when both false positives and false negatives are important.

## Results
After evaluating all the models, the Random Forest Classifier emerged as the best performing model with the following metrics:
- Accuracy: 0.900
- Recall: 0.479
- Precision: 0.764
- F1 Score: 0.581
These metrics indicate that the Random Forest model has a good balance between identifying actual churners (recall) and correctly predicting churn (precision), making it the most effective model for predicting customer churn in our dataset.
Below is the confussion matrix for the Random Forest Classifier model on the test data
![image](https://github.com/Bkiambuthi/Phase_3_Project/assets/67098705/de10eda8-2c28-41d6-9533-e8cd38cd0e02)

### For More Information
Notebook [https://github.com/Bkiambuthi/Phase_3_Project/blob/main/Phase_3_Project.ipynb](https://github.com/Bkiambuthi/Phase_3_Project/blob/main/notebook.ipynb)
Presentation 
