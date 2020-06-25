# Stows News Wave Capstone Project

This project analyzes movements in stocks' prices and correlates them to news releases and how institutional investors can be aware of these news before retail investors.

## Motivation

The goal of this project is to able to identify a wave like pattern in stock data that implies the foreknowledge of news events by institutional investors. Then be able to confirm these patterns with the actual news data. //Revising

## Problem Statement

If we acknowledge that institutional investors have access to news before the public does, what is the impact of news information on stock price? 

## Prerequisites

### Built With

* [Python](https://www.python.org/) - Language used.
* [Jupyter Notebooks](https://jupyter.org/install) - IDE used for the project.
* [Azure Notebooks](https://notebooks.azure.com/) - Online version of the IDE.

### Libraries Required
This project was made in the Python language, utilizing Jupyter notebooks.
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

In order to download this libraries you will need to add a new chunk to the code and run it before the import statements.


!pip install requests

!pip install json

!pip install pandas

!pip install numpy

!pip install datetime

!pip install pickle

!pip install matplotlib

!pip install time

!pip install mysql.connector


This list of commands will gather all the required libraries.
Each section of the code already has the import statements stablished for it to run.


### Gathering the data

The data for this project was gathered from the webpage [Dukascopy](https://www.dukascopy.com/trading-tools).

The code gathers the data automatically by running each instruments' notebook and stores it into two cvs files, one for tick bars and another one for volume bars.

### Text Findings



### Visualizations
These are some visualization that were obtained from the analysis. they will provide a summary of what the conclusions were.

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
                      
   This is mine actual time series model and one can see the predicted values and how close they were to the actual value. The model had a good accuracy interval.

![alt text](https://github.com/TheCodeMaster2030/Money_Moves/blob/master/code/Time_series.png?raw=true)
  </p>
         </details>
         

## Authors


* **Damian Echevest**


## Acknowledgments

* **Dr. Mondesire, S.** 
* **Sebastian Calzadilla** 
* **Weiyuan Wu**
