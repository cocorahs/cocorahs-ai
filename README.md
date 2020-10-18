# CoCoRaHS AI for Earth

[CoCoRaHS](https://www.cocorahs.org/) – Community Collaborative Rain, Hail & Snow Network is a network of volunteer weather observers in the United States, Canada, and the Bahamas that take daily readings of precipitation and report them to a central data store over the internet. This repository hosts resources developed as part of the CoCoRaHS AI for Earth project. The objective of the project is to leverage data science and machine learning techniques to support the key goals that include, (1) Extract insights from observation notes, (2) Use Notebooks to share data analysis, and (3) Improve QC processes.

## cocorahs-ai_book1 - Intro to Topic Modeling

The goal here is to do exploratory data analysis (EDA) on the observation notes data available in the CoCoRaHS data source. For this analysis we looked at the DailyPrecipReport that has around **46.5 million** records, out of which around **8 million** records have observation notes. This study takes a random 1% sample from the 8 million records (**91,937** records with notes) to perform the initial EDA.

Since we are dealing with large amount of unstructured and unlabeled data, the EDA is going to leverage two key unsupervised machine learning algorithms that are suitable for text analysis. Specifically, we will be looking at two topic modeling algorithms: **Latent Dirichlet Allocation (LDA)** and **K-Means Clustering**. 

This notebook is divided into the following sections:

- Setup – load and review the data from notes
- Breakdown of weather terms in the notes
- Topic Modeling with LDA
- Topic Modeling with K-Means Clustering
- Compare predictions from LDA and K-Means on test data

## cocorahs-ai_book2 - Extracting Hail Size and Duration and Condition Monitoring Observer Notes Topic Analysis

This notebook is contains two parts: (1) Hail size and duration extraction from notes in the daily precipitation reports, and (2) Condition Monitoring report analysis.

The Condition Monitoring report analysis is further broken down into three parts:

1. The condition monitoring report analysis conducts a simple analysis of comparing the reported `Scale Bar` values by observers versus the manual interpretation of the `Scale Bar` values based on observer notes. This can be a basis of training a supervised learning model to flag discrepancies between the reported `Scale Bar` values and the provided notes.

2. Analysis of `Scale Bar` values by `Observation Type`: In this section we look at how the `Scale Bar` values break down by `Observation Types` and vice versa.

3. In last section of the notebook, we look at the Topic Analysis of notes provided in the reports. We also look at the relationships between the provided `Scale Bar` values and the inferred `Topics` form the provided notes.

## cocorahs-ai_book3 - State and County Level Analysis of Dry and Wet Conditions

In this notebook we join the `Condition Monitoring Report` with `Station Information` to develop analysis and visualizations in order to understand extreme weather conditions using time and geography dimensions. Key visualization types include:

- Box and whisker plot
- Heat map
- Customized error plots
- Map at state and county level
