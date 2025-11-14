# Music Features Analysis Project

## Project Overview

This repository presents an ETL pipeline and descriptive analytics for a large music dataset. The project applies Python for extraction, transformation, loading, and data visualisations, with the goal of revealing trends in music features over time.

## Objectives

- Design and implement a reproducible Python ETL pipeline.
- Create static and interactive visualisations with Matplotlib, Seaborn, and Plotly.
- Present key findings about audio features and music release trends.
- Maintain clear documentation for ongoing development and reproducibility.

## Dataset

- Source: .csv file of music features from Kaggle and Mendeley Data (over 28,000 tracks)
- Columns include: artist, track, release date, genre, lyrics, loudness, energy, danceability, and more
- Rows with missing values in important columns are dropped as part of preprocessing

## ETL Pipeline

**Extract:**  
Load dataset from local CSV file using Pandas

**Transform:**  
Check and convert data types  
Clean data by removing incomplete entries  
Add decade feature derived from release year  
Generate basic statistics and analytics

**Load:**  
Save the cleaned DataFrame as `cleanedmusicdata.csv` for analysis

## Data Analysis and Visualisation

### Descriptive Statistics

Calculate mean, median, count by year and decade for features like loudness and energy

### Visualisations

- Line plot: Average loudness by decade
- Bar plot: Number of tracks released per decade
- Scatter plot: Tempo vs loudness (colour-coded by decade)
- Correlation heatmap for audio features
- Interactive Plotly charts for feature relationships

## Key Findings

- Average loudness of music has trended upwards since 1950, peaking more recently
- Strong correlation found between loudness and energy, varying across decades
- The number of music releases increases significantly from the 1950s to the 2010s
- Relationships identified between several music features

## Code Organisation

- Well-commented Jupyter Notebook for all code and analysis
- Consistent, descriptive file naming (lowercase, no spaces or capitals)
- Version control via GitHub

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

- Source dataset: [Kaggle](https://www.kaggle.com/)
- All external code is properly attributed per license requirements

## Maintainers

- ETL and Data Cleaning: Data Analyst
- Visualisation: Data Analyst
- Project Management and Documentation: Project Lead
