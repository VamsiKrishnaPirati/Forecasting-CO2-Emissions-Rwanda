# Rwanda CO₂ Emissions Forecasting

## 📌 Project Overview
This project focuses on **forecasting CO₂ emissions in Rwanda** using **time series analysis**. The dataset comprises **atmospheric data from Sentinel-5P** across 497 locations, clustered based on geographic proximity.

## 🏆 Objectives
- **Analyze CO₂ emission patterns** over time.
- **Handle outliers** (e.g., COVID-19 impact).
- **Use time series forecasting models** to predict future emissions.

## 📊 Dataset Insights
- **Source:** Kaggle
- **Data Span:** January 2019 - November 2022 (Weekly Data)
- **Features:**
  - **Sulfur Dioxide (SO₂)**
  - **Carbon Monoxide (CO)**
  - **Nitrogen Dioxide (NO₂)**
  - **Formaldehyde (HCHO)**
  - **UV Aerosol Index**
  - **Ozone (O₃)**
  - **Cloud Data**

## 🛠 Handling COVID-19 Outliers
1. **Splitting Data** into **pre-COVID** & **during-COVID** periods.
2. **Computing emission ratios** to normalize COVID-period data.
3. **Adjusting the dataset** to remove anomalies.

## 🚀 Methodology
### **Dimensionality Reduction**
- **Technique:** Singular Value Decomposition (SVD)
- **Goal:** Reduce 497 location features to **5 principal components**.

### **Modeling**
- **Auto-ARIMA & Prophet Models** used for each of the **5 principal components**.
- **Multivariate analysis** was discarded due to **high collinearity**.

### **Model Evaluation**
- **10-Fold Cross-Validation**
- **Residual Diagnostics** confirmed no additional predictive signals.
- **Metrics Used:** Mean Absolute Percentage Error (MAPE), Root Mean Squared Error (RMSE).

## 🔮 Forecasting
- **Prediction Horizon:** **Next 14 Days**.
- **Visualization:** 3D Scatter Plot & Time Series Graphs for clustered locations.

