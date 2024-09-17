# Serve Analysis and Player Success in Professional Tennis

## Project Overview

This project explores the relationship between serve proficiency and professional tennis success. The goal is to identify how serve statistics (e.g., first serve percentage, aces, double faults) relate to a player’s win percentage and world ranking. By clustering players based on serve statistics, we can better understand the impact of serving ability on overall performance.

## Data

The data for this project comes from Jeff Sackmann's `tennis_atp` dataset on GitHub. It includes match-level statistics from 2010-2023. Key data includes:

- Player serve statistics (first serve percentage, aces, double faults, etc.)
- Player rankings and win percentages
- Player height and hand dominance

## Key Features

- **Serve Rating**: A composite score designed to quantify a player’s overall serve proficiency. The serve rating is calculated using several serve-related variables:

    ```python
    serve_rating = first_serve_percentage + first_serve_won_percentage + second_serve_won_percentage + avg_ace - avg_df + avg_bp_saved - avg_bp_faced
    ```

- **Player Clusters**: Players are grouped into clusters based on their serve statistics using the K-Means algorithm. The optimal number of clusters is determined using the elbow method and silhouette analysis.

- **Feature Engineering**: Variables like height, career-high rank, and match win percentage are used to enhance the analysis and clustering.

## Methods

### Data Preprocessing
Data from 2010-2023 was cleaned and prepared, focusing on players with at least 10 matches played. Serve-related statistics were aggregated for each player.

### Exploratory Data Analysis
Correlation analysis was performed to find relationships between serve statistics and win percentage. The data was visualized to better understand these correlations.

### Clustering
The K-Means algorithm was used to cluster players based on their serve performance. This helped identify groups of players with similar serve styles and success rates.

### Cluster Analysis
Each cluster was analyzed to identify patterns in serving style, success rate, and ranking.

## Results

- Serve proficiency, particularly first serve win percentage and serve rating, has a significant positive correlation with win percentage.
- Clustering revealed several types of servers, including an elite group with dominant serve statistics.
- Players with higher serve ratings tended to have higher win percentages, although variability in success indicates that other factors (e.g., return game, mental toughness) also contribute to overall performance.

## Conclusion

This analysis confirms that serving is a critical component of success in professional tennis. By clustering players based on serve statistics, we can identify different playing styles and determine which serve characteristics correlate most with winning matches.
