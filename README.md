Demand Forecasting Model

This project aims to build a Demand Forecasting Machine Learning Model based on Blinkit sales data.  
It predicts future product demand by analyzing patterns from historical sales records.

Project Workflow

1. Data Loading
- Loaded data from an Excel file using pandas.
- Ensured proper handling of dates.

2. Data Preparation
- Converted the date column into datetime format.
- Sorted the dataset chronologically.
- Aggregated daily sales totals.

3. Feature Engineering
- Created useful features like:
  - Lag Features - Sales from 1, 7, and 14 days ago.
  - Rolling Averages - 7 day and 14 day moving averages of sales.
  - Date-based Features — (like month, week of year, day of week) to capture seasonal effects (optional extension).

4. Model Selection
- Chose XGBoost Regressor because it works well for structured/tabular data, and handles non-linear relationships very efficiently.

5. Hyperparameter Tuning
- Applied RandomizedSearchCV to find the best parameters.
- Tuned parameters like:
  - Number of trees (`n_estimators`)
  - Maximum depth of each tree (`max_depth`)
  - Learning rate (`learning_rate`)
  - Subsampling and column sampling rates

6. Model Evaluation
- Evaluated model using:
  - **Mean Absolute Error (MAE):** 214.80
  - **Root Mean Squared Error (RMSE):** 287.19
  - **R2 Score:** 0.36
  
  > An R² score of 0.36 means the model explains 36% of the variance in the sales data.  
  > Although not perfect, it is a reasonable first model and can be improved further.

### 7. **Visualization**
- **Actual vs Predicted Sales Plot** to compare real and forecasted values.
- **Feature Importance Plot** to understand which features impact the model most.

---

## 📈 Results Summary

- **R2 Score:** 0.36
- **Observations:**
  - The model is learning basic sales patterns.
  - There's scope for improvement by adding more features like holidays, weather, promotions, etc.
  - Model tuning and advanced time series techniques could further boost performance.

---

## 🖥 Tech Stack Used

- Python 3.8+
- Jupyter Notebook
- Libraries:
  - `pandas`
  - `numpy`
  - `matplotlib`
  - `seaborn`
  - `scikit-learn`
  - `xgboost`
  - `scipy`

---

## 🚀 How to Run

1. Clone or download this repository.
2. Install the required libraries:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn xgboost scipy
   ```
3. Open the Jupyter Notebook (`BECO Model.ipynb`).
4. Run all the cells step-by-step.

---

## 🔥 Future Scope

- Add more date-related and external features (holidays, promotions, weather).
- Try Time Series specific models (like Prophet, ARIMA).
- Improve hyperparameter tuning (Grid Search or Bayesian Optimization).
- Use TimeSeriesSplit for better validation.

---

## 🙏 Acknowledgment

This project was created as part of a **Demand Forecasting Assignment** to demonstrate a beginner-friendly, practical approach to applying machine learning in a business context.

---

# ✨ End of README
