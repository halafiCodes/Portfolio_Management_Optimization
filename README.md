# Week 9: Financial Time Series Analysis and Forecasting

## Overview
This project focuses on analyzing and forecasting financial time series data using both classical statistical models and deep learning approaches. The work is divided into two main tasks. **Task 1** involves data extraction, cleaning, and exploratory data analysis (EDA), while **Task 2** focuses on building, training, and evaluating forecasting models for Tesla’s stock price.

The assets analyzed in this project are:
- **TSLA** (Tesla stock)
- **SPY** (S&P 500 ETF)
- **BND** (Vanguard Total Bond Market ETF)

The dataset covers the period from **January 1, 2015 to January 15, 2026**.

---

## Task 1: Preprocess and Explore the Data

### Objective
The objective of Task 1 is to understand and prepare the financial data for modeling by performing data cleaning, statistical analysis, and exploratory data analysis.

### Key Steps
- Extracted historical financial data using the **YFinance** Python library
- Stored data in organized pandas DataFrames for TSLA, SPY, and BND
- Checked data types and computed basic descriptive statistics
- Identified and handled missing values using forward filling and interpolation
- Calculated daily percentage returns to analyze volatility
- Performed rolling mean and rolling standard deviation analysis
- Conducted outlier detection to identify extreme price movements
- Applied the **Augmented Dickey-Fuller (ADF) test** to assess stationarity
- Calculated basic risk metrics such as **Value at Risk (VaR)** and **Sharpe Ratio**

### Key Challenges and Solutions
- Financial time series data contained missing values due to non-trading days, which were handled using interpolation and forward filling.
- Stock prices were non-stationary, requiring differencing after confirming this using the ADF test.
- Tesla exhibited high volatility and outliers, which were analyzed using rolling statistics and return distributions.

### Deliverables
- Jupyter Notebook containing:
  - Data preprocessing code
  - Exploratory data analysis
  - Visualizations
  - Stationarity test results
- Summary of data quality issues and how they were resolved

---

## Task 2: Build Time Series Forecasting Models

### Objective
The objective of Task 2 is to develop and evaluate forecasting models to predict Tesla’s future stock prices and compare the performance of classical and deep learning approaches.

### Models Implemented
- **ARIMA / SARIMA**
- **Long Short-Term Memory (LSTM) neural network**

### Key Steps
- Split the dataset chronologically into training and testing sets  
  - Training: 2015–2024  
  - Testing: 2025–2026
- Used ACF and PACF plots and `auto_arima` to select ARIMA parameters
- Trained ARIMA/SARIMA models on the training data
- Prepared sequence data for LSTM using sliding windows
- Scaled data to improve LSTM performance
- Built and trained the LSTM model
- Generated forecasts for the test period
- Evaluated all models using:
  - MAE (Mean Absolute Error)
  - RMSE (Root Mean Squared Error)
  - MAPE (Mean Absolute Percentage Error)

### Key Challenges and Solutions
- Time series data could not be randomly shuffled, so a strict chronological split was applied.
- ARIMA modeling required differencing to ensure stationarity.
- LSTM required careful data scaling, sequence preparation, and regularization to avoid overfitting.
- Predictions from LSTM were inverse-transformed before evaluation.

### Deliverables
- Trained ARIMA/SARIMA model with documented parameters
- Trained LSTM model with documented architecture
- Model comparison table with evaluation metrics
- Discussion of model performance and selection rationale

---

## Tools and Technologies
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- YFinance
- Statsmodels
- pmdarima
- TensorFlow / Keras
- Scikit-learn

---

## Conclusion
This project establishes a strong foundation for financial time series forecasting by combining rigorous data preprocessing with both statistical and deep learning models. The results from Task 1 and Task 2 enable future tasks such as long-term forecasting, portfolio optimization, and strategy backtesting.

---
