[![MIT License](https://img.shields.io/apm/l/atomic-design-ui.svg?)](https://github.com/shwetamayekar695/Human_Centered_Data_Science/blob/main/LICENSE)

# Project - Part 2 - Extension Analysis

**DATA 512: Human-Centered Data Science**


## Goal:
For my extension analysis, I analyzed the impact of Covid-19 on the common man. I wanted to understand how the pandemic affected the spending capacity of the consumer as well as their employment growth in common industry sectors. This analysis is relevant and important so one is equipped to tackle repercussions of another such global crises. As per WebMD, the chance of someone seeing a pandemic like COVID-19 during their lifetime is about 38%, which could double in the years to come. My analysis and findings can be an extension to countless studies that have been conducted to investigate and understand how the consumer confidence index (CCI) and employment growth were affected during the pandemic. If we can foresee a similar situation due to a crisis, then we can be better prepared for its consequences.


#### Assigned County: Davidson, Tennessee

## Data Sources:
- [John Hopkins University COVID-19 data](https://www.kaggle.com/datasets/antgoldbloom/covid19-data-from-john-hopkins-university)
- [Employment growth, Davidson County](https://datausa.io/profile/geo/davidson-county-tn)
- [Consumer Confidence Index, OECD](https://data.oecd.org/leadind/consumer-confidence-index-cci.htm#indicator-chart)
- [Vaccination data by CDC](https://data.cdc.gov/Vaccinations/COVID-19-Vaccinations-in-the-United-States-County/8xkx-amqh/data)

## Input Data Files
- Data/RAW_us_confirmed_cases.csv
- Data/Employment by Industry Sector.csv
- Data/consumer_confidence_index_USA.csv
- Data/COVID-19_Vaccinations_in_the_United_States_DavidsonCounty.csv

### Data Description for RAW_us_confirmed_cases.csv (only relevant columns extracted)

| Feature        | Data type | Description                                                         |
|----------------|-----------|---------------------------------------------------------------------|
| Province_State | String    | The name of state                                                   |
| Admin2         | String    | The name of the county                                              |
| FIPS           | float64   | Unique ID for county, state                                         |
| \<date>        | int       | Confirmed number of cases for each day from 1/22/2020 to 10/30/2022 |


### Data Description for "Employment by Industry Sector.csv" (only relevant columns extracted)

| Feature                | Data type | Description                                                         |
|------------------------|-----------|---------------------------------------------------------------------|
| Date                   | String    | Monthly Timestamp                                                   | 
| Supersector            | String    | The name of industry sector                                         |
| NSA Employees Growth   | float64   | Employment growth rate in %                                         |

### Data Description for consumer_confidence_index_USA.csv (only relevant columns extracted)

| Feature                | Data type | Description                                                         |
|------------------------|-----------|---------------------------------------------------------------------|
| Time                   | String    | Monthly Timestamp                                                   | 
| Value                  | float64   | Consumer Confidence index value                                     |

### Data Description for COVID-19_Vaccinations_in_the_United_States_DavidsonCounty.csv (only relevant columns extracted)

| Feature                  | Data type | Description                                                         |
|--------------------------|-----------|---------------------------------------------------------------------|
| Date                     | String    | Daily Timestamp                                                     | 
| Administered_Dose1_Recip | int64     | Number of first doses registered on the day                         |


## Code:
Code for analysis can be found here [Part2-Extension_Analysis.ipynb](https://github.com/shwetamayekar695/Human_Centered_Data_Science/blob/main/project/part2-extension-analysis/Part2-Extension_Analysis.ipynb)

## Research Questions:
My focus was on analyzing the impact of Covid-19 in the Davidson County of Tennessee. Therefore, based on these research studies, I devised the following research questions -
1) Did the rising cases of Covid-19 affect month-over-month employment growth in Davidson County?
2) Did the consumer spending capacity take a hit due to rising cases & its impact on employment rate?
3) Did the county’s vaccination rate stabilize these monetary measures - employment growth and consumer spending capacity?

## Findings:

### 1) Heavy Decline in Consumer Confidence Index
#### ![CCI_Trendline_after_Covid-19](https://github.com/shwetamayekar695/Human_Centered_Data_Science/blob/main/project/part2-extension-analysis/visualizations/%20CCI_Trendline_after_Covid-19.png)

### 2) Comparing CCI with Employment Rate and observing a similar trend
#### ![Trendlines_for_CCI_Employment_Growth](https://github.com/shwetamayekar695/Human_Centered_Data_Science/blob/main/project/part2-extension-analysis/visualizations/Trendlines_for_CCI_Employment_Growth.png)

### 3) Correlation Analysis

| Variables                                 | Confirmed new cases | Employment growth | CCI   | Count of 1st vaccine doses administered |
|-------------------------------------------|---------------------|-------------------|-------|-----------------------------------------|
| Confirmed new cases                       |  1                  |  -0.28            | -0.38 | -0.82                                   |
| Employment growth                         | -0.28               |  1                |  0.63 |  0.90                                   |
| CCI                                       | -0.38               |  0.63             |  1    |  0.96                                   |
| Count of first vaccine doses administered | -0.82               |  0.90             |  0.96 |  1                                      |


## Summary:
You can see how the confirmed cases are negatively correlated with employment growth (-0.28). There is also a more significant negative correlation between confirmed cases and CCI (-0.38). However, when the first vaccine doses were administered there was an extremely significant positive correlation between vaccination doses and employment growth (0.9) as well as a positive correlation between vaccination doses and CCI (0.96). This shows a positive association between vaccination and monetary measures like employment growth and consumer confidence index.
Post Vaccination drives, there was a 8.45% YEAR-OVER-YEAR GROWTH in Employment rate between May 2020 and May 2021. There was also a 1.5% YEAR-OVER-YEAR GROWTH in CCI between April 2020 and April 2021.
