<div align="center">

# 🏠 House Price Prediction using Machine Learning

### Predicting Residential House Prices using Regression Models
---

![Python](https://img.shields.io/badge/Python-3.10+-blue?style=for-the-badge\&logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-orange?style=for-the-badge\&logo=pandas)
![NumPy](https://img.shields.io/badge/NumPy-Numerical%20Computing-blue?style=for-the-badge\&logo=numpy)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Machine%20Learning-red?style=for-the-badge\&logo=scikitlearn)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-green?style=for-the-badge)
![Seaborn](https://img.shields.io/badge/Seaborn-EDA-purple?style=for-the-badge)

</div>



---

# 📖 Project Overview

Real estate pricing is often influenced by multiple factors such as property size, number of rooms, amenities, location, and market demand.

This project develops a complete **Machine Learning Regression Pipeline** capable of predicting residential house prices based on property attributes.

The project demonstrates the end-to-end Machine Learning lifecycle, including:

✅ Data Collection

✅ Data Cleaning

✅ Exploratory Data Analysis

✅ Feature Engineering

✅ Model Development

✅ Model Evaluation

✅ Visualization

✅ Business Insight Generation

The final outcome is a predictive model that can estimate house prices and identify the most influential factors affecting property value.

---

# 🎯 Internship Assignment

### Project Title

**House Price Prediction**

### Objective

Build a Machine Learning Regression Model capable of predicting house prices using real-world housing data and identify the features that most strongly influence property valuation.

### Internship Requirements

The following tasks were assigned as part of the internship project:

### Task 1 — Data Loading & Exploration

* Load dataset using Pandas
* Display first 10 records
* Analyze dataset dimensions
* Identify target and feature variables
* Check missing values

### Task 2 — Data Cleaning

* Handle missing values
* Remove duplicate records
* Perform categorical encoding
* Select meaningful features

### Task 3 — Model Building

* Train Linear Regression model
* Train Random Forest Regressor
* Compare model performance
* Evaluate using MAE, RMSE, and R² Score

### Task 4 — Visualization

* Price Distribution Histogram
* Correlation Heatmap
* Actual vs Predicted Scatter Plot
* Feature Importance Analysis (Bonus)

### Task 5 — Insights & Summary

* Feature Importance Analysis
* Model Performance Interpretation
* Business Recommendations
* Final Project Summary

---

# 📂 Dataset Information

### Dataset Source

Kaggle Housing Prices Dataset

### Dataset Statistics

| Attribute         | Value      |
| ----------------- | ---------- |
| Total Records     | 545        |
| Total Features    | 13         |
| Missing Values    | 0          |
| Duplicate Records | Removed    |
| Target Variable   | Price      |
| Problem Type      | Regression |

---

## Dataset Features

| Feature          | Description                   |
| ---------------- | ----------------------------- |
| price            | House Price                   |
| area             | Property Area                 |
| bedrooms         | Number of Bedrooms            |
| bathrooms        | Number of Bathrooms           |
| stories          | Number of Floors              |
| mainroad         | Main Road Access              |
| guestroom        | Guest Room Availability       |
| basement         | Basement Availability         |
| hotwaterheating  | Hot Water Facility            |
| airconditioning  | Air Conditioning Availability |
| parking          | Parking Spaces                |
| prefarea         | Preferred Area                |
| furnishingstatus | Furnishing Level              |

---

# ⚙️ Project Workflow

```text
Housing Dataset
        │
        ▼
Data Loading
        │
        ▼
Exploratory Data Analysis
        │
        ▼
Data Cleaning
        │
        ▼
Duplicate Removal
        │
        ▼
One-Hot Encoding
        │
        ▼
Feature Selection
        │
        ▼
Train-Test Split (80/20)
        │
        ▼
Linear Regression
        │
        ▼
Random Forest Regressor
        │
        ▼
Performance Evaluation
        │
        ▼
Data Visualization
        │
        ▼
Feature Importance Analysis
        │
        ▼
Business Insights
```

---

# 🔍 Exploratory Data Analysis

EDA was performed to understand the structure and quality of the dataset before model development.

### Analysis Performed

✅ Displayed first 10 records

✅ Checked dataset dimensions

✅ Examined data types

✅ Generated descriptive statistics

✅ Identified target variable

✅ Checked missing values

✅ Analyzed duplicate records

### Key Findings

* Dataset is well-structured.
* No missing values were detected.
* Dataset contains both numerical and categorical features.
* House prices exhibit a right-skewed distribution.
* Larger houses generally tend to have higher prices.

---

# 🧹 Data Preprocessing

Before model training, several preprocessing steps were performed.

---

## 1️⃣ Duplicate Removal

Duplicate records were removed to prevent bias and improve model reliability.

---

## 2️⃣ Categorical Encoding

Categorical variables were converted into machine-readable numerical format using:

```python
pd.get_dummies(drop_first=True)
```

Encoded Columns:

* mainroad
* guestroom
* basement
* hotwaterheating
* airconditioning
* prefarea
* furnishingstatus

---

## 3️⃣ Feature Selection

### Target Variable

```python
price
```

### Input Features

All remaining property attributes were used as predictors.

---

# 🤖 Machine Learning Models

Two supervised regression algorithms were implemented and compared.

---

## Model 1 — Linear Regression

Linear Regression was selected as the baseline model.

### Advantages

* Fast training
* Easy interpretation
* Strong performance on structured datasets
* Low computational complexity

---

## Model 2 — Random Forest Regressor

Random Forest Regressor was used to capture complex nonlinear relationships.

### Configuration

```python
RandomForestRegressor(
    n_estimators=100,
    random_state=42
)
```

### Advantages

* Handles nonlinear relationships
* Robust to overfitting
* Provides feature importance scores

---

# 📊 Model Performance Dashboard

| Metric   | Linear Regression | Random Forest |
| -------- | ----------------- | ------------- |
| MAE      | ₹970,043          | ₹1,021,546    |
| RMSE     | ₹1,324,507        | ₹1,400,566    |
| R² Score | 0.6529            | 0.6119        |
| Rank     | 🥇 1st            | 🥈 2nd        |

---

## 🏆 Best Performing Model

### Linear Regression

Linear Regression achieved:

* Lowest MAE
* Lowest RMSE
* Highest R² Score

### Why did it perform better?

The dataset contains only 545 records.

Linear relationships dominate the dataset, allowing Linear Regression to generalize better than Random Forest.

The model successfully explains approximately **65.3% of the variation in house prices**.

---

# 📈 Visualizations

The project includes multiple visualizations to better understand the dataset and model performance.

---

## 📊 Price Distribution Analysis

Purpose:

* Analyze house price distribution.
* Detect skewness and outliers.

Key Observation:

Most properties fall between ₹3M and ₹6M, with a smaller number of premium properties above ₹10M.

---

## 🔥 Correlation Heatmap

Purpose:

* Identify relationships between variables.

Strongest Positive Correlations:

* Area
* Bathrooms
* Stories

---

## 🎯 Actual vs Predicted Analysis

Purpose:

* Evaluate prediction quality.

Observation:

Most predictions align closely with actual values, indicating good model performance.

---

## ⭐ Feature Importance Analysis

Purpose:

* Identify the strongest drivers of house prices.

Generated using Random Forest Feature Importance.

---

# 🔥 Feature Importance Analysis

### Top Features Influencing House Prices

| Rank | Feature           |
| ---- | ----------------- |
| 🥇 1 | Area              |
| 🥈 2 | Bathrooms         |
| 🥉 3 | Air Conditioning  |
| 4    | Parking           |
| 5    | Stories           |
| 6    | Bedrooms          |
| 7    | Preferred Area    |
| 8    | Furnishing Status |

---

# 💡 Business Insights

## 📍 Area is the Dominant Price Driver

Property area contributes the highest predictive power and remains the strongest indicator of house value.

---

## 🚿 Bathrooms Matter More Than Bedrooms

Bathrooms rank significantly higher than bedrooms in feature importance, indicating buyers prioritize functionality and convenience.

---

## ❄️ Amenities Increase Property Value

Features such as:

* Air Conditioning
* Parking Availability
* Preferred Area

have a measurable positive impact on selling price.

---

## 🏘️ Location Premium Exists

Properties located near main roads and preferred residential areas consistently achieve higher market valuations.

---

# ✅ Internship Task Completion Matrix

| Task   | Requirement              | Status      |
| ------ | ------------------------ | ----------- |
| Task 1 | Dataset Loading          | ✅ Completed |
| Task 1 | Display First 10 Rows    | ✅ Completed |
| Task 1 | Dataset Exploration      | ✅ Completed |
| Task 1 | Missing Value Analysis   | ✅ Completed |
| Task 2 | Data Cleaning            | ✅ Completed |
| Task 2 | Duplicate Removal        | ✅ Completed |
| Task 2 | One-Hot Encoding         | ✅ Completed |
| Task 3 | Linear Regression        | ✅ Completed |
| Task 3 | Random Forest Regressor  | ✅ Completed |
| Task 3 | MAE Evaluation           | ✅ Completed |
| Task 3 | RMSE Evaluation          | ✅ Completed |
| Task 3 | R² Score Evaluation      | ✅ Completed |
| Task 4 | Price Distribution Plot  | ✅ Completed |
| Task 4 | Correlation Heatmap      | ✅ Completed |
| Task 4 | Actual vs Predicted Plot | ✅ Completed |
| Task 4 | Feature Importance Plot  | ✅ Bonus     |
| Task 5 | Insights & Summary       | ✅ Completed |

---

# 📦 Project Deliverables

```bash
HousePricePrediction_VemulapalliVamseeKrishna/
│
├── analysis.ipynb
├── Housing.csv
├── summary.pdf
│
├── charts/
│   ├── price_distribution.png
│   ├── correlation_heatmap.png
│   ├── actual_vs_predicted.png
│   └── feature_importance.png
│
└── README.md
```

---

# 🛠️ Technology Stack

| Technology       | Purpose                   |
| ---------------- | ------------------------- |
| Python           | Core Programming          |
| Pandas           | Data Processing           |
| NumPy            | Numerical Computing       |
| Scikit-Learn     | Machine Learning          |
| Matplotlib       | Visualization             |
| Seaborn          | Statistical Visualization |
| Jupyter Notebook | Development Environment   |

---

# 🧠 Learning Outcomes

Through this project, practical experience was gained in:

* Data Cleaning
* Exploratory Data Analysis (EDA)
* Feature Engineering
* One-Hot Encoding
* Regression Algorithms
* Model Evaluation
* Data Visualization
* Feature Importance Analysis
* Business Insight Generation
* End-to-End Machine Learning Workflow

---

# 🚀 Future Improvements

Potential enhancements include:

* XGBoost Regressor
* LightGBM
* CatBoost
* Hyperparameter Tuning
* Feature Scaling Experiments
* Log Transformation of Target Variable
* Advanced Feature Engineering
* Model Deployment using Flask/FastAPI
* Interactive Dashboard Development

---

# 🏁 Final Conclusion

This project successfully fulfilled all internship requirements by developing a complete Machine Learning pipeline for residential house price prediction.

The workflow covered:

✔ Data Collection

✔ Data Exploration

✔ Data Cleaning

✔ Feature Engineering

✔ Regression Modeling

✔ Performance Evaluation

✔ Data Visualization

✔ Business Insight Generation

After comparing multiple algorithms, **Linear Regression emerged as the best-performing model with an R² Score of 0.6529**, explaining approximately **65% of the variation in house prices**.

The analysis revealed that **Area, Bathrooms, Air Conditioning, Parking Availability, and Location Factors** are the strongest drivers of residential property prices.

This project demonstrates the practical application of Machine Learning in solving real-world real estate pricing challenges and serves as a strong baseline solution for future predictive analytics projects.

---

<div align="center">

## 👨‍💻 Author

### Vemulapalli Vamsee Krishna

Machine Learning • Data Analytics • Software Development

⭐ If you found this project useful, consider giving it a star!

</div>
