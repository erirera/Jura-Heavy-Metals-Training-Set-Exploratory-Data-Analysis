# Jura Heavy Metals — Prediction Set (n=259)

This repository contains the **prediction (training) subset** of the classic Swiss Jura geostatistical dataset. It is primarily used for Exploratory Data Analysis (EDA), spatial interpolation training, and environmental machine learning.

---

## 📂 Included Files

| File | Description |
|---|---|
| `jura_prediction_set.csv` | The raw tabular data containing the 259 training samples. |
| `jura_eda_dashboard.html` | An interactive HTML dashboard visualizing this specific prediction set. |
| `gen_dashboard.py` | The Python script used to generate the dashboard from the CSV. |

*(Note: The remaining 100 samples from the original 359-sample dataset are withheld as a validation set for model testing).*

---

## 📊 Dataset Overview (`jura_prediction_set.csv`)

The prediction set contains **259 geo-referenced samples**. 

### Contextual & Spatial Variables
- **S/N**: Unique sample ID
- **X (km), Y (km)**: Spatial coordinates in the Swiss Jura region
- **Rock type**: Underlying geology (1=Argovian, 2=Kimmeridgian, 3=Sequanian, 4=Portlandian, 5=Quaternary)
- **Land use**: Surface land cover (1=Forest, 2=Pasture, 3=Meadow, 4=Tillage)

### Target Variables (Heavy Metals)
Concentrations (in ppm) of 7 heavy metals measured at each location:
- **Cd**: Cadmium
- **Cu**: Copper
- **Pb**: Lead
- **Co**: Cobalt
- **Cr**: Chromium
- **Ni**: Nickel
- **Zn**: Zinc

---

## 🗺️ Interactive EDA Dashboard

To explore the data without writing code, open `jura_eda_dashboard.html` in any modern web browser (Chrome, Firefox, Edge, Safari). No local web server or installation is required—it runs entirely client-side.

The dashboard includes:
- **Summary Statistics**: Min, Max, Mean, Median, Q1/Q3, and Std Dev for all 7 metals.
- **Frequency Distributions**: Histograms showing the concentration spread of each metal.
- **Pearson Heatmap & Scatters**: Interactive tools to analyze the correlation between different heavy metals.
- **Spatial Map**: Sample locations color-coded by the concentration gradient of a selected metal.
- **Categorical Breakdown**: Mean metal concentrations grouped by Rock Type and Land Use.

---

## 🚀 Usage & AI Applications

This specific 259-sample subset is strictly intended for **training** and **exploratory analysis**. 

If you are developing AI agents or geospatial models, use this data to:
1. Understand the spatial autocorrelation of heavy metals.
2. Train multi-output regression models predicting metal concentrations from spatial coordinates and categorical features.
3. Develop baseline algorithms for environmental anomaly detection.
4. Benchmark autonomous AI Agents on their ability to perform automated EDA.
