# Housing Price Prediction: Machine Learning Model Comparison

## Overview

This project examines how accurately different statistical, machine learning, and deep learning models can predict residential sale prices using the Ames Housing dataset.

The goal was to compare several predictive approaches, identify the model with the strongest performance, and determine which property characteristics had the greatest influence on housing prices.

## Data

The analysis used the Ames Housing dataset, which contains detailed information about residential properties, including their size, quality, age, location, garage features, basement characteristics, and final sale price.

The data was divided into training and testing sets using an 80/20 split. The training set was used for exploratory analysis, preprocessing, model development, and model comparison, while the test set was reserved for the final evaluation.

Two additional variables were created:

- `Age`, representing the age of the property when it was sold
- `Has_Garage`, indicating whether the property had a garage

Because sale prices were strongly right-skewed, the target variable was transformed using the natural logarithm before model development.

## Methods

The analysis was conducted in Python using:

- Exploratory data analysis
- Missing-value imputation
- Feature engineering
- Numerical feature standardization
- One-hot encoding
- Cross-validation
- Hyperparameter tuning
- Model diagnostics
- Feature-importance analysis

The following models were evaluated:

- Linear Regression
- Ridge Regression
- Lasso Regression
- Decision Tree Regression
- Random Forest Regression
- XGBoost Regression
- K-Nearest Neighbors Regression
- Deep Learning

Root mean squared error, or RMSE, was used as the primary model-comparison metric. Lower RMSE values indicated stronger predictive performance.

## Key Findings

- XGBoost achieved the strongest validation performance among the models evaluated.
- The final XGBoost model achieved a test log RMSE of **0.1110**.
- Its predictions differed from actual sale prices by approximately **$14,775 on average**.
- The model achieved a mean absolute percentage error of approximately **8.11%**.
- Random Forest and Ridge Regression also produced strong results.
- The single Decision Tree and deep learning model performed less effectively than the other approaches.
- The model was most accurate for homes in the lower and middle price ranges.
- Prediction errors were larger for some high-value properties.
- Overall quality, exterior quality, property age, garage capacity, and above-ground living area were among the most influential features.

Overall, the results suggest that tree-based ensemble methods were well suited to capturing the nonlinear relationships and interactions found in the housing data. :contentReference[oaicite:1]{index=1}

## Tools

- Python
- Jupyter Notebook
- pandas
- NumPy
- Matplotlib
- Seaborn
- scikit-learn
- XGBoost
- TensorFlow / Keras

## Project Files

- `ames_housing_prediction.ipynb` — Complete analysis with code and output
- `ames_housing_results.pdf` — Results-focused report
- `README.md` — Project overview and key findings

## Data Availability

The Ames Housing dataset is publicly available and was accessed through OpenML using Python’s `fetch_openml()` function.

The dataset is not included directly in this repository because it can be downloaded automatically when the notebook is executed.
