# 🧠 Genetic Algorithm-Optimized Deep Learning Models for Reconstruction of Terrestrial Water Storage from GRACE/GRACE-FO

---

## 📌 Overview

This repository contains the datasets used in the study titled:

### ✨ “Genetic Algorithm-Optimized Deep Learning Models for Reconstruction of Terrestrial Water Storage from GRACE/GRACE-FO”

This study integrates multiple satellite-based and reanalysis datasets to reconstruct **Terrestrial Water Storage (TWS)** over Iran using deep learning models optimized with a **Genetic Algorithm (GA)**.

The dataset includes:

- 🌍 GRACE/GRACE-FO TWS  
- 🌱 Soil moisture  
- 🌧️ Precipitation  
- 🌡️ Land surface temperature  
- 🌿 Evapotranspiration  

All datasets were obtained from the **Google Earth Engine (GEE)** platform and processed to a common **monthly temporal resolution** covering **April 2002 to December 2022**.

---

## 📊 Dataset Description

### 🌍 GRACE/GRACE-FO Terrestrial Water Storage (Target Variable)

This dataset combines GRACE and GRACE-FO Level-3 TWS anomaly products provided by the **Jet Propulsion Laboratory (JPL)**. It represents vertically integrated terrestrial water storage variations at a spatial resolution of approximately **1° (~110 km)**.

Due to mission gaps and processing limitations, the dataset contains **35 missing months**, which were handled during preprocessing.

👉 This dataset is used as the **target variable** for all deep learning models.

---

### 🌱 Soil Moisture (SM)

Soil moisture data were obtained from the **GLDAS-2.1 Noah land surface model**, which provides physically based, satellite-constrained land surface estimates. The original 3-hourly data were aggregated to **monthly averages** to ensure consistency with GRACE observations.

---

### 🌧️ Precipitation (PR)

Precipitation data were obtained from the **CHIRPS dataset**, a satellite–gauge blended product developed by USGS and UC Santa Barbara. The dataset provides daily precipitation at **0.05° spatial resolution**, aggregated here to **monthly totals**.

---

### 🌡️ Land Surface Temperature (LST)

Land Surface Temperature (LST) data were obtained from the **MODIS MOD11A2 Version 6.1 product**, which provides 8-day composite LST at **1 km spatial resolution**. Quality-controlled observations were aggregated to **monthly values**.

---

### 🌿 Evapotranspiration (ET)

Evapotranspiration data were obtained from the **MODIS MOD16A2 product** at **500 m spatial resolution**. The product is based on the Penman–Monteith equation and integrates meteorological forcing with vegetation parameters. Data were aggregated to a **monthly scale**.

---

## ⚙️ Notes

- 📅 All datasets were aligned to a **monthly time scale**
- 🧠 Input variables were used for deep learning models (**LSTM, GRU, RNN**)
- 🎯 GRACE/GRACE-FO TWS is the **target variable**
- 🧹 All data were **preprocessed and normalized** before model training

---

## 📌 Folder Description

- 📁 `data/target/` → Contains GRACE/GRACE-FO TWS data (**target variable**)  
- 📁 `data/features/` → Contains all predictor variables used for model training  

---

## 📂 Repository Structure

```bash
data/
├── target/
│   └── GRACE_TWS.csv
│
├── features/
│   ├── soil_moisture.csv
│   ├── precipitation.csv
│   ├── land_surface_temperature.csv
│   └── evapotranspiration.csv
```

---

## 📚 Citation

If you use this dataset or code in your research, please cite the following work:

> *Genetic Algorithm-Optimized Deep Learning Models for Reconstruction of Terrestrial Water Storage from GRACE/GRACE-FO*  
> (Under review, Remote Sensing)

---

## 🚀 Summary

This repository provides a fully processed, multi-source dataset framework for:

- 🌍 Hydrological modeling  
- 🧠 Deep learning-based TWS reconstruction  
- ⚙️ Genetic algorithm–optimized forecasting models  
- 📊 Long-term climate and water storage analysis (2002–2022)
