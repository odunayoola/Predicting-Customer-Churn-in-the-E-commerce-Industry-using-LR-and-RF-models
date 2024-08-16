# Predicting-Customer-Churn-in-the-E-commerce-Industry-using-LR-and-RF-models

# Customer Churn Prediction

This project aims to predict customer churn using machine learning techniques. The analysis includes data preprocessing, exploratory data analysis (EDA), and the evaluation of two machine learning models—Logistic Regression and Random Forest.

## Table of Contents

- [Project Overview](#project-overview)
- [Data Preprocessing](#data-preprocessing)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
  - [Target Variable Analysis](#target-variable-analysis)
  - [Demographic Factors](#demographic-factors)
  - [Customer Behavior](#customer-behavior)
  - [Customer Satisfaction](#customer-satisfaction)
- [Correlation Analysis](#correlation-analysis)
- [Feature Engineering](#feature-engineering)
- [Model Evaluation](#model-evaluation)
  - [Logistic Regression](#logistic-regression)
  - [Random Forest](#random-forest)
- [Model Comparison](#model-comparison)
- [Conclusion](#conclusion)
- [How to Run](#how-to-run)
- [Dependencies](#dependencies)
- [Contact](#contact)

## Project Overview

This project predicts customer churn by analyzing a dataset containing both categorical and numerical features. Two machine learning models, Logistic Regression and Random Forest, are developed, hyper-tuned, and evaluated based on accuracy, precision, recall, F1-score, and ROC AUC score.

## Data Preprocessing

- **Dataset**: Contains 5 categorical and 15 numerical features across 5630 rows.
- **Steps**:
  - Duplicates were checked and confirmed to be absent.
  - Missing values in features with more than 4% missing data were replaced with the mean of those features.
  - Outliers were identified and removed, and the new mean was recalculated to replace them.

## Exploratory Data Analysis (EDA)

### Target Variable Analysis

- **Churn Distribution**: The dataset exhibits a class imbalance, with 17% of customers labeled as 'Churn' and 83% as 'Retained'.

### Demographic Factors

- **City Tier**: Higher churn rates in Tier 1 cities.
- **Gender**: Higher churn among male customers (63%).
- **Marital Status**: Higher churn among single customers (51%).
- **Number of Addresses**: Higher churn among customers with 2-3 addresses.
- **Number of Devices**: Higher churn among customers with 3-5 devices.
- **Warehouse to Home Distance**: Churn is higher for distances between 5-16 miles.

### Customer Behavior

- **Tenure**: New customers show a higher churn rate.
- **Preferred Login Device**: Phone users show higher churn (66%).
- **Preferred Payment Method**: Debit and credit card users show higher churn.
- **Hours Spent on App**: Customers spending 3 hours on the app have a higher churn rate.
- **Preferred Order Category**: Mobile phone shoppers show higher churn.
- **Order Amount Hike from Last Year**: A 12% order hike shows the highest churn rate.
- **Coupon Used**: Customers using 1 coupon have a higher churn rate.
- **Order Count**: Customers with 2 or fewer orders show higher churn.
- **Days Since Last Order**: Higher churn among customers with recent orders (0-1 days).

### Customer Satisfaction

- **Satisfaction Score**: A score of 3.0 shows a higher churn rate.
- **Complaints**: 54% churn among customers who made complaints.

## Correlation Analysis

- **Key Findings**: Order count and coupon usage are highly correlated. To avoid multicollinearity, one feature was removed from the final model.

## Feature Engineering

- **Encoding**:
  - One-hot encoding for "Preferred Login Device" and "Gender".
  - Label encoding for "Marital Status," "Order Category," and "Preferred Payment Method".
- **Scaling**: Normalization was applied for feature scaling to enhance model performance.

## Model Evaluation

### Logistic Regression

- **Before Hyper-Tuning**:
  - Accuracy: 84%
  - Precision, Recall, F1-Score: Good for class 0, poor for class 1.
- **After Hyper-Tuning**:
  - Accuracy improved to 90%.
  - Significant improvements in recall for class 1.

### Random Forest

- **Before Hyper-Tuning**:
  - Accuracy: 96%
  - Strong performance across all metrics.
- **After Hyper-Tuning**:
  - Accuracy decreased to 88%, with trade-offs in precision and recall.
- **Final Model**:
  - After addressing overfitting, the final model achieved 96% accuracy, outperforming Logistic Regression.

## Model Comparison

The Random Forest model demonstrated superior performance across all key metrics, particularly after addressing overfitting. It outperformed Logistic Regression in predicting customer churn, especially for the minority class (class 1).

## Conclusion

- The Random Forest model is the preferred choice for predicting customer churn in this dataset, given its high accuracy and balanced performance across both classes.
- Logistic Regression, while improved after hyper-tuning, still underperformed compared to the Random Forest model.


Contact
For any inquiries or collaboration opportunities, feel free to contact me at odayoola@gmail.com



