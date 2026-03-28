# LinkedIn Post — Prediction Set EDA Dashboard

---

📊 **From Raw Geochemical Data to Actionable Insight: How EDA Sets the Stage for Spatial AI**

Before any model trains, the data must speak. I recently completed an in-depth Exploratory Data Analysis of the classical **Swiss Jura Heavy Metals dataset** — 259 training samples, 7 contaminants (Cd, Cu, Pb, Co, Cr, Ni, Zn), and a surprisingly rich geological context.

Rather than static plots, I built a fully **interactive EDA dashboard** (zero dependencies — pure HTML + Chart.js) that surfaces structure others overlook:

🔬 **Statistical KPIs** — Mean, StdDev, IQR for every metal at a glance

📈 **Frequency Distributions** — 15-bin histograms revealing the heavy right-skew typical of geochemical log-normal distributions (Zinc, I'm looking at you)

🔗 **Pearson Correlation Heatmap** — a bubble chart visual that immediately flags the strong Co-Cr-Ni triad common to mafic mineralisation signatures

🪨 **Geological Context** — rock type and land use breakdowns, with rock formations now ordered **youngest → oldest** by stratigraphic age (Quaternary at ~2.58 Ma through to Argovian at ~166 Ma). A simple reordering, but one that immediately reveals which formations dominate the training distribution.

The big takeaway? Pb and Cd cluster predominantly in **Portlandian and Kimmeridgian formations**, while Co and Cr are more evenly spread — a signal worth encoding into any spatial feature engineering pipeline.

This dashboard is the entry point to a 4-page interconnected geospatial analysis suite that includes live WGS84 maps, live categorical filtering, and a combined study area boundary polygon.

What EDA steps do you consider non-negotiable before spatial modelling? 👇

#DataScience #Geochemistry #EDA #SpatialAnalysis #MachineLearning #Python #ChartJS #GeoAI #SwissJura
