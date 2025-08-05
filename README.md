# Indian Air Quality Analysis & Forecasting

## Project Overview

This project performs a comprehensive exploratory data analysis (EDA) and time-series forecasting on air quality data from various Indian cities spanning from 2015 to 2020. The primary objective is to uncover trends, identify pollution hotspots, analyze seasonal patterns, and build a predictive model to forecast the Air Quality Index (AQI) for Delhi.

The project culminates in an interactive Power BI dashboard designed to make these insights accessible and understandable for a general audience.

## Tech Stack

* **Language:** Python
* **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, Statsmodels
* **BI Tool:** Power BI
* **Environment:** Jupyter Notebook

## Dataset

The data used for this project is the "Air Quality Data in India (2015 - 2020)" dataset, publicly available on Kaggle.
* **Link:** [Kaggle Dataset](https://www.kaggle.com/datasets/rohanrao/air-quality-data-in-india)

## Project Workflow

1.  **Data Loading & Initial Exploration:** The dataset was loaded and its basic properties were examined.
2.  **Data Cleaning & Preprocessing:**
    * Converted the `Date` column to a datetime format.
    * Handled missing values using a time-series appropriate method (forward-fill on a per-city basis).
    * Ensured data consistency across all columns.
3.  **Exploratory Data Analysis (EDA):**
    * Performed city-wise, seasonal, and weekly pattern analysis.
4.  **Feature Engineering:**
    * Created categorical `AQI_Bucket` labels based on official CPCB guidelines.
    * Engineered time-based features (Month, Day of Week) and lag features for the forecasting model.
5.  **Time-Series Forecasting:**
    * Developed a Random Forest Regressor model to predict the next day's AQI in Delhi.
    * Validated the model using a chronological train-test split and evaluated its performance with MAE and RMSE metrics.
6.  **Dashboard Creation:** The cleaned data was used to build an interactive dashboard in Power BI.

## Key Questions & Insights

* **Which cities are the most polluted?**
    * Major metropolitan areas, particularly **Delhi and Ahmedabad**, consistently exhibit the highest average AQI levels.
* **What are the dominant pollutants?**
    * Particulate matter (**PM2.5**) is the most significant contributor to poor air quality, showing the strongest correlation with the overall AQI score.
* **Are there seasonal pollution patterns?**
    * Yes, air quality follows a distinct seasonal cycle. It worsens sharply in the winter months (October-January) and improves during the monsoon season (June-September).
* **Can we predict future AQI?**
    * The Random Forest model successfully forecasted the next day's AQI, with the most recent day's AQI (`AQI_lag_1`) being the most important predictive feature.

## Visualizations

### City-wise AQI Comparison (Bar Chart)
*This chart shows the average AQI for the top 15 most polluted cities.*

### Seasonal Pollution Trends in Delhi (Line Chart)
*This line chart illustrates the clear seasonal spikes in AQI, particularly during the winter.*

### AQI Category Analysis (Stacked Bar Chart)
*This chart shows the number of days Delhi spent in each AQI category ("Good", "Poor", "Severe", etc.) per year.*

### Time-Series Forecast vs. Actuals
*This plot shows the model's predictions against the actual AQI values for the test period (2020).*

### Power BI Dashboard
*The final interactive dashboard provides a comprehensive overview of the air quality situation, with filters for city and year.*

