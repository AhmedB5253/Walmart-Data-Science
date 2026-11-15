# Walmart Data Science Capstone Project

A Data Science capstone project focused on analyzing Walmart's historical weekly sales data, discovering business insights, and forecasting sales for 45 stores over the next 12 weeks.

## Project Overview

This project explores Walmart's weekly sales performance using Python and statistical analysis techniques. It includes data cleaning, exploratory data analysis (EDA), outlier detection, business problem-solving, and time-series forecasting.

The objective is to understand sales patterns, identify factors associated with sales performance, compare store performance, and generate future sales predictions.

## Business Objectives

- Analyze historical weekly sales across 45 Walmart stores.
- Investigate the relationship between sales and economic factors.
- Identify seasonal sales patterns and holiday effects.
- Detect and examine sales outliers.
- Identify the best- and worst-performing stores.
- Forecast weekly sales for each store for the next 12 weeks.

## Dataset Description

The dataset contains 6,435 records and 8 columns, covering weekly sales information for 45 stores.

| Column | Description |
|---|---|
| Store | Store identification number |
| Date | Week ending date |
| Weekly_Sales | Weekly sales amount |
| Holiday_Flag | Indicates a holiday week |
| Temperature | Temperature |
| Fuel_Price | Fuel price |
| CPI | Consumer Price Index |
| Unemployment | Unemployment rate |

## Tools & Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Statsmodels
- Scikit-learn
- Jupyter Notebook

## Project Workflow

1. Data Loading and Inspection
2. Data Cleaning and Preprocessing
3. Statistical Analysis
4. Exploratory Data Analysis (EDA)
5. Outlier Detection using the IQR Method
6. Business Questions and Insights
7. Time-Series Forecasting
8. Model Evaluation
9. Future Sales Forecast Generation

## Key Findings

- **Top-performing store:** Store 20, with average weekly sales of approximately $2.11 million.
- **Lowest-performing store:** Store 33, with average weekly sales of approximately $259,861.69.
- **Seasonality:** November and December recorded the strongest average sales, with December at approximately $1.28 million.
- **Holiday effect:** Average sales during holiday weeks were approximately 7.84% higher than non-holiday weeks.
- **Outliers:** 34 upper-end sales outliers were identified using the global IQR method.
- **Unemployment:** Overall correlation with weekly sales was approximately -0.106.
- **Temperature:** Overall correlation with weekly sales was approximately -0.064.
- **CPI:** Overall correlation with weekly sales was approximately -0.073.

These correlations indicate associations, not proof of causation.

## Predictive Modeling

Multiple forecasting approaches were evaluated using chronological training, validation, and testing.

Models considered:

- Naive Forecast
- Moving Average
- Holt's Exponential Smoothing
- ARIMA

The best-performing candidate was selected separately for each store based on validation RMSE.

### Forecasting Results

| Metric | Result |
|---|---:|
| Number of stores | 45 |
| Forecast horizon | 12 weeks |
| Total predictions | 540 |
| Average Test MAE | 57,346.64 |
| Average Test RMSE | 69,421.69 |

The reported error metrics are macro-averages of store-level results.

### Selected Model Distribution

| Model | Stores |
|---|---:|
| ARIMA | 15 |
| Naive Forecast | 14 |
| Moving Average | 10 |
| Holt | 6 |

## Repository Structure

```text
Walmart-Data-Science-Capstone/
│
├── Walmart_Sales_Analysis.ipynb
├── Walmart DataSet.csv
├── Walmart_12_Week_Sales_Forecast.csv
├── Walmart_Capstone_Report.pdf
└── README.md
```

## How to Run the Project

1. Clone or download this repository.
2. Install the required Python libraries:

```bash
pip install pandas numpy matplotlib seaborn statsmodels scikit-learn jupyter
```

3. Open the Jupyter Notebook:

```bash
jupyter notebook
```

4. Open `Walmart_Sales_Analysis.ipynb`.
5. Run the notebook cells sequentially.

## Limitations

- The dataset covers a historical period from February 2010 to October 2012.
- Historical forecasts should not be interpreted as current Walmart sales predictions.
- External variables may influence sales but correlation alone cannot establish causation.
- Long-term seasonal patterns are difficult to estimate reliably from the limited historical period.

## Conclusion

This project demonstrates the application of Python-based Data Science techniques to a real-world retail sales analysis problem. Through statistical analysis, visualization, business insights, and forecasting, it provides a structured approach to understanding historical sales performance and estimating future demand.

## Author

**Ahmed Bhawrasa Wala**

Data Science | Python | Data Analytics | Machine Learning

---

*Developed as part of a Data Science Capstone Project.*
