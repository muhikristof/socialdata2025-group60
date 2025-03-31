---
layout: home
title: Home
---

# Introduction
Crime data analysis involves examining spatial and temporal patterns to identify trends, hotspots, and correlations. To achieve this, data must first be cleaned and organized. When working with multiple datasets, such as crime reports and location-based statistics, merging them is a crucial step. This requires ensuring both CSV files share a common key, such as case numbers or timestamps. If necessary, data types should be standardized, missing values handled, and duplicate records resolved. Once merged, the data can be visualized and analyzed to extract meaningful insights that support informed decision-making.

<!-- TODO change the link -->
See more at [SFPD_DataCombiner.ipynb](SFPD_DataCombiner.ipynb)

# Making the dataframe

the dataset is first filtered to retain only incidents with multiple records, ensuring duplicate reports from officers are correctly handled. The data is then sorted chronologically based on date and time.

To structure the dataset effectively, incidents are grouped by unique incident numbers, consolidating details such as timestamps, locations, crime categories, and district information. This transformation enables a clearer view of recurring incidents and their characteristics.

A specific subset of the data focuses on vehicle-related crimes, particularly cases where a stolen vehicle is later found. Entries with missing geographic coordinates are removed, and location points are reorganized to track movement between the theft and recovery locations. This refined dataset allows for spatial analysis of vehicle theft patterns.

<!-- TODO change the link -->
See more at [Assignment2.ipynb](SFPD_DataCombiner.ipynb)

# Charts
## Polar charts

This visualization explores the directional patterns of vehicle theft by analyzing where stolen cars from each district were later found. Each subplot represents a different district and displays the distribution of movement directions using a polar histogram. The angles correspond to the directions in which stolen vehicles were recovered relative to their theft locations.

By plotting these distributions, we can identify trends in vehicle movement after theft—such as whether stolen cars are typically recovered in specific directions. This analysis can provide insights into crime patterns and potentially inform law enforcement strategies for vehicle theft prevention.

![Polar charts](/assets/images/polars.png)

<!-- ![Alt text](/assets/images/polars.png) -->