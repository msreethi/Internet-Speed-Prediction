# Internet-Speed-Prediction
End-to-end Internet Speed Prediction using Python and machine learning, comparing KNN, Linear Regression, and SVR to identify the best-performing regression model.
# Internet Speed Prediction Using Machine Learning

## Project Overview

This project uses machine learning regression algorithms to predict internet speed based on network-related features.

The project includes:

- Exploratory Data Analysis (EDA)
- Data preprocessing
- Feature selection
- Regression model development
- Hyperparameter tuning
- Model evaluation
- Prediction on unseen test data

## Models Used

Three regression algorithms were evaluated:

1. Linear Regression
2. K-Nearest Neighbors Regression (KNN)
3. Support Vector Regression (SVR)

## Model Performance

| Model | R² Score | MAE | RMSE |
|---|---:|---:|---:|
| KNN | 99.86% | 26.31 | 34.65 |
| Linear Regression | 94.91% | 177.87 | 206.48 |
| SVR | ~77% | ~280.34 | ~433.24 |

## Best Model

KNN Regression was selected as the best-performing model.

Best parameters:

- n_neighbors = 9
- weights = distance
- algorithm = auto

### Final KNN Performance

- R² Score: 99.86%
- MAE: 26.31 Mbps
- RMSE: 34.65 Mbps

## Unseen Data Prediction

For one unseen test observation:

- Actual Internet Speed: 1616.01 Mbps
- Predicted Internet Speed: 1590.95 Mbps
- Prediction Error: 25.06 Mbps
- Percentage Error: approximately 1.55%

## Feature Analysis

Download_speed showed a very strong correlation with Internet_speed:

Correlation = 0.975699

When Download_speed was removed, KNN performance decreased substantially:

- R² = -12.89%
- MAE = 834.54 Mbps
- RMSE = 988.39 Mbps

This indicates that Download_speed contains most of the predictive information in this dataset.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook
