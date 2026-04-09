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

```text
python-stock-analysis
│
├── README.md
├── Analysing Big Data Assn 2 Part B/
├── Presentation Mod 3 Asn 2 Part B.pptx
└── (notebooks, visualisations and model outputs within folder structure)
```

---


## 📄 **Data Source**

The dataset consists of **over 1,000 CSV files**, each containing daily OHLCV (Open, High, Low, Close, Volume) data for a single stock ticker.  
For the purposes of this analysis, **five tickers were randomly selected**, allowing the workflow to be demonstrated without processing the entire archive while still maintaining scalability.

---

## 🔧 **Tools & Libraries Used**

- **Python**  
- **pandas** — data wrangling, type conversion, merging, cleaning  
- **Matplotlib** — price‑trend visualisation  
- **scikit‑learn** — Linear Regression modelling  
- **Jupyter Notebook** — iterative analysis and narrative structure

---

## 🧹 **Data Cleaning & Validation**

A series of quality‑assurance checks were applied to ensure the dataset was reliable:

- Conversion of date fields to `datetime`  
- Standardisation of column naming conventions  
- Removal of negative or impossible pricing values  
- Logical OHLC constraints, e.g.:  
  - High ≥ Low  
  - Open/Close within the High–Low range  
- Removal or correction of duplicated or corrupted rows  

These steps ensure that the dataset reflects realistic market behaviour before analysis or modelling is attempted.

---

## 📊 **Visual Explorations**

### **1️⃣ Closing Price Over Time**  
A line chart visualising long‑term price movement for a single selected ticker.  
This provides insight into trend direction, volatility, and potential breakouts.

### **2️⃣ Open vs Close — Scatter Plot**  
A scatter plot demonstrating the extremely strong linear relationship between Open and Close prices for the chosen stock.  
This explains why a simple linear model can achieve extremely high R² for same‑day prediction.

---

## 🤖 **Predictive Modelling**

A simple **Linear Regression model** was trained to predict same‑day *Close* price using *Open* price as the single feature.

**Model Performance:**  
- **R²:** ~0.998  
- **RMSE:** ~0.56  

These values reflect an extremely strong linear relationship — but also illustrate a key limitation:

⚠️ **The model includes data leakage by predicting same‑day prices using another same‑day value.**  
This is intentional for demonstration purposes and is clearly documented.

---

## 📈 **Insights & Interpretation**

- Open and Close prices show a **near‑perfect linear correlation**, which is expected due to the nature of intraday price movements.  
- Long‑term price trends differ significantly between the sampled tickers, reinforcing the importance of diversification.  
- Validation checks revealed inconsistent or illogical values in several files (e.g., negative prices), highlighting the need for robust preprocessing in financial datasets.  
- The linear model performs extremely well on same‑day prediction tasks, but **is not suitable for forecasting** — demonstrating the importance of understanding model context and limitations.  


---

## ▶️ **How to Run the Analysis**

1. Clone the repository  
2. Open the main notebook in Jupyter  
3. Ensure the CSV files are available in the appropriate directory  
4. Run each cell sequentially to reproduce cleaning, EDA, visualisations and modelling  
5. Modify the list of tickers to scale the analysis to more files in the dataset  

---

## ✅ **Conclusion**

This project demonstrates a complete, beginner‑friendly but scalable workflow for analysing stock‑market data in Python. It showcases:

- strong data‑cleaning discipline  
- a clear EDA narrative  
- professional‑quality visualisations  
- a transparent modelling example  
- analytical interpretation with documented limitations  

Together, these elements highlight the technical, analytical, and communication skills expected from a junior analyst or early‑career data professional.  
