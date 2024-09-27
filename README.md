# Weather-Trend-Forecasting

 ## Project Overview
This project focuses on cleaning, analyzing, visualizing, and forecasting global weather data using a dataset from the "GlobalWeatherRepository.csv". The code is divided into multiple sections including data preprocessing, exploratory data analysis (EDA), visualization, and time series forecasting using ARIMA models. The primary goal is to handle missing values, remove outliers, normalize the data, and apply machine learning models for weather forecasting.


## Table of Contents
- [Requirements](#requirements)
- [Data Preprocessing](#data-preprocessing)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Visualizations](#visualizations)
- [Time Series Forecasting with ARIMA](#time-series-forecasting-with-arima)
- [Model Saving](#model-saving)
- [Usage](#usage)
- [License](#license)

## Requirements
The following libraries are required to run the code:

```bash
pandas
numpy
scikit-learn
matplotlib
seaborn
statsmodels
joblib
## Data Preprocessing
The initial data preprocessing includes the following steps:

### Handling Missing Values:
- Missing values in numerical columns are filled using the median.
- Alternatively, rows with missing values can be dropped (optional).

### Outlier Removal:
- Outliers are handled using the Interquartile Range (IQR) method for key continuous variables such as temperature, precipitation, humidity, wind speed, and pressure.

### Normalization:
- The data is normalized using `MinMaxScaler` for improved model performance.

### Saving Cleaned Data:
- The cleaned dataset is saved as `Cleaned_GlobalWeatherRepository.csv`.

## Exploratory Data Analysis (EDA)
The EDA involves generating statistical summaries and understanding the relationships between weather variables. Key steps include:

### Summary Statistics:
- Provides descriptive statistics for numerical columns.

### Correlation Matrix:
- Displays correlations between weather variables such as temperature, precipitation, humidity, wind speed, and pressure.

## Visualizations

### Distribution Plots:
- Histogram and Kernel Density Estimation (KDE) plots for temperature and precipitation distributions.

### Correlation Heatmap:
- A heatmap is used to visualize the strength of correlations between weather variables.

### Line Plots for Trends:
- Time-series visualizations for temperature and precipitation over time.

### Pair Plot:
- A pair plot to visualize the distribution and correlations between weather variables.

### Box Plots:
- Used for detecting outliers in temperature and precipitation.

## Time Series Forecasting with ARIMA

### ARIMA Model:
- The code implements ARIMA (AutoRegressive Integrated Moving Average) models for temperature and precipitation forecasting.

### Evaluation:
- Forecasting models are evaluated using Mean Absolute Error (MAE) and Root Mean Square Error (RMSE).

### Visualization:
- Visual plots show actual vs. forecasted values for temperature and precipitation.

## Model Saving
The trained ARIMA models for temperature and precipitation forecasting are saved using `joblib` for future use:

- `arima_temp_forecast_model.pkl`
- `arima_precipitation_forecast_model.pkl`
