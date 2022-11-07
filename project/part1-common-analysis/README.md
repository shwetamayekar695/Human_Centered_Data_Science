[![MIT License](https://img.shields.io/apm/l/atomic-design-ui.svg?)](https://github.com/shwetamayekar695/Human_Centered_Data_Science/blob/main/LICENSE)

# Project - Part 1 - Common Analysis

**DATA 512: Human-Centered Data Science**


### Goal:
Common Analysis sets the stage for the subsequent assignments of the course project. My analysis was conducted using Covid-19 data for Davidson County in Tennessee state.
During the last three years we all have been experiencing a global pandemic. This has been tragic and disruptive to many countries and has taken a deep personal toll on many individuals and their families. 
One aspect that has been hard to miss in the last three years is the datafication of the pandemic. That is, many aspects of the individual toll of the pandemic have been collected, aggregated and re-represented as data. This datafication gives us the privilege to examine the pandemic from potentially many different perspectives to understand how it has changed lives and how it has changed society.
This is a human centered data science analysis of some available COVID-19 data.


#### Assigned County: Davidson, Tennessee

### Data Sources:
- [John Hopkins University COVID-19 data](https://www.kaggle.com/datasets/antgoldbloom/covid19-data-from-john-hopkins-university)
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


### External Research:
Since there was no mask mandate data available in the given dataset for Tennessee State/Davidson County, I did some external research.

Sources:
- [Tennessee Areas without mask mandates show higher death rate](https://www.vumc.org/health-policy/news-events/tennessee-areas-without-mask-requirements-have-higher-death-toll-capita)
- [US News Tennessee Mask Mandate Information](https://www.usnews.com/news/best-states/articles/these-are-the-states-with-mask-mandates#tenn)

As per the first report on Tennessee counties, the areas where mask requirements were instituted showed substantially lower death rates due to COVID-19 as compared to areas without mask requirements, according to an analysis by Vanderbilt Department of Health Policy researchers. The analysis, led by John Graves, PhD, associate professor of Health Policy and director of the Vanderbilt Center for Health Economic Modeling, finds that early adopting counties in Tennessee saw their death rate begin to decline by late July of 2020, while later adopting counties saw declines in August and September. Non-adopting counties continue to see death rates rise, the researchers found. Additionally, mask requirements were adopted between July 10 2020 and first week of August 2020. Now death rate going high means that the case rate was also going high in this case. We do observe a dip in new cases after July 2020.

As per the second report, Tennessee Gov. Bill Lee signed an executive order in April 2021 that removed local authority on mask mandates. Coincidently, we do observe a sudden sharp increase in new cases following a few weeks of when the mandate was officially lifted. We can associate this sudden steep rise due to relatively less or no usage of masks.


### Code:
Code for analysis can be found here [Part1_Project_Common_Analysis.ipynb](https://github.com/shwetamayekar695/Human_Centered_Data_Science/blob/main/project/part1-common-analysis/Part1_Project_Common_Analysis.ipynb)


### Final Visualization:
#### ![Visualization_of_Part1_Common_Analysis-DATA512](https://github.com/shwetamayekar695/Human_Centered_Data_Science/blob/main/project/part1-common-analysis/Visualization_of_Part1_Common_Analysis-DATA512.png)

### Visualization Summary:
The rate of change in confirmed daily cases is the black dotted line. Since this is daily data, we observe a lot of variability throughout. However, if you observe the green phase where mask mandate was adopted, you will notice that the rate of change of cases is lower than prior rates until there is a sharp increase of about 14% in new cases. This could perhaps be because of the complacency of people wearing masks while observing the rate of Covid-19 cases going down (go through code markdown statements) and then choosing to remove masks owing to the decreased rate of change.

When the Governor of Tennessee officially lifted the Mask mandate in 2021 (Red phase), Source: [US News Tennessee Mask Mandate Information](https://www.usnews.com/news/best-states/articles/these-are-the-states-with-mask-mandates#tenn), we again observe a sudden sharp increase in new cases. We can associate this steep rise due to relatively less or no usage of masks.

Now, we do observe peaks and troughs in both blue and black lines on other timelines despite having no direct relation with the available mask mandate data. Therefore, we can say that the masking policies may not always have a direct impact on the progression of Covid-19 new cases. It is also very important to consider that people did not show symptoms right away after infection. It may have taken a few days for the testing results to become available especially during the early period of the pandemic in 2020.
