# COVID-19 Data Analytics Demonstration
This repository demonstrates a reproducible COVID-19 data analytics workflow inspired by previous work at IBM.  
All data included here are synthetically generated for demonstration purposes and do not contain proprietary or sensitive information.

## Background and Objective
Rapid and accurate analysis of COVID-19 data is critical for informed decision-making during the pandemic.  
This project demonstrates an end-to-end analytics pipeline that cleans, integrates, and analyzes multi-source COVID-19 data, automates key metric calculations, generates reports and charts.

## Highlights
- Synthetic raw data generation to mimic real-world COVID-19 datasets  
- Data cleaning and integration, including 7-day rolling averages and week-over-week changes  
- Automated reporting with multi-sheet Excel files and trend charts, significantly improving reporting efficiency by **80%** (from 2-3 hours of manual work to 10 minutes automated)

## Notebooks Description
Each notebook covers a different stage of the analysis pipeline.

### `Data_Cleaning_and_Integration.ipynb` 
Shows data loading, cleaning steps, and integration of sources
- Generated a raw dataset (`covid_raw_data.csv`) for use in this file
- Clean column names, handle missing values, and standardize date formats
- Generate derived metrics such as 7-day averages, cumulative totals, and week-over-week changes
- Exporting the processed dataset (`covid_integrated_data.csv`) for use in the (`Automated_Reporting.ipynb`) notebook

### `Automated_Reporting.ipynb`
Demonstrates how the reporting process can be run automatically
- Loads the processed dataset (`covid_integrated_data.csv`)
- Calculates key metrics (averages, trends, cumulative totals)
- Generates publication-ready visualizations
- Produces a multi-sheet Excel report that includes daily, weekly, and summary data (`COVID_Report_YYYYMMDD.xlsx`)

## Data Description
### Raw Data (`covid_raw_data.csv`)
Synthetic daily time series mimicking COVID-19 pandemic data (2020-03-01 to 2024-01-31):  
- `Date`: calendar date  
- `Cases`: daily new confirmed cases  
- `Tests`: daily diagnostic tests performed  
- `Hospitalizations`: daily hospital admissions  
- `Deaths`: daily reported deaths  
- `Vaccinations`: daily vaccinations administered

**generated from**: [Data_Cleaning_and_Integration.ipynb](../notebooks/Data_Cleaning_and_Integration.ipynb)

### Processed Data (`covid_integrated_data.csv`)
Cleaned, merged, and enhanced dataset with additional calculated features:  
- 7-day rolling averages  
- Positivity rate (cases/tests)  
- Week-over-week changes  
- Cumulative totals

**generated from**: [Data_Cleaning_and_Integration.ipynb](../notebooks/Data_Cleaning_and_Integration.ipynb)

## Outputs Description
### Daily/Weekly Report (`COVID_Report_YYYYMMDD.xlsx`)
Summarizes daily and weekly key COVID-19 metrics and compares recent performance against prior weeks
- Sheet 1: Summary
- Sheet 2: Daily Data (Last 90 Days)
- Sheet 3: Weekly Summary
- Sheet 4: Key Metrics Comparison

**generated from**: [Automated_Reporting.ipynb](../notebooks/Automated_Reporting.ipynb)

### Charts
- `1_daily_cases_trend.png`: Daily Cases with 7-Day Moving Average
- `2_hospitalizations_trend.png`: Daily hospitalization with 7-Day Moving Average
- `3_positivity_rate.png`: 7-day average COVID-19 test positivity rate with a 5% reference line recommended by the WHO indicating concerning level of virus spread

**generated from**: [Automated_Reporting.ipynb](../notebooks/Automated_Reporting.ipynb)

## Technologies Used
- Python 3.x  
- Pandas & NumPy for data processing  
- Matplotlib & Seaborn for visualization  
- OpenPyXL / XlsxWriter for Excel report automation  

