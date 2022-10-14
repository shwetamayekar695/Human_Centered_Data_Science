[![MIT License](https://img.shields.io/apm/l/atomic-design-ui.svg?)](https://github.com/shwetamayekar695/Human_Centered_Data_Science/blob/main/LICENSE)

# Homework 2 - DATA 512 - Considering Bias in Data

Goal of the Project: The goal of this assignment is to explore the concept of bias in data using Wikipedia articles of political figures from different countries. For this assignment, we combine a dataset of Wikipedia articles with a dataset of populations by country and region to use a machine learning service called ORES to estimate the quality of each article.


Data Source:
[Wikipedia Politicians by nationality (Category)](https://en.wikipedia.org/wiki/Category:Politicians_by_nationality)
[Wikipedia world population data sheet](https://www.prb.org/international/indicator/population/table)

## Licenses

Wikimedia Foundation REST API terms of use: [Wikimedia Terms & Conditions](https://www.mediawiki.org/wiki/Wikimedia_REST_API#Terms_and_conditions)


### Repository Structure

```bash
└── data-512-homework_2
    ├── README.md
    ├── data
    │   ├── politicians_by_country_SEPT.2022.csv
    │   ├── population_by_country_2022.csv
    ├── output
    │   ├── wp_countries-no_match.txt
    │   ├── wp_politicians_by_country.csv
    └── src
        └── Data_Preparation_and_Analysis_Results.ipynb
```

### Data Inconsistencies

1) Politician csv data consisted of 50 duplicated names. This was taken care of by dropping all duplicates in the final dataframe wp_politicians_by_country.csv
2) Country name "Korean" present in politician data did not have any matches with population data. Therefore, its corresponding Region name and population remained empty. These rows were also dropped. 


### Input Data Files

1) List of Wikipedia article pages about politicians from a wide range of countries: data/politicians_by_country_SEPT.2022.csv
2) Population data by regions and countries: data/population_by_country_2022.csv

### Output Data Files

- wp_countries-no_match.txt
- wp_politicians_by_country.csv

**RESULTS FROM ANALYSIS **

1) 


