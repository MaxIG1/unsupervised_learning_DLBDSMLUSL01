
# Unsupervised_Machine_Learning

# Project README

# Clustering Mental Illness in the Tech Industry

## 1. Introduction

Mental illness is a significant and often stigmatized issue affecting millions of individuals worldwide. This project focuses on clustering mental health-related data within the technology industry. Mental health matters as it impacts a substantial portion of the population, with approximately 27.8% of adults in Germany experiencing mental illness each year. The consequences of untreated mental illness can be severe, affecting individuals and society as a whole, including an estimated 10,000 suicides per year in Germany and substantial economic costs.

This study utilizes data from the OSMI (Open Sourcing Mental Health) Mental Health in Tech Survey conducted in 2016. The goal is to apply unsupervised machine learning techniques to identify hidden patterns and clusters within the dataset.

## 2. Description of the Dataset

The dataset comprises responses from tech industry workers regarding their experiences with mental health. It includes 1,433 samples and 63 features. Notably, the dataset lacks strict coding standards, and questions are often not perfectly harmonized, leading to potential correlations between various features. Furthermore, the dataset predominantly represents individuals from the United States, with participants from 53 different countries in total.

Among the participants, there is an imbalance in gender, with a larger number of male respondents. Additionally, 62 of the features are categorical, primarily nominal, while only the "age" feature is on a ratio scale. Some features have a high cardinality or allow free-text input.

## 3. Data Editing
### 3.1. Feature Cleaning and Selection

Several features required cleaning and processing, including "sex" and "age," which were transformed into more manageable categories. Features like "work_position" and "diagnosis" were processed using a bag-of-words algorithm to make them suitable for unsupervised machine learning.

Features were also evaluated for removal based on criteria such as high cardinality and the results of chi-square tests. Certain features were dropped or combined, resulting in a refined dataset.

### 3.2. Dataset Preparation

Various datasets were created for clustering, with some containing imputed missing values and others without. Different approaches were explored to understand how dataset preparation impacted clustering results.

## 4. Distance Measurement and Encoding

Given the categorical nature of most features, two options were considered for distance measurement: Gower distance and one-hot encoding. Gower distance was used to account for mixed data types. The choice of encoding depended on the clustering technique applied.

## 5. Clustering and More Feature Selection

Three distinct clustering approaches were used:

DBSCAN with Gower Distance: Density-Based Spatial Clustering of Applications with Noise (DBSCAN) was employed to identify clusters within the dataset.
Agglomerative Clustering with Gower Distance: Hierarchical agglomerative clustering was used with various linkage functions and cluster counts.
DBSCAN with One-Hot-Encoded Data after PCA: DBSCAN was applied to datasets that underwent one-hot encoding and principal component analysis (PCA) to reduce dimensionality.

# 6. Presentation of Clustering Results
## 6.1. Results of Dataset Preparations
Different dataset preparations were evaluated, with "all_countries" and its one-hot-encoded sub-forms showing the most promising results for clustering. Removing participants from rarer states did not significantly impact clustering outcomes.

## 6.2. Results of Clustering
All three clustering approaches consistently revealed clusters around mental health. Participants with mental illnesses tended to cluster together, as did those without mental disorders. Additionally, some clusters included individuals with ambiguous responses regarding their mental health.

# 7. Concluding Remarks
This case study explored the clustering of mental health-related data within the tech industry. It highlighted the importance of proper data preprocessing and the choice of distance measurement for successful clustering. The results revealed that individuals with mental illnesses tended to cluster together, but the dataset's lack of representativeness limits the generalizability of these findings.

Future analyses could include hypothesis-driven t-tests, feature importance analysis, and further investigations into the impact of variables such as location and healthcare systems on mental health in the tech industry. Ultimately, this work underscores the significance of addressing mental health without stigma, as it affects a diverse range of individuals within the tech sector.
