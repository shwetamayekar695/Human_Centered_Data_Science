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

1) List of all countries for which there are no matches: wp_countries-no_match.txt
2) Final dataframe: wp_politicians_by_country.csv


### Results from analysis
Results are in tabular form in the python notebook found here: src/Data_Preparation_and_Analysis_Results.ipynb

1) Top 10 countries by coverage
2) Bottom 10 countries by coverage
3) Top 10 countries by high quality
4) Bottom 10 countries by high quality
5) Geographic regions by total coverage
6) Geographic regions by high quality coverage


### Research Implications

This project helped me source data from wikipedia articles and analyse their quality using the ORES machine learning model.

An interesting observation was that the final dataset did not contain United States of America neither the region Northern America. On further analysis I found that the article list doesn't contain articles from nations of the likes of Canada, United Kingdom, Australia, and many more. I assumed that data from these nations would also be a part of the dataset before conducting the analysis.

Because of the lack of information on many countries, especially the entire of Northern America, performing a realistic data science research where using this data (to train a model, perform a hypothesis-driven research, or make business decisions) might create biased or misleading results.

However, the metric High-quality-articles-per-population (a ratio representing the number of high quality articles per population) seems like a good measure to analyse the goodness of the articles per country/region. Higher the ratio, higher the quality of articles generated from that country. One would assume that non-native English speaking countries would have lower quality articles, but that is not always the case. Countries such as Andorra, Slovenia, Lithuania, and many more come under top 10 countries with High-quality-articles-per-population.

Speaking about population, India and China show highest densities in population so one would expect the ratio_of_articles_per_population_countrywise ratio to be synonymous with the high density in population. But neither of the 2 countries fall under the top 10 countries with the highest total articles per capita.

#### Q&A on Analysis:
1) What biases did you expect to find in the data (before you started working with it), and why?
I assumed that English speaking developed countries would show the highest ratios in High-quality-articles-per-population. However, that was not the case. In fact, Northern America was not even a part of the final dataset due to lack of its presence from the articles list.

2) What (potential) sources of bias did you discover in the course of your data processing and analysis?
The number of articles from Southern, Eastern and Western Europe are 876, 725 and 697 respectively. The data shows bias in having high number of articles from politions of the former 3 regions. The Wikipedia articles show a particular high bias towards European regions.

3) Can you think of a realistic data science research situation where using these data (to train a model, perform a hypothesis-driven research, or make business decisions) might still be appropriate and useful, despite its inherent limitations and biases?
As mentioned above, the metric High-quality-articles-per-population (a ratio representing the number of high quality articles per population) seems like a good measure to analyse the goodness of the articles per country/region. Perhaps it can also be used to conduct data science research situation to perform a hypothesis-driven research for select countries with available data.
Higher the ratio, higher the quality of articles generated from that country. One would assume that non-native English speaking countries would have lower quality articles, but that is not always the case. Countries such as Andorra, Slovenia, Lithuania, and many more come under top 10 countries with High-quality-articles-per-population.


