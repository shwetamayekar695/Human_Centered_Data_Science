[![MIT License](https://img.shields.io/apm/l/atomic-design-ui.svg?)](https://github.com/shwetamayekar695/Human_Centered_Data_Science/blob/main/LICENSE)

#Project - Part 1 - Common Analysis

**DATA 512: Human-Centered Data Science**


### Goal:
Common Analysis sets the stage for the subsequent assignments of the course project. My analysis was conducted using Covid-19 data for Davidson County in Tennessee state.
During the last three years we all have been experiencing a global pandemic. This has been tragic and disruptive to many countries and has taken a deep personal toll on many individuals and their families. 
One aspect that has been hard to miss in the last three years is the datafication of the pandemic. That is, many aspects of the individual toll of the pandemic have been collected, aggregated and re-represented as data. This datafication gives us the privilege to examine the pandemic from potentially many different perspectives to understand how it has changed lives and how it has changed society.
This is a human centered data science analysis of some available COVID-19 data.


#### Assigned County: Davidson, Tennessee

### Data Sources:
- [John Hopkins University COVID-19 data](https://www.kaggle.com/datasets/antgoldbloom/covid19-data-from-john-hopkins-university).
- [Masking Mandates by County](https://data.cdc.gov/Policy-Surveillance/U-S-State-and-Territorial-Public-Mask-Mandates-Fro/62d6-pm5i)
- [Mask Compliance Survey](https://github.com/nytimes/covid-19-data/tree/master/mask-use)

### Input Data Files
- Data/RAW_us_confirmed_cases.csv
- Data/mask-mandate.csv
- Data/mask-use-by-county.csv

### Data Description for RAW_us_confirmed_cases.csv (only relevant columns extracted)

| Feature        | Data type | Description                                                         |
|----------------|-----------|---------------------------------------------------------------------|
| Province_State | String    | The name of state                                                   |
| Admin2         | String    | The name of the county                                              |
| FIPS           | float64   | Unique ID for county, state                                         |
| \<date>        | int       | Confirmed number of cases for each day from 1/22/2020 to 10/30/2022 |

### Data Description for mask-mandate.csv (only relevant columns extracted)

| Feature                        | Data type | Description                                          |
|--------------------------------|-----------|------------------------------------------------------|
| State_Tribe_Territory          | String    | Code name of state                                   |
| County_Name                    | String    | The name of the county                               |
| date                           | String    | mask mandate date                                    |
| Face_Masks_Required_in_Public  | String    | Yes/No for mask mandates                             |

COUNTYFP        int64
NEVER         float64
RARELY        float64
SOMETIMES     float64
FREQUENTLY    float64
ALWAYS        float64

### Data Description for mask-use-by-county.csv
'NEVER', 'RARELY', 'SOMETIMES', 'FREQUENTLY', 'ALWAYS' are survey responses to “How often do you wear a mask in public when you expect to be within six feet of another person?”

| Feature       | Data type | Description                                                         |
|---------------|-----------|---------------------------------------------------------------------|
| COUNTYFP      | int64     | Unique ID for county, state (FIPS)                                  |
| NEVER         | float64   | survey response                                                     |
| RARELY        | float64   | survey response                                                     |
| SOMETIMES     | float64   | survey response                                                     |
| FREQUENTLY    | float64   | survey response                                                     |
| ALWAYS        | float64   | survey response                                                     |


### Final Visualization:
#### (https://github.com/shwetamayekar695/Human_Centered_Data_Science/blob/main/project/part1-common-analysis/Final_Visualization_Part1_Analysis.png)
