[![MIT License](https://img.shields.io/apm/l/atomic-design-ui.svg?)](https://github.com/shwetamayekar695/Human_Centered_Data_Science/blob/main/LICENSE)

# Homework 1 - DATA 512 - Professionalism & Reproducibility

Goal of the Project: To construct, analyze, and publish a dataset of monthly article traffic for a select set of pages from English Wikipedia from January 1, 2015 through September 30, 2022.


Data Source: [Wikipedia REST API Endpoint](https://wikimedia.org/api/rest_v1/#/Pageviews%20data/get_metrics_pageviews_per_article__project___access___agent___article___granularity___start___end_), licensed under the [CC-BY-SA 3.0]( CC-BY-SA 3.0 and GFDL licenses) and [GFDL licenses]( CC-BY-SA 3.0 and GFDL licenses).

Data Documentation: [Pageviews API Documentation](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews)

Terms of Use: [Wikimedia Foundation REST API terms of use](https://www.mediawiki.org/wiki/REST_API#Terms_and_conditions)


### Repository Structure

```bash
└── data-512-homework_1
    ├── README.md
    ├── data
    │   ├── dino_monthly_cumulative_201507-202209.json
    │   ├── dino_monthly_desktop_201507-202209.json
    │   ├── dino_monthly_mobile_201507-202209.json
    │   ├── dinosaur_genera.cleaned.SEPT.2022.csv
    │   └── pageview_download.json.zip
    ├── results
    │   ├── plot_for_averages.png
    │   ├── plot_for_fewest_months_of_data.png
    │   └── plot_for_top_10_peak_views.png
    └── src
        ├── Analysis_Code.ipynb
        └── Data_Preparation.ipynb
```

Please Note: *pageview_download.json.zip* is a compressed file. Original file has a large size (63MB) and is in .json format.

### Library installation required
 - tqdm

### Input Data Files
List of Dinosaur Articles: data/dinosaur_genera.cleaned.SEPT.2022.csv

### Output Data Files
**JSON Files**
- data/dino_monthly_cumulative_201507-202209.json
- data/dino_monthly_mobile_201507-202209.json
- data/dino_monthly_desktop_201507-202209.json

**PLOTS (.png files)**

- plot_for_averages.png shows Maximum Average and Minimum Average Plot
![plot_for_averages](https://github.com/shwetamayekar695/Human_Centered_Data_Science/blob/main/HW1-DATA512/results/plot_for_averages.png)

- plot_for_top_10_peak_views.png shows Top 10 Peak Page Views Plot
![plot_for_top_10_peak_views](https://github.com/shwetamayekar695/Human_Centered_Data_Science/blob/main/HW1-DATA512/results/plot_for_top_10_peak_views.png)

- plot_for_fewest_months_of_data.png shows Fewest Months of Data Plot
![plot_for_fewest_months_of_data](https://github.com/shwetamayekar695/Human_Centered_Data_Science/blob/main/HW1-DATA512/results/plot_for_fewest_months_of_data.png)
