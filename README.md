# Jura Heavy Metals — AI-Assisted Geochemical Analysis

An end-to-end data science project using the classic **Swiss Jura dataset** for spatial geochemical exploration, exploratory data analysis, and machine learning-ready data preparation.

---

## 📂 Project Files

| File | Description |
|---|---|
| `jura_prediction_set.csv` | Training set — first 259 sample locations |
| `jura_validation_set.csv` | Validation/test set — remaining 100 sample locations |
| `jura_eda_dashboard.html` | Interactive EDA dashboard (open in any browser) |
| `gen_dashboard.py` | Python script that generates the dashboard from the CSV |

---

## 📊 Dataset Overview

The Swiss Jura dataset is a benchmark in spatial statistics and environmental geochemistry. It consists of **359 geo-referenced samples** collected across the Swiss Jura region.

### Variables

| Variable | Type | Description |
|---|---|---|
| `S/N` | Integer | Sample ID |
| `X (km)` | Float | Easting coordinate (km) |
| `Y (km)` | Float | Northing coordinate (km) |
| `Rock type` | Categorical | 1=Argovian, 2=Kimmeridgian, 3=Sequanian, 4=Portlandian, 5=Quaternary |
| `Land use` | Categorical | 1=Forest, 2=Pasture, 3=Meadow, 4=Tillage |
| `Cd (ppm)` | Float | Cadmium concentration |
| `Cu (ppm)` | Float | Copper concentration |
| `Pb (ppm)` | Float | Lead concentration |
| `Co (ppm)` | Float | Cobalt concentration |
| `Cr (ppm)` | Float | Chromium concentration |
| `Ni (ppm)` | Float | Nickel concentration |
| `Zn (ppm)` | Float | Zinc concentration |

### Train/Test Split

| Set | Rows | Purpose |
|---|---|---|
| Prediction set | 259 | Model training / EDA |
| Validation set | 100 | Model evaluation |

---

## 🗺️ Interactive EDA Dashboard

Open `jura_eda_dashboard.html` directly in any modern web browser. No server or installation required.

### Dashboard Sections

- **Summary Statistics** — KPI cards + full descriptive stats table for all 7 metals
- **Frequency Distributions** — Histograms for each metal concentration
- **Pearson Correlation Heatmap** — Bubble matrix of inter-metal correlations
- **Metal Pair Scatter Plot** — Interactive: select any two metals to compare
- **Spatial Distribution Map** — Sample locations color-coded by concentration gradient
- **By Rock Type & Land Use** — Doughnut counts + interactive mean-by-category bar charts

### Regenerating the Dashboard

```bash
# Requires Python 3.x (standard library only)
python gen_dashboard.py
```

---

## 🚀 Potential AI Research Directions

1. **Spatial Prediction** — Use ML (Random Forest, GNN, Kriging-hybrid) to predict metal concentrations at unsampled locations
2. **Multi-output Regression** — Predict all 7 metals simultaneously from coordinates + rock type + land use
3. **Anomaly Detection** — Identify pollution hotspots deviating from geological baseline
4. **Spatial Cross-Validation** — Block CV to avoid spatial leakage during model evaluation
5. **Feature Importance** — Determine which geological/land-use factors drive each metal's distribution

---

## 📋 Requirements

- Python 3.x (standard library only — `csv`, `json`, `math`, `os`, `string`)
- Any modern web browser (Chrome, Firefox, Edge) for the dashboard
- Internet connection (dashboard loads Chart.js from CDN)

---

## 📚 References

- Goovaerts, P. (1997). *Geostatistics for Natural Resources Evaluation*. Oxford University Press.
- Original data: Swiss Jura case study, widely used in geostatistical literature.
