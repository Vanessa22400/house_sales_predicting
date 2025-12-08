# House Price Prediction: Machine Learning Project

This project applies machine learning techniques to predict residential property sale prices.  
It follows a clear, end-to-end structure: data cleaning, exploratory analysis, baseline modeling, and the development of a more robust model using tree-based methods.

The goal is to build a practical, interpretable solution while demonstrating essential skills for tabular data projects.

---

## 1. Project Overview

The dataset contains typical real estate features, including:

- City  
- Number of bedrooms  
- House type  
- Area (in square meters)  
- Months listed  

Two models were used:

- **Linear Regression** (baseline)
- **Random Forest Regressor**

The baseline model helps establish a starting point, while the Random Forest tests whether a more flexible approach can improve performance.

---

## 2. Technologies Used

- Python  
- Pandas, NumPy  
- Matplotlib / Seaborn  
- Scikit-Learn  

---

## 3. Data Cleaning & Preparation

The notebook performs several steps to make the dataset modeling-ready:

- Converts the `sale_date` column to datetime  
- Cleans the `area` column (removing text and converting to float)  
- Standardizes `house_type` names  
- Replaces placeholder `city` values with `"Unknown"`  
- Fills missing values (e.g., median for `months_listed`)  
- Converts all numeric columns to the correct dtype  

A preprocessing pipeline was then created to:

- Impute numerical features with the mean  
- Impute categorical features with `"Unknown"`  
- Apply one-hot encoding  

This ensures the feature engineering stays consistent across models.

---

## 4. Exploratory Data Analysis

The analysis includes:

- Distribution of the target variable (`sale_price`)
- Relationship between bedrooms and price  
- Correlations among numerical features  
- Basic trends within cities and house types  

This helps understand the structure of the data before modeling.

---

## 5. Modeling

### Baseline Model — Linear Regression  
Used as a reference to evaluate whether more advanced models offer meaningful improvements.

### Main Model — Random Forest Regressor  
A more flexible model that captures non-linear relationships and feature interactions.  
Both models were trained using the same preprocessing pipeline.

---

## 6. Results

Evaluation metric: **RMSE (Root Mean Squared Error)**

| Model                        | RMSE        |
|-----------------------------:|------------:|
| Linear Regression (Baseline) | 22,077.66   |
| Random Forest Regressor      | 17,470.93   |

### Interpretation

- The Random Forest model achieves a significantly lower error.  
- This shows that the dataset contains non-linear patterns that Linear Regression cannot capture.  
- For this task, the Random Forest is the preferred model.

---

## 7. Future Improvements

Possible next steps include:

- Adding engineered features (e.g., price per m², city averages)
- Trying gradient boosting models (XGBoost, LightGBM, CatBoost)
- Running hyperparameter tuning
- Applying cross-validation
- Using model interpretability tools (feature importance, SHAP values)


