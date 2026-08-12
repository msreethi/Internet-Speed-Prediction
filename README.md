# Internet Speed Prediction using Machine Learning

## 📌 Project Overview

Internet connectivity plays an important role in activities such as video
streaming, online gaming, video conferencing, cloud computing, and web
browsing. Internet speed can be influenced by various network-related factors.

This project develops a Machine Learning regression model to predict
**Internet Speed** using available network-related features.

The project follows an end-to-end Machine Learning workflow including:

- Exploratory Data Analysis (EDA)
- Feature Selection
- Data Preprocessing
- Regression Model Development
- Hyperparameter Tuning
- Model Evaluation
- Prediction on Unseen Data

---

## 🎯 Objective

The main objective of this project is to build a Machine Learning model that
can accurately predict Internet Speed based on network-related features.

Since Internet Speed is a continuous numerical value, this problem is treated
as a **Regression problem**.

---

## 🛠️ Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook / Google Colab

---

## 🤖 Machine Learning Models

Three regression algorithms were evaluated:

1. **Linear Regression**
2. **K-Nearest Neighbors (KNN) Regression**
3. **Support Vector Regression (SVR)**

The models were evaluated using:

- R² Score
- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)

---

## 📊 Model Performance

| Model | R² Score | MAE | RMSE |
|---|---:|---:|---:|
| KNN Regression | 99.86% | 26.31 Mbps | 34.65 Mbps |
| Linear Regression | 94.91% | 177.87 Mbps | 206.48 Mbps |
| SVR | 98.94% | 54.81 Mbps | 93.91 Mbps |

### 🏆 Best Model

**KNN Regression** achieved the best performance among the three models.

After hyperparameter tuning, the best KNN configuration was:

- Number of Neighbors: **9**
- Weight Function: **Distance**
- Algorithm: **Brute**

The final KNN model achieved an **R² score of 99.86%**.

---

## 🔍 Key Finding

Feature analysis showed that **Download_speed** was the dominant predictive
feature in the dataset.

The correlation between `Download_speed` and `Internet_speed` was
approximately **0.976**.

When `Download_speed` was removed, the KNN R² score dropped significantly,
showing that most of the predictive information in this dataset was contained
in this feature.

---

## 🧪 Prediction Example

The final KNN model was tested on an unseen observation.

- Actual Internet Speed: **1616.01 Mbps**
- Predicted Internet Speed: **1590.95 Mbps**
- Absolute Error: **25.06 Mbps**
- Approximate Error: **1.55%**

Dataset Source: https://www.kaggle.com/datasets/getanmolgupta01/internet-speed
