# Project-1-Air Quality Analysis
Text "bold text" text.
---
## Project Files

This includes files for Project no. 1
## Overview
This project analyzes air quality sensor data to explore patterns in:
- PM 2.5
- PM 10.0
- VOC
- Temperature & humidity categories
- Altitude relationships
- AQI health-risk screening (Unhealthy for Sensitive Groups or worse)
## Data Expectations 
The analysis loads the CSV into a Pandas DataFrame named air_data. Key columns used:
- date (formatted like mm/dd/yy)
- sensor.name
- pm2.5_atm
- pm10.0_atm
- voc
- temperature
- humidity
- sensor.altitude
## Analysis Summary
## Step 1) Summary Statistics & Top Locations
- Bullet Groups data by sensor.name
- Bullet Calculates mean/median for PM2.5, PM10, and VOC
- Bullet Finds top 5 locations by mean pollutant values
## Step 2) Max Values: When and Where?
Identifies the dates and sensor locations where the maximum PM2.5, PM10, and VOC values occurred
## Step 3) Temperature & Humidity Categorization
Creates categories based on assignment bins:
- Bullet Humidity
- Bullet Low: < 50%
- Bullet High: 50–80%
- Bullet Very High: > 80%
- Bullet Temperature (°F)
- Bullet Below Freezing: < 32
- Bullet Cool: 32–50
- Bullet Warm: 51–70
- Bullet Hot: > 70
## Step 4) EPA Health Risk Screening (Simplified Categories)
This step screens for potential air quality health risks using EPA-style category breakpoints applied directly to concentration values.
For PM2.5:
- Bullet Good: 0.0–12.0
- Bullet Moderate: 12.1–35.4
- Bullet Unhealthy for Sensitive Groups: 35.5–55.4
- Bullet Unhealthy: 55.5–150.4
- Bullet Very Unhealthy: 150.5–250.4
- Bullet Hazardous: > 250.4
For PM10:
- Bullet Good: 0–54
- Bullet Moderate: 55–154
- Bullet Unhealthy for Sensitive Groups: 155–254
- Bullet Unhealthy: 255–354
- Bullet Very Unhealthy: 355–424
- Bullet Hazardous: > 424
The code then filters and reports all events where:
“Unhealthy for Sensitive Groups” or worse occurred and lists when and where those events happened for both PM2.5 and PM10.
## Step 5) Altitude vs Air Quality
- Bullet Aggregates to one row per sensor
- Bullet Computes correlations between altitude and mean pollutant values
