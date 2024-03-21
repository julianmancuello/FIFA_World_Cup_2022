![Imagen](https://www.jumpdesign.co.uk/wp-content/uploads/2021/02/BANNER-LOGO-1024x288.jpg)
# FIFA World Cup 2022 Dashboard

## Overview
This repository contains a Power BI dashboard about the FIFA World Cup Qatar 2022. It includes a Jupyter Notebook in which the data processing was performed with Python.

## Tech Stack
- Power BI
- Python 3.11.5
- Python library: Pandas

## Data Sources
In order to feed the dashboard 3 files were used:

#### 1) **WorldCup2022.csv**

This file was generated with the jupyter notebook [ETL_FIFA_World_Cup_2022.ipynb](https://github.com/julianmancuello/FIFA_World_Cup_2022/blob/main/ETL_FIFA_World_Cup_2022.ipynb).
The objective of this Jupyter Notebook is generate a CSV that can feed a Power BI dashboard with all the data corresponding to every match in the FIFA World Cup 2022.

To achieve this two different datasets were used:
1) The main dataset is the following Kaggle dataset: [Main dataset](https://www.kaggle.com/datasets/die9origephit/fifa-world-cup-2022-complete-dataset)
2) The secondary dataset is the following Kaggle dataset: [Secondary dataset](https://www.kaggle.com/datasets/swaptr/fifa-world-cup-2022-match-data)

Some features were taken from the secondary dataset in order to have a more complete dataset and the necessary transformations were performed to have the dataset with a suitable format to feed the Power BI bashboard.

#### 2) **Teams.csv**

This file contains general information about each team in the tournament such as team ID, country, market value, confederation, flag, best result and appearances in previous FIFA World Cups. It was made taking data from different sources:

- Market value of each team: [CIES Football Observatory - Weekly Post 397](https://football-observatory.com/IMG/sites/b5wp/2022/wp397/en/)
- Team ID: Own creation
- The rest of the data: [Wikipedia](https://www.wikipedia.org/)

#### 3) **Squads.xlsx**
