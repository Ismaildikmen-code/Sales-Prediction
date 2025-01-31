# Sales Prediction Using LightGBM

This project demonstrates how to predict product sales using the LightGBM algorithm. The dataset contains sales data across different stores, countries, and products over several years. The objective is to predict the number of units sold based on historical data.

## Problem Statement
Predict the sales (`num_sold`) for different products in multiple stores across various countries. The task is to minimize the error between predicted and actual sales.

## Dataset
The dataset includes the following columns:
- **date**: Date of the sale
- **country**: Country where the sale occurred
- **store**: Store where the product was sold
- **product**: Product being sold
- **num_sold**: Number of units sold (target variable)

## Approach
1. **Data Preprocessing**:
   - Removed duplicates and missing values
   - Label encoded categorical features (`country`, `store`, `product`)
   - Applied log transformation to the target variable `num_sold`

2. **Model**:
   - LightGBM Regressor was used for sales prediction
   - Hyperparameter tuning was performed using GridSearchCV

3. **Evaluation**:
   - Mean Absolute Percentage Error (MAPE) was used for model evaluation
   - The final model achieved a test MAPE score of 0.142

## Installation
To run the code, you will need to install the following Python packages:

```bash
pip install lightgbm scikit-learn pandas numpy matplotlib
