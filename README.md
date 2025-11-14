# Music Features Analysis Project

## Project Overview

This repository features an Extract, Transform and Load (ETL) pipeline with descriptive and visual analytics for a large music .csv dataset featuring music metadata from [Kaggle](https://www.kaggle.com/datasets/saurabhshahane/music-dataset-1950-to-2019) and [Mendeley Data](https://data.mendeley.com/datasets/3t9vbwxgr5/2). The project used Python with Visual Studio for extraction, transformation, loading, and data visualisations. The goal was to explore how music features change and trend over time, in particular loudness.
Originally, this project was supposed to use the Spotify developer API and Million Song Database, but for the sake of a smaller and manageable dataset a local .csv of the mentioned sources was used instead.

## Objectives

- Design and implement a reproducible Python ETL pipeline.
- Create static and interactive visualisations with Matplotlib, Seaborn, and Plotly.
- Present key findings about song features and music quality trends.
- Maintain clear documentation for ongoing development and reproducibility.

## Hypothesis
The hypothesis of the project is that loudness has increased over time. It's known in the audio engineering world that there has been a "loudness war" increasing over the past few decades. This analytical project would be able to visualise this purported trend.

## Dataset

- Source: .csv file of music features from Kaggle and Mendeley Data with around 28,000 tracks.
- Columns with both strings and integers include: artist, track, release date, genre, lyrics, loudness, energy, danceability.
- Rows with missing values in important columns are dropped as part of dartaset cleansing.

## ETL Pipeline

**Extract:**  
Load dataset from a local .csv file using Pandas.

**Transform:**  
Checked and convert data types column by column.
Clean data by dropping and removing incomplete entries into a cleaned dataset.  
Make a "decade" column using the release year column.  
Generated basic descriptive statistics and visual analytics.

**Load:**  
Save the cleaned DataFrame as `cleanedmusicdata.csv` for analysis.

## Data Analysis and Visualisation

### Descriptive Statistics

Calculate mean, median, count by year and decade for features like loudness and energy

### Visualisations

- Line plot: Average loudness by decade
![Plot 1](visualisations/Average%20Loudness%20by%20Decade.png)

- Bar plot: Number of tracks released per decade
![Plot 2](visualisations/Number%20of%20Tracks%20per%20Decade.png)

- Scatter plot: Energy vs Loudness by Decade
![Plot 3](visualisations/Energy%20vs%20Loudness%20by%20Decade.png)

- Correlation heatmap for audio features
![Plot 4](visualisations/Music%20Feature%20Correlation%20Heatmap.png)

- Interactive Plotly charts for feature relationships
![Plot 5](visualisations/Loudness%20vs%20Energy%20Static%20Image.png)
![Plot 6](visualisations/Loudness%20Distribution%20by%20Decade%20Static%20Image.png)


## Key Findings

- Average loudness of music has trended upwards since 1950, peaking more recently
- Strong correlation found between loudness and energy, varying across decades
- The number of music releases increases significantly from the 1950s to the 2010s
- Relationships identified between several music features

## How to Use

1. Clone or download this repository
2. Download the dataset to the `data/` directory
3. Open and run the Jupyter Notebook to reproduce ETL and analysis steps

## Challenges and Solutions

- Large dataset handled with memory-efficient loading and cleaning
- Missing values dropped to improve data integrity
- Custom categorical features (such as decade) created
- Used advanced visualisation tools for clear communication of results

## Reflections and Next Steps

- Additional features and lyric sentiment analysis could further enrich findings
- Potential development of a dashboard for interactive exploration
- Extension to predictive modeling and deeper feature engineering

## Attribution

- Source dataset: [Kaggle](https://www.kaggle.com/datasets/saurabhshahane/music-dataset-1950-to-2019) and [Mendeley Data](https://data.mendeley.com/datasets/3t9vbwxgr5/2)
- All external code is properly attributed per license requirements
