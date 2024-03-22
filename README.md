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

Using **Pandas**, some features were taken from the secondary dataset in order to have a more complete dataset and the necessary transformations were performed to have the dataset with a suitable format to feed the Power BI bashboard.

#### 2) **Teams.csv**

This file contains general information about each team in the tournament such as team ID, country, market value, confederation, flag, best result and appearances in previous FIFA World Cups. It was made taking data from different sources:

- Market value of each team: [CIES Football Observatory - Weekly Post 397](https://football-observatory.com/IMG/sites/b5wp/2022/wp397/en/)
- Team ID: Own creation
- The rest of the data: [Wikipedia](https://www.wikipedia.org/)

#### 3) **Squads.xlsx**
This file contains data about the players in each team in the tournament such as number, position, name, age, team ID, caps, goals, club and league where he plays.

Source: [FIFA World Cup 2022 squads](https://en.wikipedia.org/wiki/2022_FIFA_World_Cup_squads)

## Data Preparation 

- For WorldCup2022.csv, the main transformations were performed with Pandas and its explanation is in [ETL_FIFA_World_Cup_2022.ipynb](https://github.com/julianmancuello/FIFA_World_Cup_2022/blob/main/ETL_FIFA_World_Cup_2022.ipynb)
- For Teams.csv and Squads.xlsx, given the simplicity of the data, they were processed in Microsoft Excel.

## Dashboard

To make it more enjoyable for the person who visits this repository, avoiding to install Power BI on their computer and download the Power BI file, the results of the dashboard are presented below.

### Overview by confederation

In this visualization we can see an overview of the tournament as a whole or by confederation.

Some insights to highlight:
- We can see that **England** is the team with the highest market value, followed by **Brazil** and **France**. In 6th place is **Germany** with a market value of €1,020M, which was eliminated in the group stage.
- **Iran** has the highest average age of the entire tournament.
- We can see that the Big Five European leagues (**England**, **Spain**, **Germany**, **Italy** and **France**) contribute 54.87% of the players in the tournament, with the English league being the one with the highest participation with 19.74% and 164 players.
- **Barcelona**, **Bayern Munich** and **Manchester City** are the teams that contribute the most players to the tournament with 17, 16 and 16 respectively.
- Regarding the distribution by age, we can see that the majority of players are between 24 and 30 years old.

https://github.com/julianmancuello/FIFA_World_Cup_2022/assets/162643807/39fc5d66-c42a-4ad0-acb1-8d23626197e2

### Overview by team

In this visualization we can see an overview of each team in the tournament.

Some insights to highlight:
- In **Argentina**:
  - **Lionel Messi** is by far the player with the most goals and caps, followed by **Ángel Di María**.
  - 19 of 26 players play in the leagues of **Spain**, **England** and **Italy**.

- In **Germany**:
  - **Thomas Müller** and **Manuel Neuer** are by far the players with the most caps.
  - 20 of 26 players play in the German league.
  - **Bayern Munich** is the club that contributes the most players with 7.

- In **Portugal**:
  - **Cristiano Ronaldo** is by far the player with the most goals and caps.
  - His own league has a significant contribution of players to the team with 7.
  - It has a market value of €1,154M, one of the highest in the tournament.

https://github.com/julianmancuello/FIFA_World_Cup_2022/assets/162643807/8a61b09b-24c7-4517-afc1-8c9f3cd64d93

### Defensive and offensive efficiency

In this visualization we can see a quadrant graph, which shows the defensive and offensive efficiency of each team.

To represent defensive efficiency, the ***defensive efficiency in line breaks*** will be used as a variable, that is, when the team receives an attack from the opponent, what is the percentage of success of the defense frustrating line break attempts.

To represent offensive efficiency, the ratio ***On target attempts / Total attempts*** will be used as a variable, that is, when the team attacks and shots, what is the percentage of shots placed towards the goal. This measure provides the effectiveness of the team when completing the attacks.

As a complement, this dashboard has a bar chart with the average of passes completed by team.

Some insights to highlight:

- Considering only the matches corresponding to the group stage and round of 16:
  - **Argentina**, **England**, **Brazil**, **Croatia** and **Portugal** were the teams with the best defensive and offensive efficiency.
  - **Spain**, the team with the highest average number of passes completed, showing great control over the ball and the flow of the game, paid dearly for its low offensive efficiency, close to 30%, being eliminated in the round of 16.
  - **France**, one of the best teams in the tournament, had a performance close to average.
  - The big disappointments of the tournament were **Germany** and **Belgium**, who although they had a high average of passes completed, showing good control over the ball and the flow of the game, due to their low defensive and offensive efficiency they did not manage to pass the group stage.
  - **Mexico** is an outlier, having almost 70% defensive efficiency and an offensive efficiency close to average, it failed to make it past the group stage. The other side of this is **Poland**, with whom they shared group C, which had one of the worst defensive and offensive efficiencies of the tournament but still managed to pass the group stage.
  - **Costa Rica** and **Cameroon** are also outliers, you can see a high offensive efficiency but if we look at the completed passes we can see that these were very low (not seen in the video), so we can conclude that these teams had little of the ball , barely reaching the rival goal, but on the occasions they kicked, the shots went to the goal.

https://github.com/julianmancuello/FIFA_World_Cup_2022/assets/162643807/08f402f6-6377-43d6-9605-19e0ac6b6b65








