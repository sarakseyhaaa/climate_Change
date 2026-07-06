
# Climate Change – Exploratory Data Analysis

**Final Project — Group 3**

| Name          | ID        |
|---------------|-----------|
| METH Sreyka   | e20230172 |
| NY Sarakseyha | e20230075 |
| LOY Kimlong   | e20230483 |
| LEU Sophal    | e20230555 |

## Overview

This project explores a global climate change dataset covering **15 countries from 2000 to 2024** (1,000 records). It analyzes key environmental and socio-economic indicators to uncover trends, correlations, and regional differences related to climate change.

## Dataset

The dataset (`climate_change_dataset.csv`) includes the following fields per country/year:

| Column | Description |
|---|---|
| `year` | Year of the record (2000–2024) |
| `country` | Country where data was collected |
| `avg_temperature` | Average annual temperature (°C) |
| `co2_emissions` | CO2 emissions (metric tons per capita) |
| `sea_level_rise` | Annual sea-level rise (mm) |
| `rainfall` | Rainfall (mm) |
| `renewable_energy` | Share of renewable energy (%) |
| `forest_area` | Forest area (%) |
| `extreme_weather_events` | Count of extreme weather events |
| `population` | Population |

Countries are also grouped into regions (Asia, Europe, Africa, Americas, Oceania) for continent-level comparisons.

## Project Structure

```
.
├── climate_change.ipynb        # Main analysis notebook
├── climate_change_dataset.csv  # Source dataset (not included — see Data)
└── README.md
```

## Analysis Workflow

The notebook (`climate_change.ipynb`) is organized as follows:

1. **About the Dataset** – field descriptions and context
2. **Importing Libraries & Dataset** – load and clean the raw data (renaming columns, checking nulls/duplicates)
3. **Exploratory Data Analysis**
   - Outlier detection (IQR method)
   - Trend analysis: CO2 emissions vs. average temperature
   - Sea-level rise vs. temperature, rainfall, and extreme weather events
   - Renewable energy vs. CO2 emissions
   - Population vs. renewable energy, sea-level rise, and extreme weather events
   - Country-level bar charts (temperature, CO2 emissions, renewable energy, rainfall, forest area, population, extreme weather events, sea-level rise)
   - Correlation heatmap of all climate indicators
   - Choropleth map of global CO2 emissions
   - Country deep-dive: China, USA, and UK compared on CO2 emissions, temperature, and rainfall over time

## Key Findings

- CO2 emissions and average global temperature show a positive relationship over time.
- Higher renewable energy adoption doesn't always correspond to lower CO2 emissions at the country level — total energy demand and industrial activity matter too.
- Sea-level rise correlates moderately with the frequency of extreme weather events, though country-level exceptions exist (e.g., Indonesia shows high extreme weather activity despite lower sea-level rise).
- Population size alone does not predict higher emissions, temperatures, or extreme weather exposure.
- China shows the most volatile year-to-year emissions and temperature trends, the USA is consistently high but stable, and the UK trends lower and smoother — likely reflecting differences in industrial activity and environmental policy.

## Libraries Used

- **pandas** / **numpy** – data manipulation
- **matplotlib** / **seaborn** – static visualizations
- **plotly** – interactive visualizations (choropleth map)

## Getting Started

1. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn plotly jupyter
   ```
2. Place `climate_change_dataset.csv` in the project root.
3. Launch the notebook:
   ```bash
   jupyter notebook climate_change.ipynb
   ```