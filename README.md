# VRI-Decision-Support-Tool-Using-R

## Overview
The VRI-DSS (Variable Rate Irrigation Decision Support System) script, created by Ahmed Elnaggar on 2023-08-23, performs advanced agronomic and hydrological computations to estimate weather data, reference evapotranspiration (ETo), crop coefficients (Kcb), and soil-water balance. The script integrates spatial data, including soil types, to optimize irrigation decisions and provide insights into water use efficiency for different soil zones.

## Requirements
### R Packages:
- readxl: To read data from Excel files.
- dplyr: Data manipulation.
- lubridate: Date-time handling.
- reshape2: Data reshaping for visualizations.
- ggplot2: Data visualization.
- sf: For handling spatial data (shapefiles).
- raster: For raster data handling.
- gridExtra: For arranging multiple plots.
### Input Data:
1- Weather Data (Excel): Contains daily weather data (temperature, humidity, etc.).
- File: HR-barley.xlsx
- Sheet: barley
2- Shapefile (Spatial Data): Contains spatial data for soil zones.
- File: barley-hr-4soils2.shp

## Key Functions
1- Reading Weather Data:
- Reads and summarizes weather data (Date, Precipitation, Min/Max Temperature, Wind Speed, Solar Radiation, Relative Humidity).
  
2- ETo Calculation:
- Calculates reference evapotranspiration (ETo) using the FAO Penman-Monteith equation based on daily weather data and location (latitude, elevation).

3- Crop Coefficients (Kcb):
- Determines crop coefficients based on growth stages: initial, development, mid-season, and late-season.

4- Soil-Water Balance:
- Calculates soil-water balance components (e.g., drainage, deficit, irrigation needs) using soil and weather data.

5- Spatiotemporal Model:
- Integrates soil zones and temporal weather data to create a spatio-temporal model for irrigation scheduling.

6- Visualization:
- Generates plots, including:
  - Soil Water Deficit Map.
  - Temporal Irrigation Needs.
  - Crop Water Use.
  - Water Efficiency Analysis.

## Output
1- Spatio-Temporal Data:
- A CSV file can be generated to store irrigation and water balance calculations per soil zone and day.

2- Plots:
- Various plots visualizing soil-water deficit, irrigation needs, and water use efficiency are generated for further analysis.

## How to Use
1- Prepare the Data:
- Ensure weather and spatial data files are in place and correctly formatted.
2- Run the Script:
- Execute the script in an R environment, making sure all required packages are installed.
3- Analyze Outputs:
- Review the plots and data outputs to guide irrigation decisions.
## Future Improvements
- Expand the model to incorporate real-time weather data.
- Add more soil zones and fine-tune resolution for better irrigation precision.
- Automate irrigation scheduling with trigger-based thresholds.
