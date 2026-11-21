# Gode-Water-Dashboard
# Gode Zone Water Dashboard: Drought, Flood & Evapotranspiration

## 1. Objective
This project provides a multi-variable water analysis for the Shabelle (Gode) Zone in the Somali Region of Ethiopia. It calculates historical drought, surface runoff (flood), and crop water demand (evapotranspiration) for the period 2021–2025 to support irrigation and disaster risk planning.

## 2. Study Area
- **Country:** Ethiopia
- **Region:** Somali
- **Zone:** Shabelle (Gode)
- **Area:** ~34,005 km²

## 3. Data & Methods
All data was extracted using the Google Earth Engine Python API.
- **Drought:** Standardized Precipitation Index (SPI-3) using CHIRPS daily rainfall and a 30-year baseline (1991–2020).
- **Flood (Runoff):** SCS Curve Number (SCS-CN) method, combining CHIRPS rainfall with ESA WorldCover land cover data.
- **Evapotranspiration (ET₀):** FAO-56 Penman-Monteith equation using ERA5-Land climate data (temperature, wind, radiation).

## 4. Workflow
1. Extracted daily datasets from Earth Engine for 2021–2025.
2. Aggregated daily data to monthly totals.
3. Applied scientific formulas (Gamma distribution for SPI, SCS-CN for runoff, and Penman-Monteith for ET).
4. Exported results to CSV and generated professional visualizations in R.

## 5. Key Results (Combination Chart)
![Gode Dashboard](Gode_Final_Combination_Dashboard.png)
*The dashboard combines rainfall and flood runoff (bars) with crop water demand (ET0) and drought severity (SPI) to show the full water balance of the zone.*

## 6. Repository Contents
- `Gode_Irrigation_Analysis.ipynb`: Google Earth Engine Python code.
- `Gode_Analysis_Charts.R`: R code for visualization.
- `Gode_Monthly_*.csv`: Exported raw data (Rainfall, Flood, ET).
- `*.png`: Generated charts (Drought, Flood, ET, Dashboard).

## 7. Author
[Your Name]
