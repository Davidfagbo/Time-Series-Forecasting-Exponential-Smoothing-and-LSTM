# NVIDIA Stock Price Forecasting using Exponential Smoothing

## Overview
This project implements a **time series forecasting pipeline** to analyze and predict **NVIDIA (NVDA) daily stock prices** using **Holt-Winters Exponential Smoothing**. The workflow covers **data ingestion via API**, data preprocessing, **model training and evaluation**, and **short-term future forecasting**, with results visualized for clear insight delivery.

The project demonstrates practical time series analysis, model evaluation, and business-focused interpretation of predictive outputs.

---

## Objectives
- Collect historical daily stock price data using a public financial API  
- Clean, transform, and structure time series data for modeling  
- Train and evaluate a forecasting model using historical prices  
- Assess model performance using standard regression metrics  
- Generate and visualize short-term future price forecasts  

---

## Data Source
- **API Provider:** Twelve Data  
- **Asset:** NVIDIA Corporation (NVDA)  
- **Frequency:** Daily closing prices  
- **Time Range:** Last 3 years of historical data  

> Note: An API key from Twelve Data is required to run this project.

---

## Tools & Technologies
- **Python**
- **Pandas** – data manipulation and preprocessing  
- **Statsmodels** – Holt-Winters Exponential Smoothing  
- **Scikit-learn** – model evaluation metrics  
- **Matplotlib** – data visualization  
- **Requests** – API data ingestion  

---

## Methodology

### 1. Data Ingestion
- Pulled daily NVDA price data using the Twelve Data REST API  
- Retrieved ~4 years of historical data and filtered to the most recent 3 years  

### 2. Data Preprocessing
- Converted date fields to datetime format  
- Set datetime as the index for time series modeling  
- Converted price columns to numeric types  
- Sorted data chronologically  
- Exported the cleaned dataset to CSV for reproducibility  

### 3. Train-Test Split
- Split data into:
  - **80% training set**
  - **20% testing set**
- Forecast target: daily closing price  

### 4. Model Training
- Applied **Holt’s Exponential Smoothing** with an additive trend  
- Trained the model on historical closing prices  

### 5. Model Evaluation
Model performance was evaluated using:
- **MAPE (Mean Absolute Percentage Error)**
- **RMSE (Root Mean Squared Error)**  

A detailed **Actual vs Predicted** comparison was generated to assess forecast accuracy.

### 6. Future Forecasting
- Generated a **7-day forward price forecast**
- Created future timestamps dynamically
- Visualized recent historical prices alongside future predictions

---

## Visualizations
- Actual vs Predicted prices (test set)  
- Short-term future forecast with confidence shading  
- Clear time-based plots designed for interpretability and stakeholder communication  

---

## Key Outputs
- Cleaned and structured time series dataset  
- Forecast accuracy metrics (MAPE & RMSE)  
- Tabular comparison of actual vs predicted values  
- 7-day future price forecast with visual insights  

---

## Example Metrics
- **MAPE:** Reported as a percentage for interpretability  
- **RMSE:** Expressed in USD to reflect real-world price deviation  

