# Jura Heavy Metals — Prediction Set EDA Dashboard

## Overview

This dashboard (`index.html`) delivers a fully interactive **Exploratory Data Analysis** of the 259-sample Swiss Jura geochemical training dataset. Built as a zero-dependency, self-contained HTML file powered by **Chart.js**, it provides a complete statistical profile of 7 heavy metal contaminants before any machine learning modelling begins.

## Contents of This Folder

| File | Purpose |
|---|---|
| `index.html` | Interactive EDA dashboard (open in any browser) |
| `gen_dashboard.py` | Python generator script — re-run to rebuild `index.html` |
| `jura_prediction_set.csv` | Source data (259 samples, 12 columns) |
| `jura.csv` | Full raw dataset reference |

## Dashboard Sections

### 1. Summary Statistics (KPI Cards)
Seven colour-coded cards display the **mean, min, max, and standard deviation** for each heavy metal (Cd, Cu, Pb, Co, Cr, Ni, Zn) at a glance.

### 2. Descriptive Statistics Table
A full statistical table per metal: Min · Q1 · Median · Mean · Q3 · Max · Std Dev.

### 3. Frequency Distributions
Individual histogram panels for each metal revealing skewness, clustering, and outlier presence across the training population.

### 4. Correlation Analysis
- **Pearson Correlation Heatmap** (bubble chart): size and colour encode positive/negative correlation strength between all metal pairs.
- **Metal Pair Scatter Plot**: drill-down tool for any two-metal correlation, with dropdown selectors.

### 5. By Rock Type & Land Use
- **Count by Rock Type** doughnut chart (ordered **youngest → oldest** per stratigraphic literature: Quaternary · Portlandian · Kimmeridgian · Sequanian · Argovian)
- **Count by Land Use** doughnut chart (Forest · Pasture · Meadow · Tillage)
- **Mean by Rock Type** bar chart — selectable per metal
- **Mean by Land Use** bar chart — selectable per metal

## Navigation
- **Spatial Maps →** Opens the live WGS84 geographic map dashboard for the prediction set
- **Validation Set →** Jumps to the equivalent EDA dashboard for the 100-sample hold-out set
