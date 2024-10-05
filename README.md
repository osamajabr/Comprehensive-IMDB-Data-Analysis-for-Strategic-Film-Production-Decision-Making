
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

<br>

### Exploratory Data Analysis (EDA)

#### Statistical Summary

Utilised pandas to generate descriptive statistics to understand central tendencies, dispersion, and shape of the dataset's distribution.
#### Data Visualisation

Visualisations play a crucial role in understanding the underlying distributions and relationships within the dataset. The following types of visualisations were used:

- **Box Plot**:
  - A box plot was created for the 'gross_to_budget' ratio to visually represent the distribution's quartiles and outliers, which helps in understanding the spread and central tendency of this financial metric.


![Example Image](https://github.com/osamajabr/Comprehensive-IMDB-Data-Analysis-for-Strategic-Film-Production-Decision-Making/blob/main/assets/box.png?raw=true)

<br>
<br>

- **Histogram and KDE Plot**:
  - A histogram combined with a Kernel Density Estimate (KDE) was used for the 'gross_to_budget' ratio. This visualisation helps to understand the frequency distribution and the smoothness of the data distribution across the dataset.

![Example Image](https://github.com/osamajabr/Comprehensive-IMDB-Data-Analysis-for-Strategic-Film-Production-Decision-Making/blob/main/assets/kde.png?raw=true)

<br>
<br>

- **Probability-Probability (P-P) Plot**:
  - A P-P plot was generated to compare the cumulative distribution of the 'gross_to_budget' ratio against a theoretically normal distribution, which is useful for assessing normality.

![Example Image](https://github.com/osamajabr/Comprehensive-IMDB-Data-Analysis-for-Strategic-Film-Production-Decision-Making/blob/main/assets/pp.png?raw=true)

<br>
<br>

- **Empirical Cumulative Distribution Function (ECDF)**:
  - An ECDF plot was used to observe how the empirical distribution of 'gross_to_budget' compares to the true cumulative distribution, providing insights into the proportion of data points below each value.

![Example Image](https://github.com/osamajabr/Comprehensive-IMDB-Data-Analysis-for-Strategic-Film-Production-Decision-Making/blob/main/assets/ECDF.png?raw=true)

<br>

#### Hypothesis Testing

- **Bootstrap Hypothesis Testing**:

Bootstrap tests were performed to evaluate the impact of IMDB ratings and movie duration on financial success, specifically looking at the gross-to-budget ratio:

- **IMDB Ratings**: The analysis found significant evidence that movies with an IMDB rating of 7 or higher tend to have a greater average gross-to-budget ratio compared to movies with lower ratings. This indicates that higher IMDB ratings are positively associated with financial returns, suggesting that ratings are an important factor in predicting a movie's financial success.

- **Movie Duration**: Similarly, it was found that movies with longer durations (106 minutes or more) consistently show higher average gross-to-budget ratios than shorter films. This implies that longer movies, which often involve more detailed storytelling and potentially higher production values, are likely to be more financially successful.

These results suggest that both the perceived quality of a movie, reflected in higher IMDB ratings, and its duration are important predictors of financial success.

<br>


#### Advanced Statistical Findings

- **Outlier Management**:
  - Rigorously identified and removed outliers, particularly in financial metrics like the gross-to-budget ratio, to prevent skewed results.
- **Non-parametric Analysis**:
  - Due to the non-normal distribution of data, non-parametric methods such as bootstrapping were used to validate the findings from hypothesis testing.


### Conclusions and Strategic Recommendations


Based on the comprehensive analysis, several strategic recommendations have been formulated to guide the future film productions and optimise financial success:

- **Invest in Proven Genres and Formats**: Prioritise investments in the **Drama** genre, which has historically demonstrated financial success, particularly within the budget constraint of **£1.5 million**. Additionally, focus on producing films that are coloured and predominantly in the English language, attributes that align with the successful characteristics of historically profitable films.


- **Optimal Film Duration and Rating**: Aim to produce the movie to with durations of **106 minutes** or longer, which have shown to be more successful. Also, consider adhering to an **R rating** and an aspect ratio of **1.85**, as these characteristics were common among top-performing films.



- **Specific Recommendations for Director and Actors**:
- 
  - **Primary Recommendation**: Collaborate with the crew that produced **"Urbania"**, particularly director **Jon Shear**, and actors **Dan Futterman**, **Josh Hamilton**, and **Matt Keeslar**. This film exhibited the highest gross-to-budget ratio of **4.564973**, indicating a highly profitable model.
  - **Alternative Recommendation**: If the primary choice is unavailable, consider the team behind **"Half Nelson"**, directed by **Ryan Fleck** with actors **Ryan Gosling**, **Tristan Mack Wilds**, and **Jeff Lima**. This film also showcased a high gross-to-budget ratio and significant audience popularity, as evidenced by a high number of total likes.

These targeted recommendations are designed to utilise historical data and proven success factors to enhance the commercial outcomes of future film projects.

