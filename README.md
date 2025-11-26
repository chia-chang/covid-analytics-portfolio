# Python Portfolio: COVID Analytics Automation
Automated COVID-19 data pipeline that cut reporting time by 80% (2-3 hours → 10 minutes).
Note: All data is synthetically generated for demonstration purposes.

## Overview
This project demonstrates a reproducible COVID-19 data analytics workflow inspired by previous work at IBM. Rapid and accurate analysis of COVID-19 data is critical for informed decision-making during the pandemic. This project demonstrates an end-to-end analytics system that automates the entire workflow from data cleaning and integration to metric calculation and report generation, which reduced reporting time by **80%** (from 2-3 hours of manual work to 10 minutes automated).
This system showcases my approach to solving business problems at scale: identify inefficiencies, design comprehensive solutions, and deliver measurable impact through automation.

## The Problem
Some critical data challenges healthcare organizations faced during the pandemic:
- Hours of manual data aggregation from multiple sources daily
- Inconsistent metric calculations across teams led to conflicting reports
- Delayed reporting meant decisions were made on outdated information
- Manual processes couldn't scale with increasing reporting demands

## Solution
Python-based analytics system with these key points:
- **Data Integration Pipeline**: Automates cleaning, validation, and standardization from multi-source COVID data
- **Standardized metrics** (7-day rolling averages, positivity rates, and week-over-week changes): Ensure consistency across all outputs
- **Automated Reporting**: Generates a publication-ready Excel report and visualizations for executive audiences

## My Philosophy
- System-level thinking:
  The solution addresses the entire workflow, not just isolated pieces. From data ingestion to executive reporting, each component works together to deliver end-to-end value.
- Reliability and maintainability:
  Keeping the code clean and robust, so it would be easy for anyone to understand and modify the logic without extensive documentation.
- Business-focused outputs
  Reports and visualizations are designed for stakeholder consumption, not just technical audiences. Clean formatting, clear messaging, and actionable insights.

## Impact
- **80% reduction of reporting time**: From 2~3 hours to 10 minutes
- **Metrics consistency**: Eliminated discrepancies between teams
- **Same-day insights**: Enables real-time decision-making with current data
- **Scalable Solutions**: Handles increasing data volumes without additional changes

## Notebooks Description
Each notebook covers a different stage of the analysis pipeline.

- Data Cleaning and Integration ([View Notebook](../notebooks/Data_Cleaning_and_Integration.ipynb))  
  Shows data loading, cleaning steps, and integration of sources
  - Generate a raw dataset (`covid_raw_data.csv`) for use in this file
  - Clean column names, handle missing values, and standardize date formats
  - Generate derived metrics such as 7-day averages, cumulative totals, and week-over-week changes
  - Exporting the processed dataset (`covid_integrated_data.csv`) for downstream reporting

- Automated Reporting ([View Notebook](../notebooks/Automated_Reporting.ipynb))  
  Demonstrates how the reporting process can be run automatically
  - Loads the processed dataset (`covid_integrated_data.csv`)
  - Calculates key metrics (averages, trends, cumulative totals)
  - Generates publication-ready visualizations
  - Produces a multi-sheet Excel report that includes daily, weekly, and summary data (`COVID_Report_YYYYMMDD.xlsx`)

## Data Description
- Raw Data (`covid_raw_data.csv`) ([View data](../data/raw/covid_raw_data.csv))  
  Synthetic daily time series mimicking COVID-19 pandemic data (2020-03-01 to 2024-01-31):  
  - `Date`: calendar date  
  - `Cases`: daily new confirmed cases  
  - `Tests`: daily diagnostic tests performed  
  - `Hospitalizations`: daily hospital admissions  
  - `Deaths`: daily reported deaths  
  - `Vaccinations`: daily vaccinations administered

- Processed Data (`covid_integrated_data.csv`) ([View data](../data/processed/covid_integrated_data.csv))  
  Cleaned, merged, and enhanced the dataset with additional calculated features:  
  - 7-day rolling averages  
  - Positivity rate (cases/tests)  
  - Week-over-week changes  
  - Cumulative totals

 
## Outputs Description
- Excel Report (`COVID_Report_YYYYMMDD.xlsx`) ([View report](../outputs/reports/COVID_Report_20251113.xlsx))  
  Summarizes daily and weekly key COVID-19 metrics and compares recent performance against prior weeks
  - Sheet 1: Summary
  - Sheet 2: Daily Data (Last 90 Days)
  - Sheet 3: Weekly Summary
  - Sheet 4: Key Metrics Comparison

- Charts ([View sample charts](../outputs/charts))
  - **1_daily_cases_trend.png**: Daily Cases with 7-Day Moving Average
  - **2_hospitalizations_trend.png**: Daily hospitalization with 7-Day Moving Average
  - **3_positivity_rate.png**: 7-day average COVID-19 test positivity rate with a 5% reference line recommended by the WHO, indicating concerning level of virus spread  



## Technologies Used
- Python 3.x  
- Pandas & NumPy for data processing  
- Matplotlib & Seaborn for visualization  
- OpenPyXL / XlsxWriter for Excel report automation  
