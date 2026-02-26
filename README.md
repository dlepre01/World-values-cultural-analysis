# World Values Survey – Cultural Clustering Analysis

## Overview

This project explores global cultural patterns using data from the World Values Survey (Wave 7, 2017–2022), covering 63 countries and ~90,000 respondents after cleaning.

The goal is to identify culturally homogeneous country clusters and analyze how cultural values correlate with socioeconomic and political indicators such as GDP per capita and regime type.



## Objectives

- Construct composite cultural indices from survey variables
- Perform hierarchical clustering on country-level aggregates
- Compare clustering techniques (Agglomerative vs K-Means)
- Evaluate clustering quality using Silhouette analysis
- Analyze relationships between cultural values and:
  - GDP per capita
  - Political regime type
  - Education levels
  - Family structure


## Methodology

### Feature Engineering

Eight cultural indices were constructed (values in [0,1]):

- Defiance  
- Disbelief  
- Relativism  
- Scepticism  
- Autonomy  
- Equality  
- Choice  
- Voice  

Indices were computed by aggregating standardized survey questions.

Additional features integrated:
- GDP per capita (World Bank)
- Regime type (Economist Democracy Index)
- Population data
- Education level
- Religion denomination


### Data Processing

- Original dataset: 97,220 rows × 613 columns
- Cleaned dataset: 89,940 rows
- Aggregation at country level
- Removal of missing values (~7.5%)

### Clustering Techniques

####  Hierarchical Clustering (Primary Model)
- Agglomerative clustering
- Ward linkage
- Dendrogram visualization
- 7–9 clusters evaluated

#### Dimensionality Reduction
- Multidimensional Scaling (MDS)
- Self-Organizing Map (SOM) in R

#### Comparison Model
- K-Means clustering
- UMAP for dimensionality reduction
- Silhouette score evaluation

Optimal K-Means clusters: **7**

## Key Findings

- Clear cultural macro-clusters emerge globally.
- GDP per capita strongly correlates with:
  - Choice (0.74)
  - Equality (0.67)
  - Disbelief (0.64)
- Wealthier democracies tend to show:
  - Higher gender equality
  - Greater support for civil liberties
  - Lower religious adherence

Authoritarian regimes show:
- Higher respect for authority
- Lower support for individual freedoms
- Stronger religious influence



## Tech Stack

- Python (scikit-learn, umap-learn, matplotlib, seaborn)
- R (kohonen package for SOM)
- pandas / numpy
- Hierarchical clustering (Ward linkage)
- Silhouette score evaluation

## Why This Project Matters

This project combines:

- Feature engineering
- Unsupervised learning
- Cross-method validation
- Statistical interpretation
- Socioeconomic analysis

It demonstrates the ability to translate raw survey data into interpretable macro-patterns using rigorous data science methodology.



## Authors

Daniele Lepre  
Alice Anna Maria Brunazzi
Alessandro Della Beffa
Sofia Turroni
University of Milano-Bicocca  
Data Science Lab – 2023/2024
