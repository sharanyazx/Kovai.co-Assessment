# Transportation Ridership Forecasting - Kovai.co Assessment

## 📌 Project Overview

This project implements a **Vector Autoregression (VAR)** model to forecast daily ridership across multiple transportation service categories. Developed as part of the Kovai.co technical assessment, it demonstrates the application of multivariate time series forecasting on public transport data.


## ❓ Problem Statement

Forecast the **daily passenger journeys for the next 7 days** across five service types:

- **Local Route** (bus services)  
- **Light Rail**  
- **Peak Service** (rush hour trains/buses)  
- **Rapid Route** (express services)  
- **School** (educational transport services)  

Reliable forecasts help transit authorities optimize schedules, manage resources, and improve service quality.

---

## ⚙️ Solution Approach

### Algorithm: Vector Autoregression (VAR)

- Models multiple time series simultaneously to capture interdependencies  
- Accounts for relationships between ridership in different service categories  
- Provides joint forecasts, enabling holistic planning  
- Lag order selected using **Akaike Information Criterion (AIC)** or **Bayesian Information Criterion (BIC)** to balance model fit and complexity  

---

## 🔑 Key Features

### Robust Data Processing

- Supports multiple date formats and automatic parsing  
- Converts ridership columns to numeric, handling errors gracefully  
- Removes duplicates, missing values, and infinite values to ensure data integrity  
- Indexes data by date for time series analysis  

### Intelligent Model Selection

- Automatically selects optimal lag length based on information criteria  
- Implements fallbacks if automatic selection fails, ensuring model stability  
- Trains VAR model on cleaned data to capture temporal and cross-series dependencies  

### Comprehensive Forecasting

- Generates 7-day ahead ridership forecasts for all service types  
- Applies non-negativity constraints to avoid unrealistic negative passenger counts  
- Outputs daily ridership estimates and summary statistics for planning  

---

## 📊 Data Summary

- Dataset includes daily passenger counts for five service categories  
- Data cleaned and validated to ensure quality  
- Date index and numeric data types standardized for modeling  

---

## 🛠 Implementation Details

- Developed in **Python** using `pandas` for data handling, `numpy` for numerical operations, and `statsmodels` for VAR modeling  
- Uses robust date parsing and data cleaning techniques to handle real-world data inconsistencies  
- Includes comprehensive error handling for file I/O, parsing, and data sufficiency issues  

---

## 📈 Forecasting Results

- Produces ridership forecasts for each service type over a 7-day horizon  
- Provides both individual service forecasts and aggregated daily totals  
- Facilitates demand anticipation, enabling better resource allocation and scheduling  

---

## ⚠️ Error Handling & Validation

- Catches and reports file not found, empty file, and parsing errors clearly  
- Validates sufficient data is available after cleaning before modeling  
- Filters warnings to provide a cleaner runtime experience  

---

## 🚀 Conclusion

The implemented VAR forecasting model effectively captures the complex temporal dynamics and inter-service relationships inherent in public transport ridership data. This solution empowers transportation planners with actionable insights to improve operational efficiency and meet passenger demand proactively.

---


