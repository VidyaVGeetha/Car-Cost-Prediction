# 🚗 Used Car Price Prediction — UK Market  

**Author:** Vidya V.G.  
**Location:** Edinburgh, Scotland  
**Seeking:** Entry-level Data Analyst Role  

---

## 📄 Project Overview  
This project predicts used car prices in the UK using a **regression-based machine learning pipeline**.  
It was developed as part of my portfolio to showcase **data preprocessing, model selection, and evaluation** skills in Python.

**Key Goals:**  
- Analyze historical used car prices and identify key pricing factors  
- Compare multiple regression algorithms to select the best model  
- Produce journal-ready metrics, plots, and a deployable model  

---

## 📊 Dataset  
- **Source:** `Used Cars Prices in UK export 2025-08-09 05-54-05.csv`  
- **Rows:** 3,685  
- **Columns:** 14  
- **Target Variable:** `price` (£)  

**Example Features:**  
- **Numeric:** `mileage_miles`, `registration_year`, `previous_owners`, `engine_l`, `Doors`, `Seats`  
- **Categorical:** `fuel_type`, `body_type`, `Gearbox`, `emission_class`, `service_history`, `brand`  

---

## 🛠 Methodology  
- **Preprocessing:**  
  - Missing value imputation  
  - One-hot encoding of categorical variables  
  - Log transformation of target for skew reduction  
- **Model Selection:**  
  - LinearRegression  
  - Ridge / Lasso / ElasticNet  
  - RandomForestRegressor  
  - HistGradientBoostingRegressor  
  - SVR (RBF)  
- **Tuning:** 5-fold cross-validation with `RandomizedSearchCV`  
- **Evaluation Metrics:** RMSE, MAE, R²  

---

## 🏆 Results  

| Model                   | Val RMSE | Test RMSE | Test MAE | Test R²  |
|-------------------------|----------|-----------|----------|----------|
| **HistGradientBoosting**| 1,577.65 | **1,620.13** | 979.08   | 0.850    |
| RandomForest            | 1,676.59 | —         | —        | —        |
| ElasticNet              | 1,749.34 | —         | —        | —        |
| Lasso                   | 1,755.52 | —         | —        | —        |
| Ridge                   | 1,762.11 | —         | —        | —        |
| LinearRegression        | 2,009.12 | —         | —        | —        |
| SVR                     | 4,104.50 | —         | —        | —        |

---

## 📈 Figures Generated  
- 📊 Predicted vs Actual prices (Test set)  
- 📉 Residuals vs Fitted values  
- 📦 Residual distribution histogram  
- 📚 Learning curve (Train vs CV RMSE)  
- ⭐ Top-20 feature importances  

All plots are saved in the `figures/` directory.  

---

## 📂 Project Structure  

