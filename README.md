# Stows News Wave Capstone Project

This project analyzes movements in stocks' volatility parameters and correlates them to news releases and how institutional investors can be aware of these news before retail investors.

## Motivation

This project was created with the intent to give retail investors an indicator that there is a potential move in stock prices. The mentioned indicator will facilitate trend identification even before news are released to the general public. Thus, benefiting retail investors and level the playfield between them and institutional investors.


## Problem Statement

If we acknowledge that institutional investors have access to news before the public does, what is the impact of news information on the stock market volatility? 

## Prerequisites

### Built With

* [Python](https://www.python.org/) - Language used.
* [R](https://www.r-project.org/) - Language used

### Libraries Required
The gathering and manipulation of the data was made in the Python language, utilizing Jupyter notebooks.
The Libraries that are require for this Python project to properly run are:

import requests 

import json 

import pandas as pd

import numpy as np

from datetime import datetime, timedelta, time

import pickle

import matplotlib.pyplot as plt

import matplotlib.dates as mdates

from time import process_time 

import mysql.connector

from newsapi import NewsApiClient

The Analysis part of this project, that is under the analysis folder, was performed in R.
The libraries required for the proper implementation of the R code are:

library(tidyverse)

library(lubridate)

library(ggplot2)

library(plotly)

Each section of the code already has the import statements stablished for it to run.


### Gathering the data

The data for this project was gathered from the webpage [Dukascopy](https://www.dukascopy.com/trading-tools).

The code gathers the data automatically by running each instruments' notebook and stores it into two cvs files, one for tick bars and another one for volume bars.

## Methodology

In this study, the data is pulled automatically in a batch process that requests 5000 quotes per request. Then the data is processed by developing volume and tick bars for further analysis. Some of the variables created in the bars are ticks inside the bar, Volume from bid-ask, Price, Spread of bid-ask quotes, and TickRule. The study is then focused on aggregated tick and volumes bars to more precisely detect significantly different pattern behaviors. An index is then developed in which it is 0 at the moment of the news release, or the closest on distance bar. Therefore, allowing us to analyze the significance of the moves before and after the news is released. The next method implemented involves the development of a function which calculates the normalized (to deal with outliers) absolute (to deal with negative values) percentage change on any specified parameter. These procedures allow us to evaluate index detailed behavior on catalyst days, therefore being able to identify the exact index location of the average wave start, end, and strength.

## Text Findings

In conclusion, our research tested whether news catalyst had, in general, an impact on the market volatility. We have tested that both tick and volume bars accurately show these differences, but they also convey information more frequently when markets are moving more (more market orders and more volume being traded).  

Also, we have proven that, in general, before and after news sessions are not significantly different, which reflects that information influences trades (informed investors) before the news are released to the public.  

The research serves as a ground to deep dive into the research of machine learning automated models which would analyze the patterns to signal significant probabilities that news release may arrive and its direction based on the influence on the trades, setting investors steps ahead of the public.  

## Visualizations

<details>
           <summary>"Wave" pattern visualization</summary>
           <p>
                      Aims to visualize “the wave” by plotting the index (distance from news release) vs the row-wise percent change. Significant difference on volume bars supports that these bars are better to classify the wave. They prove the significance between the days with events and the days without events, by showing the increase in volatility and volume.
         

![alt text](https://github.com/DrMondesire/StockNewsWave/blob/master/Graphs/PercentChange.png?raw=true)

![alt text](https://github.com/DrMondesire/StockNewsWave/blob/master/Graphs/IndexPercentChange.png?raw=true)

</p>
</details>

         
 <details>
           <summary>Market trends news days vs no news days</summary>
           <p>
                      These bars visualizes market trends and the news days vs non news days significant different indexes (lines). These graphs helps us test the stastitially different behavior of informed traders (before news release) and the retail investors (after news release). Note that these values may provide better comparison when tested on specific clusters of news days.

   ![alt text](https://github.com/DrMondesire/StockNewsWave/blob/master/Graphs/EventsVSnoEventsSigDif.png?raw=true)
  </p>
 </details>
         

## Authors


* **Damian Echevest**


## Acknowledgments

* **Dr. Mondesire, S.** 
* **Sebastian Calzadilla** 
* **Weiyuan Wu**
