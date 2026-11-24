# CISC7204 Assignment 02 — Data Visualization with Python

**WONG SI IEONG (MC632743) · CISC7204 Class A**

## Overview

Completed work for Assignment 02, *Data Visualization with Python*. Two visualization notebooks (Final and Practice) and two Plotly/Dash dashboards are included. The notebooks run from a clean kernel. The two CSV datasets are fetched from the course cloud URLs; the US states GeoJSON is shipped locally for the optional folium map.

## Repository structure

```
assignment-02-data-visualization/
├── final-automobile-sales/
│   ├── final_lab01.ipynb
│   └── us-states.json
├── practice-wildfires/
│   └── practice_lab01.ipynb
├── dash/
│   ├── final/Final-Lab02-dashboard/        # Automobile sales Dash app
│   └── practice/Practice-Lab02-dashboard/ # Wildfire Dash app
├── README.md
└── requirements.txt
```

## Final: Automobile sales visualizations

- **Question**: How do automobile sales, advertising spend, GDP, unemployment, and consumer confidence differ between recession and non-recession periods?
- **Data**: `automobile-sales.csv`, fetched from the IBM SkillsNetwork DV0101EN course URL; `us-states.json` is the GeoJSON used by the optional choropleth map.
- **Methods/tools**: pandas, Matplotlib, Seaborn, Folium; line, bar, pie, bubble, scatter, subplot, and choropleth charts.
- **Results**: 12 visualizations covering sales trends over time, advertising expenditure by vehicle type, GDP variation in recession periods, seasonality, consumer confidence, and a recession-period sales map by city.
- **Limitation**: the charts describe this historical sample; the recession flag is binary, and the city-level map hides variation within cities.

## Practice: Australian wildfire analysis

- **Question**: How do estimated fire area and fire pixel count vary over time and across Australian regions?
- **Data**: `Historical_Wildfires.csv`, fetched from the IBM SkillsNetwork DV0101EN course URL.
- **Methods/tools**: pandas, Matplotlib, Seaborn, Folium; line, bar, pie, histogram, scatter plots, and a region map.
- **Results**: 9 visualizations of fire area by year and month, fire brightness by region, vegetation-fire pixel share, brightness distribution by region, and radiative power versus brightness.
- **Limitation**: results are regional aggregates; the brightness and pixel measures are satellite-derived estimates rather than ground-level fire counts.

## Dash dashboards

- **Final** — `dash/final/Final-Lab02-dashboard/DV0101EN-Final-Assign-Part-2-Questions.py`: dropdown for yearly versus recession statistics and a year selector; four Plotly charts in each report view. Runs on port 8054.
- **Practice** — `dash/practice/Practice-Lab02-dashboard/Dash_wildfire.py`: region radio buttons and a year dropdown; a pie chart and a bar chart for the selected region and year. Runs on port 8053.

## How to run

Notebooks:

```bash
pip install -r requirements.txt
jupyter notebook final-automobile-sales/final_lab01.ipynb
jupyter notebook practice-wildfires/practice_lab01.ipynb
```

Dash apps:

```bash
cd dash/final/Final-Lab02-dashboard
python DV0101EN-Final-Assign-Part-2-Questions.py

cd dash/practice/Practice-Lab02-dashboard
python Dash_wildfire.py
```

## Source and permissions

The datasets come from the IBM Developer SkillsNetwork DV0101EN course labs provided for CISC7204 coursework, retained here to reproduce the submitted notebooks and apps. No passwords, API keys, or personal records are included.
