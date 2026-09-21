# Olympic Swimming Data Analysis

Academic data analysis project completed as part of the Master's program in Mathematics and Applications at Sorbonne University.

## Project overview

This project analyzes Olympic swimming performances between 1912 and 2020.

The dataset contains information such as:
- Olympic year
- Event
- Gender
- Country
- Rank
- Medals
- Performance time

The main objective is to study:

> How have Olympic swimming performances evolved over time, and what national profiles can be identified from historical results?

The analysis is structured around three main dimensions:
1. Evolution of swimming performances over time
2. Identification of country profiles using multivariate analysis and clustering
3. Projection of future performances using linear regression

## Data preparation

The first step consists in cleaning and standardizing the dataset.

In particular:
- swimming times were stored in multiple formats and were converted into seconds
- invalid results such as withdrawals, disqualifications and non-starts were removed
- historical country codes were harmonized in order to avoid artificial fragmentation of the same nation

A custom Python function was implemented to convert all performance times into a common format.

## Exploratory data analysis

The project studies the long-term evolution of swimming performances for several representative Olympic events, including:

- 100m Freestyle
- 100m Backstroke
- 200m Butterfly
- 200m Breaststroke
- 400m Freestyle

The analysis shows a clear decrease in average swimming times over the long term, suggesting a general improvement in Olympic performance.

The relative performance gap between men and women is also analyzed across events.

## Country profile analysis

To compare national swimming profiles, several indicators were aggregated at country level:

- Number of participations
- Number of medals
- Average rank
- Number of Olympic years represented
- Number of events
- Medal rate
- Gold medal rate
- Medals per year

Because several of these variables are strongly correlated, Principal Component Analysis (PCA) is used to summarize the information and visualize the structure of the countries.

## Clustering

Two clustering approaches are applied:

- Hierarchical Agglomerative Clustering
- K-means

The number of clusters is selected using:
- the elbow method
- the silhouette score
- interpretation of the dendrogram

The analysis identifies four main country profiles:

1. United States as a highly dominant outlier
2. Major historical swimming nations
3. Countries with intermediate or modest performance
4. Countries with lower participation but relatively high efficiency

The hierarchical clustering and K-means results are highly consistent.

## Performance forecasting

Linear regression models are used to project future average swimming performances.

Two models are compared:
- regression using the full historical period
- regression using only recent data from 1980 onward

The recent-period model provides more conservative projections and better reflects the slowdown in performance improvements observed in recent decades.

The projections are also compared with observed Olympic performances in 2024 as a consistency check.

## Main findings

- Olympic swimming performances have improved strongly over the long term
- Performance improvements appear to slow down in recent decades
- Country performance cannot be summarized only by total medal count
- PCA and clustering reveal distinct national performance profiles
- The United States appears as a clear outlier in Olympic swimming history
- Recent-period regression gives more realistic projections than a model fitted on the full historical period

## Methods

- Data cleaning and preprocessing
- Exploratory Data Analysis
- Data visualization
- Principal Component Analysis (PCA)
- Hierarchical clustering
- K-means clustering
- Elbow method
- Silhouette score
- Linear regression

## Tools

- Python
- pandas
- NumPy
- scikit-learn
- matplotlib
- seaborn
- Jupyter Notebook

## Repository structure

```text
olympic-swimming-data-analysis/
├── olympic_swimming_analysis.ipynb
├── report_olympic_swimming_analysis.pdf
└── README.md
