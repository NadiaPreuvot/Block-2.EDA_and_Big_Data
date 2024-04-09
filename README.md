# Block-2.EDA_and_Big_Data

## NOTE POUR LE JURY : J'ai créé un autre repository pour l'EDA, voici le lien pour y avoir accés
https://github.com/NadiaPreuvot/Block.2.EDA-Speed.Dating-Tinder_Project

# Steam Games Analysis with PySpark in Databricks

This README summarizes a comprehensive analysis of video games available on Steam, focusing on various aspects like the distribution of games across genres, their availability on different operating systems (Windows, Mac, Linux), and identifying the most popular and lucrative genres. The analysis is performed using PySpark within the Databricks environment.

You can find the link of the notebook : https://community.cloud.databricks.com/?o=2029342077115939#notebook/2807590592639607/command/3575907893182817

## Dataset

The dataset used for this analysis is stored in a JSON format and includes information about games such as name, developer, publisher, genres, platforms, price, and the number of positive reviews.

## Objectives

- Analyze the distribution of games by publisher and genre.
- Determine the availability of games across different operating systems (Windows, Mac, Linux).
- Identify the most popular and lucrative genres.
- Explore the relationship between game genres and their platform availability.

## Analysis Overview

### Setting Up the Environment

1. Import necessary PySpark libraries:
    ```python
    from pyspark.sql import functions as F
    from pyspark.sql.functions import col, explode, split, sum as _sum
    ```

2. Load the dataset:
    ```python
    filepath = "path/to/steam_game_output.json"
    steam_df = spark.read.json(filepath)
    ```

### Analysis 1: Game Distribution by Publisher and Genre

- Group games by publisher to find out which publisher has released the most games.
- Explore the genres to see which are the most represented and which genres are most popular based on positive reviews.

### Analysis 2: Platform Availability

- Analyze the distribution of games across Windows, Mac, and Linux.
- Calculate the percentage of games available on each platform to understand platform preferences.

### Analysis 3: Most Lucrative Genres

- Estimate the potential revenue by genre, using the price of games as a proxy for their market value.
- Identify genres with the highest average price as an indicator of their lucrative potential.

### Analysis 4: Platform Preference by Genre

- Determine if certain genres are preferentially available on certain platforms, indicating a potential platform-genre affinity.

## Key Findings

- **Publisher Analysis**: [Summarize key findings about game distribution by publisher.]
- **Genre Analysis**: [Summarize findings on the most represented and popular genres.]
- **Platform Availability**: [Highlight the distribution of games across OS platforms.]
- **Lucrative Genres**: [Discuss which genres are potentially the most lucrative.]
- **Platform Preference by Genre**: [Present insights into platform preferences for certain genres.]

## Conclusion

This analysis provided valuable insights into the Steam video game ecosystem, revealing trends in game distribution by publishers and genres, platform availability, and the economic potential of different game genres. These findings can inform stakeholders in the video game industry, from developers to marketers, about current trends and potential areas of focus.
