# IBM Data Science Capstone Project

## Introduction

This repository contains all of the Jupyter Notebooks and other relevant files/media required to complete this course. I applied skills taught in the IBM Data Science MOOC to a simulated scenario using real data. The scenario provided SpaceX data to predict whether the company will successfully land a Falcon 9 rocket. The goal of this project is to predict the outcomes of the Falcon 9 first-stage landing process, but to find the answer to this goal, we have to ask the following questions:

1. Which factors influence landing success?
2. Which launch sites and orbits perform best?
3. Can machine learning accurately predict landing success?

## Methodology

As with every data science project, I needed to collect as much relevant data as possible. My main data sources were SpaceX APIs for past launches (https//:api.spacexdata.com/v4/launches/past/) and web scraping using the Python library BeautifulSoup, looking at relevant Wikipedia pages. Additional APIs were also used for further information:

1. getBoosterVersion: Rockets; URL: https//:api.spacexdata.com/v4/launches/rockets/
2. getLaunchSite: Launchpads; URL: https//:api.spacexdata.com/v4/launches/launches/
3. getPayloadData: Payloads; URL: url: https//:api.spacexdata.com/v4/launches/payloads/
4. getCoreData: Core; URL: https//:api.spacexdata.com/v4/launches/cores/

The next step after identifying relevant data sources was to parse the fetched API data (as JSON/HTML files) into data frames via the Python library Pandas. The original dataset also included Falcon 1 information, so I imputed missing values to prepare the dataset for analysis. Additionally, one of the headers obtained from data wrangling was named ‘Outcome’ with eight possible results. For simplicity, I mapped the outcomes to zero (failure) or one (success). I left other useful variables (launch pad usage, booster version, payload mass (kg), etc.) alone, as they were already in perfect condition for data manipulation. 

The penultimate step before exploratory data analysis (EDA) was to understand the data via SQL magic commands in Jupyter Notebook. Analysing the data for imbalances and the underlying context to understand the task at hand (E.G., the baseline success rate of SpaceX launches and the rocket payload mass) was crucial to tell the right story. One query involved counting success versus failure outcomes, with the result showing a clear data imbalance. Recognising this early was critical in the machine learning phase, as relying on one accuracy score can be misleading. Instead, a confusion matrix is necessary to uncover the model’s true predictive performance (E.G., identifying false positives and false negatives).

Finally, prior to EDA, I was also tasked with creating an interactive map of SpaceX launch site locations in North America. These maps included markers, site labels, and the total number of launches per site. While this step failed to introduce new quantitative data, this information provides context to help uncover the project goal. The insights derived from these SQL queries and Folium maps set the stage for the deeper visual analysis in the next section.

## Exploratory Data Analysis

## Interactive Visual Analytics & Dashboard

## Predictive Analysis (Classification)

## Discussion

## Conclusion
