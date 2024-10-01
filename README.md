# ML-Data-Cleaning-and-Feature-Selection
This project involves data preprocessing, exploratory data analysis, and predictive modeling using machine learning algorithms. The goal is to predict the Retention Ratio from a dataset of insurance-related variables. Various methods, including feature selection, data imputation, and model evaluation, are used to improve prediction accuracy.

---

## Author: Charmi Parmar  
**NUID**: 002766700

---

## Overview
This repository contains the code and analysis for Data Science and Engineering Management Techniques (DSEMT) Assignment 1. The assignment focuses on exploratory data analysis, feature selection, data imputation, and model training to predict the target variable `RETENTION_RATIO`.

---

## Requirements

- Python 3.x
- Libraries:
  - numpy
  - pandas
  - seaborn
  - matplotlib
  - statsmodels
  - category_encoders
  - sklearn
  - eli5
  - skfeature-chappers (for feature selection)

---

## Contents

### 1. **Data Import and Exploration**
- **Data Import**: The dataset is loaded from a CSV file and inspected for the first few rows using `data.head()`.
- **Missing Values**: Checked for missing values in the dataset using `data.isnull().sum()`.
- **Dataset Information**: Data types and basic statistics are retrieved using `data.info()` and `data.describe()`.

### 2. **Data Preprocessing**
- **Normalization**: Numerical columns were selected and visualized using Q-Q plots for understanding data distribution.
- **Target Variable Transformation**: The `RETENTION_RATIO` is converted into three categorical bins (low, average, high) for easier interpretation.
- **Data Sampling**: A 10% sample of the dataset is selected for faster computation.

### 3. **Feature Encoding and Selection**
- **Categorical Encoding**: Categorical features are encoded using Leave-One-Out Encoder (`category_encoders`) to handle high cardinality.
- **Filter Method - Mutual Information**: Features were selected using Mutual Information to reduce the dataset's dimensionality to the top 20 features.
- **Second Feature Selection Method**: Fisher Score was used as another method for selecting important features.

### 4. **Exploratory Data Analysis**
- **Correlation Matrix**: A heatmap is created to show the correlation between selected features and the target variable.
- **Pair Plot**: Visualized relationships between numerical variables using seaborn’s pair plot.
  
### 5. **Model Training**
- **Random Forest Model**: A RandomForestRegressor model is trained on the selected features and evaluated using R-Squared.
- **Logistic Regression Model**: A Logistic Regression model is trained and evaluated using confusion matrix, accuracy, precision, recall, and F1 scores.

### 6. **Data Imputation**
- **Missing Data Creation**: Missing data is artificially introduced for selected columns at 1%, 5%, and 10% levels for testing imputation methods.
- **Mean Imputation**: Missing values are filled using the mean method, and percentage changes are calculated for accuracy.
- **KNN Imputation**: KNN Imputer is used to fill missing data, and percentage changes in the imputed values are analyzed.

### 7. **Model Evaluation**
- **Confusion Matrix**: Visualized the confusion matrix of the Logistic Regression model predictions.
- **Metrics**: Model performance is evaluated using metrics such as Mean Squared Error, accuracy, precision, recall, and F1 score.

### 8. **Q-Q Plot and Distribution Analysis**
- **Q-Q Plot**: Generated Q-Q plots for each numerical column to check for normality.
- **Distributions**: Distribution histograms and Anderson-Darling tests were used to assess the distribution types of numerical columns.

### 9. **Feature Importance**
- **Random Forest Feature Importance**: The most important predictor variables were identified and ranked using feature importance from RandomForestRegressor.

---

## Conclusion
The analysis successfully applied feature selection, imputation methods, and machine learning models to predict the `RETENTION_RATIO`. Various techniques like Random Forest, Logistic Regression, and KNN Imputation were employed to handle and analyze the data effectively.

---

## License
This project is licensed under the MIT License.

---
