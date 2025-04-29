# State-wise Water Quality Analysis and Forecasting in India

## 📌 Overview

This project analyzes and forecasts the water quality of India's river systems across various states from 2012 to 2024. Using real-world data from the Central Pollution Control Board, we study four key parameters—**Biochemical Oxygen Demand (BOD), Dissolved Oxygen (DO), pH, and Coliform bacteria levels**—to evaluate the state of water bodies and predict future trends using statistical and geospatial methods.

---

## 📚 Objectives

- Identify pollution hotspots across Indian rivers.
- Perform time-series forecasting of key water quality parameters.
- Visualize data using interactive maps and trend charts.
- Recommend policy-level interventions for water safety.

---

## 🗂️ Dataset Details

- **Source**: Central Pollution Control Board (NWMP Data)
- **Timeframe**: 2012–2024
- **Parameters**: 
  - pH  
  - BOD (mg/L)  
  - DO (mg/L)  
  - Conductivity (µS/cm)  
  - Coliform (MPN/100ml)
- **Additional Fields**: State, Station Code, River Name, Location, Latitude, Longitude

---

## 🧹 Data Preprocessing

- Missing values treated via interpolation/deletion based on severity.
- Converted columns to appropriate datatypes (`datetime`, `float`, etc.).
- Outliers removed based on domain knowledge (e.g., Coliform > 10,000 MPN/100ml).

---

## 🔍 Methodology

### 📈 Correlation Analysis
- Strong correlation between **BOD and Coliform**, **BOD and Conductivity**
- Inverse relationship observed between **BOD and DO**

### ⏳ Time Series Forecasting
- Model: **ARIMA (1,1,1)**
- Parameters Forecasted: BOD, DO, pH, Coliform
- Evaluation Metrics:
  - BOD – MAE: 38.76, RMSE: 41.74, MAPE: 16.76%
  - DO – MAPE: 2.20%
  - pH – MAPE: 1.27%
  - Coliform – MAPE: 7.98%

### 🗺️ Geospatial Mapping
- Interactive **Folium map** showing river station pollution levels based on BOD:
  - 🟢 Safe (<2 mg/L)
  - 🟡 Moderate (2–3 mg/L)
  - 🔴 Polluted (>3 mg/L)

---

## 📊 Results Summary

### 1. **Parameter Distributions**
- Most pH values: 6.8–8.3 (safe)
- BOD: 1.5–3.8 mg/L (moderate)
- DO: 5.0–7.8 mg/L (mostly healthy)
- Coliform: Often 500–2000 MPN/100ml, exceeding safe limits

### 2. **State-wise Trends**
- **Maharashtra, Kerala, Punjab** show stable pH trends
- **UP, Assam, Chhattisgarh** display fluctuating and poor-quality values

### 3. **Water Safety Classification**
- Safe (BOD < 3 & Coliform < 1000): **25.8%**
- Polluted (BOD > 3 & Coliform > 1000): **74.2%**

### 4. **Forecast Analysis**
- Predicts **improvement by 2030** in most regions
- **Yamuna and Ganges** remain severely polluted, requiring urgent attention

---

## ✅ Conclusions

- Indian water quality is improving overall but still poses serious concerns in the northern river basins.
- ARIMA-based forecasting is effective for early warning systems.
- The combination of **statistical, spatial, and visual analysis** provides actionable insights for policymakers.

---

## 🔮 Future Recommendations

- Deploy real-time monitoring sensors at pollution hotspots
- Launch clean-up programs near high-risk urban areas
- Use public dashboards for data transparency
- Apply satellite data (Sentinel-2, Landsat) for broader surveillance
- Upgrade forecasting models using **LSTM and RNN**

---

## 👨‍💻 Authors

- **Nikhil Deshmukh** – E22CSEU1099  
- **Utkarsh Maurya** – E22CSEU1107  
- **Ganesh Galbale** – E22CSEU1100  

Mentor: **Dr. Gitika Sharma**

---

## 📍 Institution

**School of Computer Science Engineering and Technology**  
**Bennett University**, Greater Noida, Uttar Pradesh

---

## 📁 Files

- `river_pollution_map.html` – Interactive Folium map
- `statewise_pH_trend.png` – Line plot of state-wise pH values
- `distribution_analysis.png` – KDE & histograms of parameters
- `forecast_model.py` – ARIMA model code

---

## 📎 License

This project is for academic and research purposes only.

