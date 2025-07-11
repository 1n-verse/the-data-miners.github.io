---
title: Mini Project 1
date: 2025-07-10
author: Income vs. Air Quality
---
<iframe src="/plotly/income_aqi.html" width="100%" height="400px" style="border:none;"> </iframe>

---
The goal of the project was to determine if there was a correlation between income (measured by median income of a specific location, e.g. county/city) and air quality (measured by PM2.5, or particulate matter with a diameter of 2.5 micrometers or less).

# Data acquisition
Data acquisition involved collecting data via the United States Census Bureau website, where we submitted a request for [median income data for cities across the United States in 2023](:*
https://api.census.gov/data/2023/acs/acs5?get=NAME,B19013_001E&for=place:*&in=state:*). Because the second part of the project required using counties as locations for FIPS, the project collected this additional information from the [NIH HD Pulse California income data](https://hdpulse.nimhd.nih.gov/data-portal/social/table?age=001&age_options=ageall_1&demo=00011&demo_options=income_3&race=00&race_options=race_7&sex=0&sex_options=sexboth_1&socialtopic=030&socialtopic_options=social_6&statefips=06&statefips_options=area_states). 

For the part of the project that analyzed cities across the United States, AQI data from the same time period was collected via [the Air Quality Open Data Platform[https://aqicn.org/data-platform/token-confirm/e3fc5e05-5205-4a36-a70d-583165b81fef]. AQI for California counties was also acquired from [NIH HD Pulse](https://hdpulse.nimhd.nih.gov/data-portal/physical/table?age=001&age_options=ageall_1&demo=234&demo_options=air_pollution_1&physicaltopic=002&physicaltopic_options=physical_2&race=00&race_options=raceall_1&sex=0&sex_options=sexboth_1&statefips=06&statefips_options=area_states).

# Data cleaning
The project converted data into dataframe formats. Excess columns from AQI and Income were removed, leaving only the city/county, AQI, and income data. Income and AQI were converted into integer and float values, respectively. Then, a dataframe for both income and AQI were created. Because the AQI data contained significantly less observations than the income data, observations in the income data that contained a city/county not recorded in AQI data were deleted. 

# Exploratory Data Analysis
Income and AQI were related via a linear relationship. Linear correlation was very weak, with a correlation coefficient of -0.09.

# Modeling
Income vs. AQI were plotted on a scatterplot.


