# ₿ Bitcoin Price Movement Prediction using Machine Learning

## 📌 Project Overview

This project focuses on predicting the **next-day Bitcoin price movement** using historical cryptocurrency market data and machine learning techniques.

The objective is to analyze Bitcoin trading patterns, engineer meaningful features from market indicators, and build classification models capable of predicting whether the Bitcoin closing price will increase or decrease on the following day.

The project demonstrates an end-to-end machine learning workflow including:

* Data Cleaning and Preprocessing
* Exploratory Data Analysis (EDA)
* Feature Engineering
* Model Training and Evaluation
* Performance Comparison of Multiple Algorithms

---

## 🎯 Business Problem

Cryptocurrency markets are highly volatile and influenced by multiple factors. Investors and traders often seek predictive insights to support trading decisions.

This project aims to answer:

> **Can historical Bitcoin market data be used to predict whether the price will rise or fall on the next trading day?**

---

## 📂 Dataset

The dataset contains historical Bitcoin trading information including:

| Feature | Description                  |
| ------- | ---------------------------- |
| Date    | Trading date                 |
| Open    | Opening price                |
| High    | Highest price during the day |
| Low     | Lowest price during the day  |
| Close   | Closing price                |
| Volume  | Trading volume               |

---

## 🛠 Technologies Used

### Programming Language

* Python

### Libraries

* NumPy
* Pandas
* Matplotlib
* Seaborn

### Machine Learning

* Scikit-Learn
* XGBoost

### Models

* Logistic Regression
* Support Vector Machine (SVM)
* XGBoost Classifier

### Development Environment

* Google Colab

---

## 🔍 Exploratory Data Analysis (EDA)

Several visual analyses were performed to understand market behavior:

### Data Inspection

* Dataset shape and structure
* Statistical summaries
* Missing value analysis

### Visualizations

* Bitcoin closing price trend
* Feature distributions
* Outlier detection using boxplots
* Correlation analysis using heatmaps
* Year-wise price trend comparison

These analyses helped identify important patterns and relationships among market variables.

---

## ⚙️ Feature Engineering

To improve predictive performance, new features were created:

### Market Spread Features

```python
open-close = Open - Close
low-high = Low - High
```

These features capture intraday price movement and volatility.

### Quarter-End Indicator

```python
is_quarter_end = 1 if month % 3 == 0 else 0
```

Used to identify possible market behavior changes around quarter-end periods.

### Target Variable

```python
target = 1 if Next Day Close > Current Day Close
target = 0 otherwise
```

This transforms the problem into a binary classification task.

---

## 🧠 Machine Learning Pipeline

### Data Preparation

* Feature scaling using StandardScaler
* Train-Test Split (70% Training / 30% Validation)

### Models Trained

#### Logistic Regression

A baseline classification model used for interpretability and performance comparison.

#### Support Vector Machine (SVM)

Polynomial kernel SVM used to capture non-linear relationships in the data.

#### XGBoost Classifier

Gradient boosting model designed for high predictive accuracy and robust performance.

---

## 📊 Model Evaluation

Models were evaluated using:

### ROC-AUC Score

The Receiver Operating Characteristic – Area Under Curve (ROC-AUC) metric was used to measure classification performance.

Evaluation was performed on:

* Training Dataset
* Validation Dataset

### Confusion Matrix

A confusion matrix was generated to analyze:

* Correct Predictions
* False Positives
* False Negatives

This provided a detailed understanding of model classification behavior.

---

## 📈 Key Insights

* Bitcoin price movements exhibit identifiable patterns through engineered features.
* Market spread indicators contributed valuable predictive information.
* Feature scaling improved model stability.
* Advanced ensemble methods such as XGBoost demonstrated strong predictive capability.
* Classification models can provide useful signals for short-term market direction forecasting.

---

## 🏗 Project Workflow

```text
Data Collection
       │
       ▼
Data Cleaning
       │
       ▼
Exploratory Data Analysis
       │
       ▼
Feature Engineering
       │
       ▼
Feature Scaling
       │
       ▼
Train-Test Split
       │
       ▼
Model Training
(Logistic Regression, SVM, XGBoost)
       │
       ▼
Performance Evaluation
       │
       ▼
Prediction & Insights
```

---

## 📁 Repository Structure

```text
Bitcoin-Price-Prediction/
│
├── BITCOIN.ipynb
├── bitcoin.csv
├── README.md
│
├── images/
│   ├── price_trend.png
│   ├── correlation_heatmap.png
│   ├── distribution_plots.png
│   └── confusion_matrix.png
```

---

## 🚀 How to Run

1. Clone the repository

```bash
git clone https://github.com/your-username/Bitcoin-Price-Prediction.git
```

2. Open the notebook in Google Colab or Jupyter Notebook

3. Install dependencies

```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost
```

4. Run all notebook cells sequentially

5. Review model performance and visualizations

---

## 💡 Future Improvements

* Incorporate technical indicators such as RSI, MACD, and Bollinger Bands.
* Use LSTM and Deep Learning models for time-series forecasting.
* Integrate real-time cryptocurrency data APIs.
* Perform hyperparameter tuning for improved accuracy.
* Build a deployment-ready prediction dashboard.

---

## 👨‍💻 Skills Demonstrated

* Data Analysis
* Exploratory Data Analysis (EDA)
* Feature Engineering
* Machine Learning Classification
* Model Evaluation
* Data Visualization
* Financial Data Analytics
* Python for Data Science

---

## 📬 Conclusion

This project demonstrates the practical application of machine learning techniques in financial market prediction. By leveraging historical Bitcoin trading data, feature engineering, and multiple classification algorithms, the project provides insights into short-term market direction and showcases a complete machine learning workflow from data preprocessing to model evaluation.
