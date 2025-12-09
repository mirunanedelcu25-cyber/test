# COURT DYNAMICS

*Team The powerpuff girls*

* Nedelcu Ioana-Miruna 313421- data cleaning  
* Kovaleva Darya 322681  
* Akbota Kablatin 321281

# SECTION 1

## INTRODUCTION

In this project, we investigate how NBA players develop over time and how their roles evolve within different team contexts. Although the [basketball.db](http://basketball.db) dataset contains multiple tables with player and team statistics, our analysis focuses specifically on the player\_regular\_season table, as it provides the most detailed and consistent season performance indicators. This table includes key metrics such as scoring efficiency, assist ratios, defensive contributions and playing time, allowing us to examine how individual performance evolves across multiple seasons.  
Rather than building a predictive model or classifying players, our goal is to design a comprehensive analytical framework that captures performance patterns, identifies anomalies and traces progression trajectories throughout a player’s season. By analyzing how these indicators change over time and how they relate to player responsibilities on the court, we aim to generate interpretable insights that are meaningful for coaches, analysts and scouts. Ultimately, our findings are intended to support data-informed decisions in player development, role assignment and long-term team-building strategies.

# SECTION 2

## METHODS

### Choosing the table

We first explored all 12 tables available in the [basketball.db](http://basketball.db) database by inspecting their structure with PRAGMA table\_info. Among them, the player\_regular\_season table provided the most complete and relevant information for our analysis, including minutes played, points, rebounds, assists and other key performance statistics. Other tables either aggregated data at the career level or contained incomplete or redundant information, so they were not suitable for our goals.

### Data cleaning

To ensure data quality, we applied several cleaning steps:

* Visualized missing values using missigno.bar() and missigno.heatmap()  
* Filled all missing values in numerical columns with 0  
* Removed rows containing logically impossible values, such as:  
  * fgm\> fga (field goals made\> field goals attempted)  
  * ftm\> fta  (free throws made\> free throws attempted)  
  * tpm\> tpa (three-point made \> three-point attempted)  
  * reb \< oreb \+ dreb (total rebounds\< offensive \+ defensive rebounds)

### Data validation

We performed additional checks to confirm the consistency of the dataset:

* No years earlier than 1946 or later than 2025  
* No duplicated rows  
* No negative values in any numerical feature

These steps ensured that the dataset was coherent and ready for further analysis.

## Environment

Regarding the environment, we used a version of Python3 and we worked on colab.  
The libraries that we used are: sqlite3, pandas, missingno, seaborn, matplotlib.pyplot. 

# SECTION 3

### Purpose

The goal of the cleaning process was to obtain a reliable dataset that accurately reflects player performance and can support meaningful exploratory data analysis and modeling.

### Baseline

We explained the distribution of points per game (PPG) after cleaning to understand the overall shape of the data and identify potential outliers. This served as a baseline for evaluating the quality of the cleaned dataset.

### Evaluation Metrics

We used several visual tools to assess the dataset:

* Histogram to inspect the distribution of PPG  
* Boxplots to detect outliers  
* A correlation heatmap to understand relationships between features

These visual metrics helped us evaluate whether the cleaned data behaved as expected.




