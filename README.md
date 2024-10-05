## README: Comprehensive IMDB Data Analysis for Strategic Film Production Decision-Making

### Project Overview

This project was initiated by SussexBudgetProductions to navigate from a substantial box office loss towards a profitable future in film production. In light of a previous film's failure with a budget of £500K grossing only £100K, and with an anticipated budget of £1.5 million for future projects, a detailed data-driven strategy was crucial. The objective was to analyse historical IMDB data to derive actionable insights that could ensure the success of subsequent productions.

### Dataset Description

The dataset is a comprehensive collection of data extracted from IMDB, encompassing a variety of movie-related information:

- **General Information:** Movie titles, release years, and color information.
- **Financial Data:** Budget and gross earnings of movies in GBP.
- **Performance Metrics:** IMDB scores, number of reviews, Facebook likes for movies and cast members.
- **Content Characteristics:** Genres, plot keywords, languages, countries, content ratings.
- **Personnel Details:** Director and actor information, including their popularity on social media.

### Technical Setup and Installation

The analysis requires the following Python libraries:
- **pandas**: for data manipulation.
- **matplotlib** and **seaborn**: for plotting and visualization.
- **numpy** and **scipy**: for numerical and statistical analysis functions.
- **statsmodels**: for more advanced statistical analysis such as probability plots, ECDF, and hypothesis testing.
- **scipy.stats**: specifically used for its functions like `norm` for normal distributions, and `normaltest` to test for the normality of the distribution.


### Detailed Analysis Workflow

#### Data Preparation and Cleaning

- **Loading Data**: Data was loaded using pandas.
- **Initial Cleaning**:
  - Removed rows containing missing values, reducing the dataset size by 1287 rows.
  - Columns were reordered for improved clarity and focus on relevant information.
  - Renamed `title_year` to `release_date` to better reflect the data's content.
- **De-duplication**:
  - Removed duplicate movie titles to ensure data uniqueness.
  - After removing duplicates, 101 movie titles were eliminated, leaving 3655 unique entries for analysis.

### Exploratory Data Analysis (EDA)

#### Statistical Summary

Utilised pandas to generate descriptive statistics to understand central tendencies, dispersion, and shape of the dataset's distribution.
#### Data Visualisation

Visualisations play a crucial role in understanding the underlying distributions and relationships within the dataset. The following types of visualisations were used:

- **Box Plot**:
  - A box plot was created for the 'gross_to_budget' ratio to visually represent the distribution's quartiles and outliers, which helps in understanding the spread and central tendency of this financial metric.


![Example Image]((https://github.com/osamajabr/Comprehensive-IMDB-Data-Analysis-for-Strategic-Film-Production-Decision-Making/blob/8fd7e6004e683d3432960c24fb0b9f4326c58c13/assets/box.png))

- **Histogram and KDE Plot**:
  - A histogram combined with a Kernel Density Estimate (KDE) was used for the 'gross_to_budget' ratio. This visualisation helps to understand the frequency distribution and the smoothness of the data distribution across the dataset.

- **Probability-Probability (P-P) Plot**:
  - A P-P plot was generated to compare the cumulative distribution of the 'gross_to_budget' ratio against a theoretically normal distribution, which is useful for assessing normality.

- **Empirical Cumulative Distribution Function (ECDF)**:
  - An ECDF plot was used to observe how the empirical distribution of 'gross_to_budget' compares to the true cumulative distribution, providing insights into the proportion of data points below each value.

These visualisations were instrumental in identifying key trends, distributions, and potential anomalies within the variables such as 'gross_to_budget', enhancing the analytical depth and aiding in decision-making processes related to film production investments.

#### Statistical Analysis and Hypothesis Testing

- **Correlation Analysis**: 
  - Investigated the relationships between movie budgets, gross earnings, and IMDB ratings. Found significant correlations between budget and gross earnings, but weaker correlations between IMDB ratings and financial success.
- **Bootstrap Hypothesis Testing**:
  - Implemented bootstrap tests to assess the impact of IMDB ratings on financial success. The results indicated no strong evidence that higher IMDB ratings are associated with higher financial returns. This suggests that other factors, perhaps genre or star power, might be more influential in determining a movie's financial success.

#### Actionable Insights and Recommendations

- **Genre and Budget Analysis**:
  - Identified genres with higher average returns, recommending a focus on Action and Comedy for future productions.
  - Suggested optimal budget ranges based on historical data to maximize returns without the heightened risks associated with very high-budget films.
- **Star Power**:
  - Highlighted the importance of casting popular actors. The presence of well-known actors was strongly correlated with higher gross earnings, suggesting their significance in attracting larger audiences.

#### Advanced Statistical Findings

- **Outlier Management**:
  - Rigorously identified and removed outliers, particularly in financial metrics like the gross-to-budget ratio, to prevent skewed results.
- **Non-parametric Analysis**:
  - Due to the non-normal distribution of data, non-parametric methods such as bootstrapping were used to validate the findings from hypothesis testing.

### Conclusions and Strategic Recommendations

Based on the comprehensive analysis, strategic recommendations were formulated to guide future film productions:
- **Invest in Profitable Genres**: Focusing investments on genres like Action and Comedy which have historically shown financial success.
- **Efficient Budgeting**: Advocating for mid-range budgets that have demonstrated the best return on investment ratios.
- **Utilization of Star Power**: Emphasizing the need to cast well-known actors to enhance marketability and audience draw.

#### Further Insights and Recommendations

The analysis also highlighted the complex interplay between various factors such as genre, budget size, and cast popularity, which should be considered in future production decisions.

### Contribution and Collaboration

For additional insights, contributions, or discussions on the methodologies used in this analysis, stakeholders and external reviewers are encouraged to contact the data science team at SussexBudgetProductions or participate in discussions through the project's GitHub repository.

