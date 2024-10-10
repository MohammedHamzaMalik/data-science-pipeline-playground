## Time Series Modelling

### 🎯 **Goal**

The primary goal of this project is to perform a comprehensive time series analysis on the daily retail sales data of the United States. The purpose is to identify underlying patterns, trends, and seasonal effects within the sales data, which can help stakeholders make informed business decisions. By forecasting future sales, businesses can better manage inventory, optimize supply chains, and improve financial planning.

### 🧵 **Dataset**

The dataset used in this analysis is `real_sales_per_day.csv`, which contains monthly aggregated data of US retail sales in million dollars (adjusted for inflation to 2017 dollars). This dataset can be obtained from the [U.S. Census Bureau](https://www.census.gov/retail/index.html) or any relevant financial datasets repository. The dataset includes the following columns:

- **Date**: The date of the sales record.
- **Sales**: The retail sales figures in million dollars.

### 🧾 **Description**

- Visualizing the time series data to observe trends and seasonal patterns.
- Conducting stationarity tests to determine the need for differencing.
- Applying differencing techniques to stabilize the mean of the time series.
- Utilizing seasonal decomposition to extract seasonal components.
- Implementing forecasting models such as Exponential Smoothing and ARIMA to predict future sales.

### 🧮 **What I had done!**

1. **Data Loading**: The dataset is loaded into a pandas DataFrame from the CSV file.
2. **Initial Time Series Plot**: A time plot of the original sales data is created to visualize trends over the entire period.
3. **Stationarity Tests**: 
   - **ADF Test (Augmented Dickey-Fuller Test)**: This test checks if the time series is stationary or has a unit root.
   - **KPSS Test (Kwiatkowski-Phillips-Schmidt-Shin Test)**: This test checks for stationarity around a deterministic trend.
4. **Differencing**: If the series is found to be non-stationary, differencing is applied to stabilize the mean and remove trends.
5. **Differenced Series Plot**: The differenced time series is plotted to visualize the changes over time.
6. **Seasonal Decomposition**: The time series is decomposed into trend, seasonal, and residual components using an additive model.
7. **Forecasting Models**:
   - **Exponential Smoothing (ETS)**: An ETS model is fitted to capture the underlying trend and seasonality.
   - **ARIMA (Auto ARIMA)**: This model is fitted using the `auto_arima` function to automatically select the best parameters for the time series.
8. **Forecasting**: The ARIMA model is used to forecast sales for the next 36 months, and these forecasts are plotted alongside the original data for comparison.

### 🚀 **Models Implemented**

- **Exponential Smoothing (ETS)**: This model was chosen due to its effectiveness in handling seasonality and trends in time series data. It provides a flexible approach to modeling various patterns.
  
- **ARIMA (Auto ARIMA)**: This model was selected because it can automatically determine the best parameters for the time series, making it suitable for data that may not be stationary. It incorporates both autoregressive and moving average components.

### 📚 **Libraries Needed**

To successfully run this project, the following libraries are required:

- `pandas`: For data manipulation and analysis.
- `numpy`: For numerical operations.
- `matplotlib`: For creating visualizations.
- `statsmodels`: For statistical modeling and hypothesis testing.
- `pmdarima`: For implementing the ARIMA model and automated parameter selection.

You can install these libraries using the following command:

```bash
pip install pandas numpy matplotlib statsmodels pmdarima
