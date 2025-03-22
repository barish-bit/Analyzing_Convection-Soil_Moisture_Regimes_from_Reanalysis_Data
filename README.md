# 🌧️ Identification of Convection–Soil Moisture Regimes from Reanalysis Data

This repository presents a 6th semester project on identifying and analyzing the relationship between **rainfall and soil moisture** across various Indian regions using **ERA-5** and **IMD** datasets. The project involves **visual analysis, regression modeling, and clustering** to understand the interactions between soil memory and precipitation patterns.

---

## 📌 Objective

- Analyze spatial and temporal distribution of rainfall and soil water volume across India.
- Explore potential correlations between rainfall and soil moisture.
- Identify regional patterns and regimes using statistical and machine learning methods.

---

## 🌐 Data Sources

- **IMD (India Meteorological Department)** – Rainfall data
- **ERA-5 Reanalysis Data** – Soil moisture, temperature, and rainfall data

> All data was provided in **NetCDF** format and processed using **Python**.

---

## 🧪 Methodology

### 🔸 Data Processing

- NetCDF files parsed to extract multi-year time series.
- Merged, subsetted, and processed for individual cities: Pune, Delhi, Kolkata, Bangalore, Mawsynram, and Mumbai.
- Daily rainfall and soil water volume extracted and averaged.
- Normalization and smoothing used for comparative plotting.

---

## 📊 Visual Analysis

### ✅ Spatial and Temporal Plotting
- Plotted **all-India rainfall** maps for daily intervals.
- Visualized **city-wise rainfall** patterns over 5 years.
- Plotted **ERA-5 soil moisture** and **temperature** for key cities.

### ✅ Power Spectrum and PDF
- Frequency domain analysis of rainfall to detect dominant patterns.
- Plotted **probability distribution functions (PDF)** of rainfall and temperature.

### ✅ Bar Plots
- Long-term trend (30 years) comparison of June–September rainfall over **Middle India** and **Rajasthan**.

---

## 🔍 Correlation & Regression Attempts

### 🔸 Linear Regression (Rainfall vs Soil Water Volume)
- Weak correlation observed initially.
- Data from ERA-5 with four soil layers averaged to form a single soil moisture series.
- R² values remained low, even after excluding outliers.

### 🔸 4-Day Averaging
- Attempted smoothing by averaging rainfall and soil moisture over 4-day periods.
- Minor improvements in visual alignment but no significant statistical gain.

### 🔸 Rainfall & Soil Water Volume Overlay
- Rainfall plotted as bar, soil moisture as a line → clear delayed response observed.
- Moisture rises with rainfall and decays after — mimics **RC circuit** behavior (memory effect).

---

## 📈 Daily Averaging and RC-like Behavior

- Averaged data across daily intervals for 3-month periods.
- Observed characteristic rise and fall pattern in soil moisture in response to rain events.
- Plots divided into subregions showed consistent memory effect across locations.

---

## 🔍 Clustering Analysis

### ✅ K-Means Clustering (k=6)
- Applied K-means to detect potential latent soil–rainfall regimes.
- Fitted **linear regression within each cluster**:
  - Slight improvement in some (e.g., Cluster 1 & 2)
  - Overall: no strong linearity observed in most clusters.

---

## 🔗 Project Code

📌 Google Colab:  
[Click here to view full code](https://colab.research.google.com/drive/1zebdxHm9g8pwd8USzbUmjPFclQz2jaP1?usp=share_link)

---

## ✅ Key Observations

- **Rainfall and soil moisture show weak global correlation** but strong **local temporal dynamics**.
- Memory effect of soil water can potentially be modeled using analogies like **RC circuits**.
- Daily average plots and K-means analysis highlight micro-regimes.
- Further modeling (e.g., physics-inspired or LSTM-based) could improve predictive accuracy.

---

## 👤 Author

**Barish Sarkhel**  
Reg. No: 20201242  
6th Semester Project – DS3613  
Indian Institute of Science Education and Research (IISER) Pune  
Supervisor: Dr. Joy Merwin Monteiro

---

## 📚 References

- ERA5 Reanalysis Data – [ECMWF/ERA5](https://www.ecmwf.int/en/forecasts/datasets/reanalysis-datasets/era5)
- IMD Rainfall Data – [India Meteorological Department](https://mausam.imd.gov.in/)
- RC Circuit Behavior – Physics Analogy in Hydrology
- K-Means Clustering – Scikit-learn Documentation

---

## 📎 License

This project is for academic and research purposes only. Please cite the author and supervisor for any derivative work.


