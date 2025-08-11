# Heart Disease Classification Project

## Introduction

This project aims to build a machine learning model to predict the presence of heart disease based on clinical data. Using a dataset of patient attributes such as age, chest pain type, blood pressure, cholesterol levels, and more, the goal is to accurately classify patients with and without heart disease to assist early diagnosis.

## Dataset

The dataset includes 13 clinical features:
- Age
- Sex
- Chest pain type (cp)
- Resting blood pressure (trestbps)
- Serum cholesterol (chol)
- Fasting blood sugar (fbs)
- Resting electrocardiographic results (restecg)
- Maximum heart rate achieved (thalach)
- Exercise induced angina (exang)
- ST depression induced by exercise relative to rest (oldpeak)
- Slope of the peak exercise ST segment (slope)
- Number of major vessels colored by fluoroscopy (ca)
- Thalassemia (thal)

The target variable is the presence (1) or absence (0) of heart disease.

## Methodology

- Data preprocessing and feature engineering were performed.
- Three machine learning models were tested:
  1. Logistic Regression
  2. K-Nearest Neighbors Classifier (KNN)
  3. Random Forest Classifier
- Hyperparameter tuning was conducted using `RandomizedSearchCV` and `GridSearchCV`.
- Model evaluation was performed using accuracy, recall, precision, F1-score, confusion matrix, ROC curve, and AUC.
- Cross-validation was used to assess model stability.

## Results

- Logistic Regression with hyperparameter tuning achieved:
  - Accuracy: 88%
  - Recall (Sensitivity): 91%
  - Precision: 88%
  - AUC: 0.93
- Random Forest also performed well with an AUC close to logistic regression.
- KNN showed moderate performance with optimal neighbors around 10-12.
- Feature importance analysis revealed key predictors of heart disease.

## Feature Importance

The logistic regression coefficients indicated important features such as chest pain type, exercise-induced angina, and resting ECG results as positive contributors, while age, oldpeak, number of vessels, and thalassemia negatively influenced the prediction.

## Conclusion

The tuned logistic regression model demonstrated strong predictive performance in distinguishing heart disease presence using 13 clinical features. This model could serve as a helpful tool for early diagnosis and risk stratification in clinical settings. Further improvements could involve testing additional models, incorporating more features, and validating in prospective studies.

