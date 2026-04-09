# Stock Market Data Analysis — Python Project

## 📌 Project Overview
This project provides an end‑to‑end analysis of historical stock‑market data using Python. It demonstrates core analytical skills relevant to junior data roles, including data ingestion, cleaning, exploratory analysis, visualisation, and a simple supervised learning model. The project was originally developed as part of an academic assignment and has since been expanded and reframed for professional portfolio use.

---

## 📊 Executive Summary
This analysis explores how stock‑price data can be processed, validated, visualised, and modelled within a scalable Python workflow. The project makes use of over 1,000 original CSV files representing daily OHLCV data for individual stock tickers, from which a subset of five were selected for analysis.
The workflow demonstrates:

data ingestion from multiple files
data cleaning and quality validation
exploratory trend analysis
visualisation of price movements
a simple predictive model using scikit‑learn
interpretation of results and discussion of limitations

This mirrors real‑world analytical expectations where the ability to extract patterns, validate data integrity, and communicate insights is as important as any modelling output.

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
