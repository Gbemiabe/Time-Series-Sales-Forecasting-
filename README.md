# Sales Forecasting Project

   [![Project Status](https://img.shields.io/badge/Status-Completed-brightgreen)](https://img.shields.io/badge/Status-Completed-brightgreen)

   ## Executive Summary

   This project analyzed sales data to forecast future trends and identify factors influencing sales volatility. Time series models were developed and evaluated, providing insights into sales patterns and the challenges of accurate prediction in a dynamic business environment. The findings can inform inventory management, marketing strategies, and financial planning.

   ## Business Problem

   Accurate sales forecasting is crucial for businesses to optimize inventory, allocate resources effectively, and make informed strategic decisions. However, sales data can be complex and influenced by various factors, making accurate forecasting challenging.

   ## My Role

   As the data analyst, I was responsible for the entire analytical process, including data cleaning, exploratory data analysis, model selection, implementation, evaluation, and interpretation of results.

   ## Key Skills

   This project demonstrated my skills in:

   * Time series analysis
   * Data visualization
   * Statistical modeling (ARIMA, Prophet)
   * Data cleaning and preprocessing
   * Feature engineering (TotalSales calculation)
   * Communication of technical findings

   ## Data Description

   The dataset consists of sales transactions, including information on:

   * `Date`: Date of the transaction
   * `SKU`: Stock Keeping Unit (product ID)
   * `Price`: Price of the product
   * `Quantity`: Quantity sold
   * Other relevant columns (if any)

   ## Methodology

   The analysis followed these key steps:

   1.  **Data Loading and Cleaning:**
       * The data was loaded from a CSV file.
       * Irrelevant columns were removed.
       * The `Date` column was converted to datetime format.
       * `TotalSales` was calculated (`Price` \* `Quantity`).
       * Sales data was aggregated by date to create a daily sales time series.

   2.  **Exploratory Data Analysis (EDA):**

       * **Time Series Visualization:**
           ![Daily Total Sales](images/daily_total_sales.png)
           This plot reveals an overall trend with significant spikes and increased volatility, particularly in the later period.
       * **Stationarity Check:**
           The Augmented Dickey-Fuller (ADF) test indicated that the time series is stationary (p-value = 0.0027), which is important for ARIMA modeling.
       * **ACF and PACF Analysis:**
           ![ACF and PACF Plots](images/acf_pacf_plots.png)
           ACF and PACF plots were used to inform the initial selection of ARIMA parameters.

   3.  **Time Series Modeling:**

       * **ARIMA:**
           * An ARIMA(1, 0, 1) model was initially explored.
           * Model order selection was performed using AIC.
           * ![ARIMA Predictions](images/arima_predictions.png)
           * The ARIMA model's performance was evaluated using RMSE.
       * **Prophet:**
           * The Prophet model was implemented to handle trends and potential outliers.
           * ![Prophet Predictions](images/prophet_predictions.png)
           * The Prophet model's performance was also evaluated using RMSE.

   4.  **Results and Discussion:**

       * Both ARIMA and Prophet models struggled to capture the sales spikes, resulting in high RMSE values.
       * This suggests that external factors (e.g., promotions, marketing campaigns) likely influence sales and are not captured by the time series alone.
       * The models' limitations highlight the challenges of forecasting volatile sales data.

   ## Conclusion and Future Work

   This project demonstrated a systematic approach to time series analysis. Future work could explore:

   * Incorporating external data to improve forecast accuracy.
   * Advanced time series models for volatile data.
   * Outlier treatment techniques.

   ## Repository Contents

   * `README.md`: This file (project documentation).
   * `data/sales_data.csv`: The sales dataset.
   * `images/`: Folder containing visualizations.
   * `Sales_Forecasting_Notebook.ipynb`: Google Colab notebook with the analysis code.

   ## Contact

   Aduragbemi Abe| abeaduragbemi@gmail.com
