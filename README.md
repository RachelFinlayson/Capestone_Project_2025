# Capestone Project 2025
# Vegetable Prices Analysis

This project explores vegetable price patterns using Python.  
It is part of the ExploreAI 2501 Data Science module.

## 📊 Dataset

We used the **Vegetable Prices** from Kaggle:  
[https://www.kaggle.com/datasets/ksamiksha19/vegetable-prices]

Trello board: https://trello.com/invite/b/68a1be65fc3961c39dc55262/ATTI34a4e0d13276faef1d4bd3c3705e80fc98CDDE7D/my-trello-board

## 🔧 Tools Used

- Python  
- Jupyter Notebook  
- Pandas, NumPy, Seaborn, Matplotlib  
- GitHub for version control  

## 🧠 Objectives

- Understand vegetable pricing trends  
- Visualize data across regions and years  
- Practice data cleaning, manipulation, and EDA  
- Work using Git and GitHub  

## 🗂 Structure

- `notebook.ipynb`: Analysis notebook  
- `requirements.txt`: Package list  
- `README.md`: Project overview  

📘 Vegetable Price Forecasting – Capstone Project

A complete end-to-end time-series forecasting workflow using Python, Jupyter Notebook, and Power BI.

🌱 Project Overview

This project analyses and forecasts daily vegetable prices using a full data science workflow. It includes:

Data ingestion & cleaning

Exploratory data analysis (EDA)

Seasonal & trend analysis

Multiple forecasting models

Model evaluation & validation

Final model selection

Power BI dashboard for reporting

Vegetable prices show different behaviours: some are stable (e.g., Tomato, Potato), while others are volatile (e.g., Garlic, Peas, Brinjal, Green Chilli).
The final selected model is Lagged Linear Regression, which provided the best forecasting accuracy across most vegetables.

📊 Dataset

Source: Kaggle – Vegetable Prices Dataset
Link: https://www.kaggle.com/datasets/ksamiksha19/vegetable-prices

Variables include:

date

Bhindi

Tomato

Onion

Potato

Brinjal

Garlic

Peas

Methi

Green Chilli

Elephant Yam (Suran)

Challenges addressed:

Missing values

Large outliers (especially Methi’s extremely high prices)

Inconsistent date intervals

Short time range (~1 year)

The dataset was cleaned, interpolated, and standardised before modelling.

🔍 Exploratory Data Analysis (EDA)

Key EDA findings:

Several vegetables display right-skewed distributions.

Tomato and Elephant Yam have very little variation.

Garlic, Peas, and Brinjal show high volatility and large swings.

Quarterly seasonal decomposition reveals weak long-term seasonality due to the short dataset.

Strong autocorrelation indicates recent prices heavily influence next-day prices.

EDA visualisations include:

Histograms

Boxplots

Correlation heatmap

Monthly average trends

Time-series plots

Rolling window statistics

🤖 Modeling

Models evaluated:

Naïve baseline

ARIMA(3,1,2)

Lagged Linear Regression

Random Forest Regressor

XGBoost Regressor

Feature Engineering

Lag variables: 1, 7, 14, 30 days

Rolling averages: 7-day & 30-day

Time-based train/test split (80/20)

Evaluation Metrics

MAE

RMSE

🏆 Final Model Selection

After comparing all models across each vegetable:

Lagged Linear Regression achieved the lowest RMSE for 9 out of 10 vegetables

It also had the best average RMSE across all vegetables

Random Forest performed best only for Elephant Yam (Suran)

ARIMA performed best only for Tomato (due to its flat price behaviour)

XGBoost underperformed relative to LR and RF

⭐ Selected Final Model: Lagged Linear Regression

Chosen because it is:

Accurate

Robust across vegetables

Interpretable

Computationally efficient

Well-suited for datasets with strong autocorrelation

📈 Power BI Dashboard

The Power BI dashboard includes:

Page 1 – Overview

Historical price trends

Average RMSE per model

Best model per vegetable

Vegetable & date slicers

Page 2 – Final Model Performance

Actual vs predicted plots (test period)

Error distribution

Scatter plot (Actual vs Predicted)

MAE & RMSE KPIs

Page 3 – Exploratory Analysis

Histogram and boxplot visuals

Correlation heatmap

Summary stats per vegetable

This enables stakeholders to explore insights interactively.

🗂️ Repository Structure
.
├── data/
│   ├── prices_raw.csv
│   ├── prices_clean.csv
│   ├── final_predictions.csv
│   └── model_results.csv
│
├── notebooks/
│   ├── VegetableForecasting.ipynb
│   └── EDA_and_Preprocessing.ipynb
│
├── powerbi/
│   └── VegetableForecastingDashboard.pbix
│
├── models/
│   └── final_lagged_lr.joblib
│
├── README.md
└── requirements.txt

🧪 How to Run
1. Install dependencies
pip install -r requirements.txt

2. Launch the Jupyter Notebook
jupyter notebook

3. Open the Power BI dashboard

Open the file:
powerbi/VegetableForecastingDashboard.pbix

🔮 Future Work

Extend dataset to include more historical years

Add external variables (weather, fuel costs, holidays, supply volumes)

Compare performance with SARIMA, Prophet, LSTM, Transformer-based models

Build automated pipelines for continuous forecasting

Extend Power BI dashboard with what-if forecasting & automatic refresh
