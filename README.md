# Stock Market Data Analysis — Python Project

## 📌 Project Overview
This project is an end‑to‑end Python analysis of historical stock‑market data.  
The goal is to demonstrate core data‑analysis skills expected for junior analyst roles, including:

- Data ingestion from multiple files  
- Data cleaning & validation  
- Exploratory data analysis (EDA)  
- Visualisation using Matplotlib  
- A simple predictive model using scikit‑learn  
- Interpreting insights & documenting limitations  

This project was originally built as part of an academic assignment, and has been expanded and reframed for professional portfolio use.

---

## 📂 Data Source
The dataset consists of over **1,000 CSV files**, each representing a single stock ticker with daily OHLCV data.  
For the purposes of this project, **five randomly selected tickers** were used, demonstrating how the methods apply to a large, scalable dataset.

---

## 🛠 Tools & Libraries Used
- **Python**
- **Pandas** (data wrangling & cleaning)
- **Matplotlib** (visualisation)
- **scikit‑learn** (linear regression model)
- **Jupyter Notebook**

---

## 🔧 Data Cleaning Steps
The following transformations were applied:

- Converted date columns to proper datetime format  
- Standardised column names  
- Removed negative or invalid price values  
- Ensured OHLC values followed logical constraints  
  - High ≥ Low  
  - Open/Close within the High–Low range  

These checks ensure real‑world data quality before analysis.

---

## 📊 Visualisations
### 1️⃣ Closing Price Over Time  
A line chart visualising long‑term price movement for a selected ticker.

### 2️⃣ Open vs Close Scatter Plot  
A scatter plot showing the strong linear relationship between open and close prices.

Both images are included in this repository.

---

## 🤖 Predictive Model
A simple **Linear Regression** model was trained to predict same‑day *Close* price from *Open* price.

**Model Results:**
- **R²:** ~0.998  
- **RMSE:** ~0.56  

⚠️ **Important Note:**  
This model is not intended for real forecasting — it demonstrates understanding of modelling workflow. Because the model predicts same‑day values, it includes *data leakage* and is intentionally basic.

---

## ⚠️ Limitations
- Dataset sample is small (5 tickers)  
- Model predicts same‑day Close → not suitable for forecasting  
- Random train/test split instead of time‑series split  
- Spark not available in the environment (not used)  

---

## 🚀 Future Improvements
- Predict next‑day Close instead of same‑day  
- Engineer lag features (returns, rolling averages)  
- Use a proper **time-series split**  
- Scale analysis to all 1,000+ tickers  
