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

### Text Findings



### Visualizations

<details>
           <summary>Visualization 1</summary>
           <p>
         
The following visualization shows How the price changed throughout the years. It shows minimun, max and average value
![alt text](https://github.com/TheCodeMaster2030/Money_Moves/blob/master/code/download.png?raw=true)

</p>
</details>
<details>
           <summary>Visualization 2</summary>
           <p>
                      


![alt text](https://github.com/TheCodeMaster2030/Money_Moves/blob/master/code/Time_series.png?raw=true)
  </p>
         </details>
         

## Authors


* **Damian Echevest**


## Acknowledgments

* **Dr. Mondesire, S.** 
* **Sebastian Calzadilla** 
* **Weiyuan Wu**
