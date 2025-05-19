# Road-Accident-Analysis

# Table of Contents
•	Introduction
•	Dashboard Requirements
•	Installation / Usage
•	DAX Formulas Used in Measures
•	Bug / Feature Request
•	Authors

# Introduction
•	This project is aimed at developing a Power BI Dashboard for generating insights about road accident data in the United Kingdom.
•	The dataset can be accessed from this link: Road Accident Data (UK)
# Dashboard Requirements
•	Primary KPI's - Total Casualties and Total Accident values for Current Year and YoY Growth
•	Primary KPI's - Total Casualties by Accident Severity for Current Year and YoY Growth
•	Secondary KPI's - Total Casualties with respect to Vehicle Type for Current Year
•	Monthly Trend showing comparison of Casualties for Current Year and Previous Year
•	Casualties by Road Type for Current Year
•	Current Year Casualties by Area/Location & Day/Night
•	Total Casualties and Total Accident by Location
# Installation / Usage
•	Install Power BI Desktop from Official Power BI Download Site
•	Download data files from link given in Introduction
•	Clone/download this repository to your local machine
•	Open Dashboard report file (Road Accidents Dashboard.pbix) in Power BI Desktop, to access the dashboard's interactivity
# DAX Formulas Used in Measures
1. Total Casualties For Current Year and Year on Year Growth
(a) Current Year To Date Casualties -- CY Casualties Measure
•	CY Casualties = TOTALYTD(SUM(Data[Number_of_Casualties]), 'Calendar'[Date])

(b) Previous Year Casualties -- PY Casualties Measure
•	PY Casualties = CALCULATE(SUM(Data[Number_of_Casualties]), SAMEPERIODLASTYEAR('Calendar'[Date]))

(c) Year on Year Growth of Casualties - YoY Casualties Measure
•	YoY Casualties = ([CY Casualties] - [PY Casualties])/[PY Casualties]

3. Total Accidents for Current Year and Year on Year Growth
(a) Current Year Accidents Count -- CY Accidents Count Measure
•	CY Accidents Count = TOTALYTD(COUNT(Data[Accident_Index]), 'Calendar'[Date])

(b) Previous Year Accidents Count -- PY Accidents Count Measure
•	PY Accidents Count = CALCULATE(COUNT(Data[Accident_Index]), SAMEPERIODLASTYEAR('Calendar'[Date]))

(c) Year on Year Growth of Accidents - YoY Accidents Measure
•	YoY Accidents = ([CY Accidents Count]-[PY Accidents Count])/[PY Accidents Count]

# Bug / Feature Request
If you find a bug (the dashboard gave undesired results), kindly open an issue here by including your search query and the expected result.
If you'd like to request a new function, feel free to do so by opening an issue here. Please include sample queries and their corresponding results.
# Authors
•	Sahani Nilesh
