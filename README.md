# GCP-Predict_Coronary_Heart_Disease

# Objective 
Predict Coronary Heart Disease from patients within 10 years of examination.

# Dataset 
Kaggle Dataset :  https://www.kaggle.com/datasets/mahdifaour/heart-disease-dataset

# Business Impact
1) Reduce CHD-related healthcare costs by implementing proactive and preventive measures.
2) Improve patient outcomes by identifying at-risk individuals early and implementing timely interventions.

# Data Preprocessing
## Missing values  
8 variables have missing values
education : Missing value is replaced by a new value ‘5’ and considered as a separate category.
cigsPerDay
BPMeds
totChol
BMI
heartRate
glucose
a1c
Rest all variables are filled with median

## Feature Selection
Drop the following variables:
1) ‘income’ : Strong positive skewed variable. Performed log transformation and created a new feature ‘income_log’
2) ‘glucose’ : Highly correlated with ‘a1c’ variable

## Feature Engineering
1) Log-transform ‘income’ due to strong positive skew and create a new variable ‘income_log’
2) Perform one-hot encoding on ‘education’ as it can be treated as nominal feature
3) Perform Winsorisation to handle outliers on below features. Outliers that exceed the upper bound are replaced with the value at the upper bound, while outliers below the lower bound are replaced with the value at the lower bound.
		'a1c', 'cigsPerDay', 'income_log', 'totChol', 'sysBP',  'BMI'
4) Perform Feature Scaling to standardize the features.
5) Perform SMOTE oversampling due to unbalanced dataset on training data

##Pipeline
Build 2 pipelines for Model Pipeline and Inference Pipeline











