# Task 2 — Build and Evaluate Forecasting Models

## Objective
Train and compare time-series models (ARIMA and LSTM) to forecast TSLA prices, then select the best-performing model.

## Notebook
- notebooks/task_2.ipynb

## Key Steps
- Train ARIMA with auto_arima
- Train LSTM on scaled series
- Evaluate models on a holdout test set
- Save the best model artifact

## Outputs
- Error metrics (MAE, RMSE, MAPE)
- Forecast comparison plot
- Saved model: models/arima_model_tsla.pkl

## How to Run
Open the notebook and run all cells from top to bottom.
