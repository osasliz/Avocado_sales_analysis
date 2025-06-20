# Avocado Sales Analysis

## Project Overview
The goal of this analysis project was to provide insight into the avocado sales performance in various years or seasons. By analysing various aspects of the Avocado data, we seek to identify trends, make data-driven recommendation and acquire more insight on Avocado's sales.

## Data Source
Avocado dataset for this analysis can be found in "Kaggle" [website](https://www.kaggle.com/datasets/neuromusic/avocado-prices) or as "avocado.csv" file.

## Tools
- BigQuery / MySQL - Data Analysis
- Tableau - Creating Reports

## Exploratory Data Analysis
EDA involved exploring the avocado data to answer some key questions based on certain factors like:
- Price and Sales Trends


![avg_price by Date](https://github.com/user-attachments/assets/e1d63584-0fdd-4a01-aa6e-caa61a55669f)


- Product Type Comparison
- Regional Analysis


![total_sales by region](https://github.com/user-attachments/assets/c66f5b1c-e132-4ab6-a773-d0a4e5114dcb)


- Size-Specific Insights
- Temporal Trends
- Correlation and Averages

## Data Analysis

```BigQuery
SELECT 
    year_month,
    AVG(AveragePrice) AS avg_price
FROM (
    SELECT 
        FORMAT_DATE('%Y-%m', Date) AS year_month,
        AveragePrice
    FROM `my-1st-project-454410.Avocado_data.Avocado_price`
)
GROUP BY year_month
ORDER BY year_month;
```

## Results
Result summary include:
- A noticeable change was seen in total sales volume year over year with a drastic sales decrease in the year 2018.
- Conventional avocados had more sales than the organic avocados.
- The average avocado price over time was unstable with inconsistent derived pattern.

## References
1. Kaggle.com
2. Chatgpt.com




