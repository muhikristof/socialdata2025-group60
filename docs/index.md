---
layout: home
title: Home
---

- Bence Gattyán, s204773
- João Diogo Silva Oliveira, s250263
- Kristóf Muhi, s240194

# Introduction

If my car is stolen in San Francisco, where should I look for it?

> A look into crime statistics in Vehicle Theft from San Francisco

Having your vehicle stolen can be devistating and you may feel at a loss and have no idea where to look for it.
Luckily there some patterns can be seen on what might happen to it that could help you and the police find it.

We are using data provided by the San Francisco Police department available at [https://datasf.org/opendata/](https://datasf.org/opendata/)

On the websites you can find two datasets, one spanning the years 2003-2018 and one from 2018-present. See more at [SFPD_DataCombiner.ipynb](https://github.com/muhikristof/socialdata2025-group60/blob/main/assignment_2/SFPD_DataCombiner.ipynb) <!-- TODO change the link -->


In these information about crimes committed is available, such as the time and date they occured, the location and police district, type of crime and an incident ID.

Incident ID's are used for submitting reports of crimes that have a connection to eachother, for example, if someone breaks into a house and steals something they get two reports submitted in the dataset, one about the breaking in and one about the theft itself.

Another way Incident ID can connect reports is by linking them two from different time and place to the same crime, for example a car being stolen and later being found elsewhere.

In this data story, we were interested in looking into what patterns emerge when we focus on reports relating to cars being stolen and found elsewhere later.

# Making the dataframe

The dataset is first filtered to retain only incidents with multiple records, ensuring duplicate reports from officers are correctly handled. The data is then sorted chronologically based on date and time.

To structure the dataset effectively, incidents are grouped by unique incident numbers, consolidating details such as timestamps, locations, crime categories, and district information. This transformation enables a clearer view of recurring incidents and their characteristics.

A specific subset of the data focuses on vehicle-related crimes, particularly cases where a stolen vehicle is later found. Entries with missing geographic coordinates are removed, and location points are reorganized to track movement between the theft and recovery locations. This refined dataset allows for spatial analysis of vehicle theft patterns.

<!-- TODO change the link -->
See more at [Assignment2.ipynb](https://github.com/muhikristof/socialdata2025-group60/blob/main/assignment_2/Assignment2.ipynb)

# Charts
## Heatmaps

San Francisco is broken up into 10 police districts governing how police officers get deployed and from what police center.

Below you can see a heatmap visualizing where stolen cars end up depending on the location they were stolen from:

![Heatmaps](/assets/images/heatmaps.png)

The police district is enclosed by a blue line and the amount of cars is illustrated by colour, increasing from the minimum blue -> green -> yellow -> red to the maximum.

From this we can find two patterns.

1. Stolen cars are more often found near their original location of theft rather then far away.
2. Cars are more likely to be found on the east side of the city and the city center.

A possible explanation to this could be that the cars that have been found were only stolen for short term use and not for resale or salvaging for parts.

The eastern side of the city and especially downtown are more scenic that the west which may lead to joyriders travelling there and leaving the vehicle there.

San Francisco also automatic license plate reader cameras installed which make it hard to stay undetected in a stolen vehicle for long potentially leading to car thiefs preferring to not drive very far.

## Polar charts

This visualization explores the directional patterns of vehicle theft by analyzing where stolen cars from each district were later found. Each subplot represents a different district and displays the distribution of movement directions using a polar histogram. The angles correspond to the directions in which stolen vehicles were recovered relative to their theft locations.

By plotting these distributions, we can identify trends in vehicle movement after theft—such as whether stolen cars are typically recovered in specific directions. This analysis can provide insights into crime patterns and potentially inform law enforcement strategies for vehicle theft prevention.

![Polar charts](/assets/images/polars.png)

<!-- ![Alt text](/assets/images/polars.png) -->