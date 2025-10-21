
Machine Learning Internship Project at Future Interns
# Walmart Sales Forecast project

## 📑 Table of Contents
1. [Problem Statement](#problem-statement)  
2. [Project Objective](#project-objective)  
3. [Data Description](#data-description)  
4. [Data Pre-processing Steps](#data-pre-processing-steps)  
5. [Choosing the Algorithm](#choosing-the-algorithm)  
6. [Motivation for Choosing the Algorithm](#motivation-for-choosing-the-algorithm)  
7. [Model Evaluations and Techniques](#model-evaluations-and-techniques)  

## Problem Statement
Walmart is one of the largest retail chains globally. Accurate weekly sales forecasting is essential for inventory management, staffing, and marketing planning. The goal of this project is to predict future weekly sales for Walmart stores using historical data, identify trends and seasonality, and evaluate the performance of the forecasting model.

## Project Objective
- Explore and understand Walmart’s weekly sales data.  
- Handle missing values and outliers in the dataset.  
- Build a forecasting model to predict future weekly sales.  
- Evaluate the model using appropriate metrics (MAE, MSE, RMSE).  
- Visualize historical and predicted sales trends for actionable insights.  

## Data Description
The dataset contains weekly sales information for Walmart stores. The main features include:

| Feature          | Description |
|-----------------|-------------|
| `Store`         | Unique store number |
| `Date`          | Week of the sales record |
| `Weekly_Sales`  | Total sales for the week |
| `Holiday_Flag`  | Indicates if the week contains a holiday (1 = holiday, 0 = non-holiday) |
| `Temperature`   | Average temperature during the week |
| `Fuel_Price`    | Fuel price for that week |
| `CPI`           | Consumer Price Index |
| `Unemployment`  | Unemployment rate |

The dataset provides historical sales trends for multiple stores and departments, which can be used to model patterns and forecast future sales.

## Data Pre-processing Steps
1. Handling Missing Values:Checked for null or missing entries and imputed or removed them as needed.  
2. Outlier Treatment: Used Interquartile Range (IQR) to detect and clip outliers in numeric columns.  
3. Date Formatting: Converted the `Date` column to datetime format and sorted the data chronologically.  
4. Aggregation: Grouped data by `Date` and `Store` as required for time series analysis.  
5. Transformation: Applied log transformations where necessary to stabilize variance for ARIMA modeling.  

## Choosing the Algorithm
For this project, I chose the ARIMA (AutoRegressive Integrated Moving Average) model because:  
- It is suitable for univariate time series forecasting.  
- Can capture trend and seasonality in sales data.  
- Well-established and widely used for retail sales predictions.  


## Motivation for Choosing the Algorithm
- Simplicity: ARIMA is interpretable and works well on historical sales data without requiring many external features.  
- Effectiveness:Provides accurate short-term forecasts for weekly sales trends.  
- Availability:Supported by Python libraries like `statsmodels`, making it easy to implement and evaluate.  

## Model Evaluations and Techniques
- Metrics Used:
  - MAE (Mean Absolute Error):Measures average absolute difference between predicted and actual sales.  
  - MSE (Mean Squared Error):Penalizes larger errors by squaring the differences.  
  - RMSE (Root Mean Squared Error): Square root of MSE, gives error in original units.  

  
 ##Visualization
  - Line plots to compare actual vs predicted weekly sales.  
  - Bar plots for top-performing stores.
<img width="1166" height="549" alt="download" src="https://github.com/user-attachments/assets/aa8e767f-3260-4849-a348-424d386747df" />
<img width="1389" height="590" alt="download" src="https://github.com/user-attachments/assets/1c5b84ce-41e4-491c-ab29-f18dab8318ca" />


  #Process
  1. Split data into training and testing sets based on time.  
  2. Fit the ARIMA model on training data.  
  3. Generate predictions for the test period.  
  4. Calculate evaluation metrics to measure performance.  
  5. Visualize predictions against actual sales trends to assess model accuracy.  

