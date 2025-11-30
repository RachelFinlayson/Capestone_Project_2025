<p align="center">
  <img src="https://via.placeholder.com/1200x300/0d1117/00ff88?text=Vegetable+Price+Forecasting+%7C+Time+Series+%2F+Machine+Learning+Capstone" alt="Vegetable Price Forecasting Banner">
</p>

# 📘 Vegetable Price Forecasting – Capstone Project
*A complete end-to-end time-series forecasting workflow using Python, Jupyter Notebook, and Power BI.*

---

## 🌱 Project Overview

This project analyses and forecasts **daily vegetable prices** using a full data science workflow. It includes:

- Data ingestion & cleaning  
- Exploratory data analysis (EDA)  
- Seasonal & trend analysis  
- Multiple forecasting models  
- Model evaluation & validation  
- Final model selection  
- Power BI dashboard for reporting  

Vegetable prices show different behaviours: some are **stable** (e.g., Tomato, Potato), while others are **volatile** (e.g., Garlic, Peas, Brinjal, Green Chilli).  
The final selected model is **Lagged Linear Regression**, which provided the best forecasting accuracy across most vegetables.

---

## 📊 Dataset

**Source:** Kaggle – *Vegetable Prices Dataset*  
**Link:** https://www.kaggle.com/datasets/ksamiksha19/vegetable-prices

**Variables include:**

- `date`  
- Bhindi  
- Tomato  
- Onion  
- Potato  
- Brinjal  
- Garlic  
- Peas  
- Methi  
- Green Chilli  
- Elephant Yam (Suran)

**Challenges addressed:**

- Missing values  
- Large outliers (especially Methi’s extremely high prices)  
- Inconsistent date intervals  
- Short time range (~1 year)

The dataset was cleaned, interpolated, and standardised before modelling.

---

## 🔍 Exploratory Data Analysis (EDA)

Key EDA findings:

- Several vegetables display **right-skewed** distributions.  
- Tomato and Elephant Yam have **very little variation**.  
- Garlic, Peas, and Brinjal show **high volatility** and large swings.  
- Quarterly seasonal decomposition reveals weak long-term seasonality due to the short dataset.  
- Strong **autocorrelation** indicates recent prices heavily influence next-day prices.

EDA visualisations include:

- Histograms  
- Boxplots  
- Correlation heatmap  
- Monthly average trends  
- Time-series plots  
- Rolling window statistics  

---

## 🤖 Modeling

Models evaluated:

- **Naïve baseline**
- **ARIMA(3,1,2)**
- **Lagged Linear Regression**
- **Random Forest Regressor**
- **XGBoost Regressor**

### Feature Engineering
- Lag variables: 1, 7, 14, 30 days  
- Rolling averages: 7-day & 30-day  
- Time-based train/test split (80/20)  

### Evaluation Metrics
- **MAE**
- **RMSE**

---

## 🏆 Final Model Selection

After comparing all models across each vegetable:

- **Lagged Linear Regression** achieved the **lowest RMSE for 9 out of 10 vegetables**  
- It also had the **best average RMSE across all vegetables**  
- Random Forest performed best only for *Elephant Yam (Suran)*  
- ARIMA performed best only for Tomato (due to its flat price behaviour)  
- XGBoost underperformed relative to LR and RF  

### ⭐ Selected Final Model: Lagged Linear Regression  
Chosen because it is:

- Accurate  
- Robust across vegetables  
- Interpretable  
- Computationally efficient  
- Well-suited for datasets with strong autocorrelation  

---
