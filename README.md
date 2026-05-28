This repository uses multiple satellite-based and reanalysis datasets to reconstruct Terrestrial Water Storage (TWS) over Iran using deep learning models. The dataset includes GRACE/GRACE-FO TWS, soil moisture, precipitation, land surface temperature, and evapotranspiration. All datasets were obtained from the Google Earth Engine (GEE) platform and processed to a common monthly temporal resolution covering April 2002 to December 2022.

🌍 GRACE/GRACE-FO Terrestrial Water Storage

This dataset combines GRACE and GRACE-FO Level-3 terrestrial water storage (TWS) anomaly products provided by the Jet Propulsion Laboratory (JPL). It represents vertically integrated water storage variations at a spatial resolution of approximately 1° (~110 km).
Due to mission gaps and processing limitations, the dataset contains 35 missing months, which were handled during preprocessing. The TWS data are used as the target variable for all deep learning models.

🌱 Soil Moisture (SM)
Soil moisture data were obtained from the GLDAS-2.1 Noah land surface model. The dataset provides physically based, satellite-constrained estimates of land surface conditions. It was resampled from 3-hourly to monthly averages for consistency with GRACE data.

🌧️ Precipitation (PR)
Precipitation data were obtained from the CHIRPS dataset, a satellite–gauge blended product developed by USGS and UC Santa Barbara. The dataset provides daily precipitation at 0.05° resolution, aggregated here to monthly totals.

🌡️ Land Surface Temperature (LST)
LST data were obtained from the MODIS MOD11A2 Version 6.1 product. It provides 8-day composite land surface temperature at 1 km spatial resolution. The data were quality-controlled and aggregated to monthly values.

🌿 Evapotranspiration (ET)
Evapotranspiration data were obtained from the MODIS MOD16A2 product at 500 m spatial resolution. The product is based on the Penman–Monteith equation and combines meteorological forcing with vegetation parameters. Data were aggregated to monthly scale.

⚙️ Notes
All datasets were processed and aligned to a monthly time scale.
All input variables were used as predictors for deep learning models (LSTM, GRU, RNN).
GRACE/GRACE-FO TWS is used as the target variable.
Data preprocessing and normalization were applied before model training.
