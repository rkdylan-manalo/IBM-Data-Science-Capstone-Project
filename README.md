# IBM Data Science Capstone Project

## Introduction
This repository contains all of the Jupyter Notebooks and other relevant files/media required to mark this course. I was tasked to apply the skills I learnt on the IBM Data Science MOOC and apply it to a simulated scenario with real data. The provided scenario included using SpaceX data to predict whether the company will launch a rocket or not. 

As a starting point for every data science project, I needed to collect as much relevant data as possible. The main sources of data I used were from a SpaceX API on past launches (https//:api.spacexdata.com/v4/launches/past/), and web scraping using the Python library BeautifulSoup for relevant Wikipedia pages. Additional APIs were also used for further information:
1. getBoosterVersion: Rockets; URL: https//:api.spacexdata.com/v4/launches/rockets/
2. getLaunchSite: Launchpads; URL: https//:api.spacexdata.com/v4/launches/launches/
3. getPayloadData: Payloads; URL: url: https//:api.spacexdata.com/v4/launches/payloads/
4. getCoreData: Core; URL: https//:api.spacexdata.com/v4/launches/cores/

One of the headers obtained from data wrangling was named 'Outcome' with eight possible results. For simplicity sake, I will map the outcomes to either zero (failure) and one (success). 

## Exploratory Data Analysis


## Interactive Visual Analytics & Dashboard


## Predictive Analysis (Classification)
