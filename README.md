# House Sale Price Prediction

### Predictive Modeling to Optimize Real Estate Listing Prices

## 1. Project Overview

This project was developed for RealAgents, a real estate company aiming to **optimize its listing prices** to reduce the time houses spend on the market. The core objective is to build a Machine Learning model that accurately predicts a house's final sale price based on its characteristics.

This repository contains the complete analysis, documented in the **House_Sales_Prediction.ipynb** Jupyter Notebook.

## 2. Technical Stack (Ferramentas Utilizadas)

* **Language:** Python
* **Libraries:** Pandas (for data handling), Scikit-learn (for machine learning models), Matplotlib (for data visualization).

## 3. Methodology and Key Findings

The project followed a standard data science pipeline:

### 3.1 Data Cleaning and Preparation (Data Wrangling)
This initial phase focused on ensuring data quality. Key steps included:
* Handling missing values through imputation (filling gaps with the mean or most common value) for columns like `months_listed` and `area`.
* Standardizing categorical text data (like abbreviations in `house_type`) and replacing non-standard missing values (like `--` in the `city` column).

### 3.2 Exploratory Data Analysis (EDA)
We investigated the relationship between the house features and the sale price.
* **Key Insight:** Analysis confirmed the business team's hypothesis: the **number of bedrooms** is the primary driver of the house price, showing a clear, linear increase.
* The analysis also showed that the **price variance** (how much prices differ) is much higher for larger houses, suggesting other factors like `city` and `area` are very important for high-value properties.

### 3.3 Predictive Modeling
We compared two types of Regression models:

* **Baseline Model:** Simple Linear Regression, using only the `bedrooms` feature. This gives us a basic performance score to measure future improvements against.
* **Comparison Model:** **Random Forest Regressor**. This more advanced model was used because it handles complex, non-linear relationships well. We used Scikit-learn **Pipelines** to automatically manage data preparation (like transforming text categories into numerical values) before training the model.

