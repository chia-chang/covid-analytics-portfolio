# Outputs Directory

This folder contains the reports and charts that are generated in this project.

## Reports
- **COVID_Report_20251112.xlsx:** 
  This automatically generated report is designed to replace manual spreadsheet work. This file is produced by the `Automated_Reporting.ipynb` notebook.
  It summarizes daily and weekly key COVID-19 metrics and compares recent performance against prior weeks, enabling quick insights for stakeholders.
  
  - Sheet 1: Summary
    - Latest key statistics such as daily and 7-day averages for cases, tests, hospitalizations, deaths, and positivity rate  
    - Week-over-week changes for cases and hospitalizations  
    - Cumulative totals for cases, deaths, and vaccinations  
  - Sheet 2: Daily Data (Last 90 Days)
    - Daily records showing cases, tests, hospitalizations, deaths, vaccinations, and positivity rate  
    - 7-day moving averages to track short-term trends and anomalies 
  - Sheet 3: Weekly Summary
    - Aggregated weekly totals for cases, tests, hospitalizations, deaths, and vaccinations  
    - Provides a higher-level view of trends over time  
  - Sheet 4: Key Metrics Comparison
    - Side-by-side comparison of the latest 7-day averages and week-over-week changes for cases, hospitalizations, deaths, vaccinations, and positivity rate  
    - Easy to spot emerging trends at a glance 
  **generated from**: [Automated_Reporting.ipynb](../notebooks/Automated_Reporting.ipynb)


## Charts
- `1_daily_cases_trend.png`: Daily Cases with 7-Day Average
  - Daily reported COVID-19 cases as bars over the last six months.  
  - 7-day moving average line to smooth out daily fluctuations and reveal trends.  
  - Easy to track how case counts are evolving with seasonal or outbreak patterns.  
  **generated from**: [Automated_Reporting.ipynb](../notebooks/Automated_Reporting.ipynb)
    
- `2_hospitalizations_trend.png`: 
  - Daily hospitalizations related to COVID-19 as bars.  
  - Includes a 7-day average line for trend insight.  
  **generated from**: [Automated_Reporting.ipynb](../notebooks/Automated_Reporting.ipynb)
    
- `3_positivity_rate.png`: 
  - 7-day average COVID-19 test positivity rate as a filled line graph.  
  - Includes a red dashed reference line at 5% (the WHO recommended threshold to indicate concerning levels of virus spread).  
  - Shows testing sufficiency and the underlying spread of the virus.     
  **generated from**: [Automated_Reporting.ipynb](../notebooks/Automated_Reporting.ipynb)


Suggestions, feedback, or additional notebooks are always welcome!
