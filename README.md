# 🏗️ Bulldozer Price Prediction

## 📦 End-to-End Machine Learning Project

This project predicts the **sale price of bulldozers** using historical data from the **Blue Book for Bulldozers** dataset. It follows a complete end-to-end machine learning pipeline: from data cleaning to model training, evaluation, and feature importance analysis.

📚 **Author**: Lyna Bouikni  
📅 **Project Type**: Portfolio – Tabular Data Regression  
🎯 **Goal**: Predict auction prices for used heavy equipment

---

## 🔍 Problem Statement

> Given characteristics of a bulldozer (year made, model, size, usage, etc.), predict its **future sale price** as accurately as possible.

---

## 🗂️ Dataset

- 📥 **Source**: [Kaggle Blue Book for Bulldozers](https://www.kaggle.com/competitions/bluebook-for-bulldozers)
- 📊 **Samples**: ~400,000 entries
- 📌 **Target**: `SalePrice` (in USD)

---

## 🛠️ ML Pipeline Steps

### 1. 📁 Data Loading & Cleaning
- Handled missing values and inconsistent datatypes
- Dropped columns with >50% missing values
- Converted dates and removed non-informative columns

### 2. 🏷️ Feature Engineering
- Extracted `saleYear`, `saleMonth`, and `machineAge`
- Transformed categorical variables with ordinal encoding
- Added domain-relevant variables (e.g., age at sale)

### 3. 🤖 Model Training
- Used **RandomForestRegressor** as baseline
- Evaluated using **RMSLE** (Root Mean Squared Log Error)

### 4. 📈 Evaluation & Tuning
- Compared validation scores across folds
- Interpreted model with **feature importances**

---

## 🧠 Key Features

| Feature | Description |
|---------|-------------|
| `YearMade` | Year the machine was manufactured |
| `ProductSize` | Size category of the equipment |
| `saleYear` | Year the bulldozer was sold |
| `fiBaseModel` | Base model code of the bulldozer |

These features showed the highest predictive power based on impurity-based importance from the Random Forest.

---

## 📊 Performance

| Metric | Score |
|--------|-------|
| Train RMSLE | ~0.19 |
| Validation RMSLE | ~0.25 |
| Test RMSLE | ~0.23 |

✅ No overfitting  
✅ Stable generalization performance  
✅ Fast model inference

---

## 📁 Project Structure
```bash
├── end_to_end_bulldozer_price_regression.ipynb # Main notebook
├── README.md
├── requirements.txt
└── data/ (not included due to Kaggle terms)
```
