# NBA Shot Prediction - Maximizing Chances of Victory in Basketball

## Project Overview

Our objective is to build a shot prediction model, whether the player will score or not score, based on the data analysis that we conduct after taking the shots and the circumstances under which they are made into consideration, to help all stakeholders develop more effective game strategies. 
In building our models, our data mining goal is to find the best model that has the highest accuracy and F1-score.


## Impact on Stakeholders and Potential Benefits

![Impact on Stakeholders](/images/table1.png)


## Data Understanding & Preparation

We will first explain our original dataset before explaining how it is prepared. Afterwards, we will explore our new, blended dataset using exploratory data visualization (EDA) methods.

### The Original Kaggle Dataset

The dataset is a public Kaggle dataset that records all the shots attempted during the NBA 2014-2015 season. It is uploaded by a Kaggle data scientist named “DanB”, and he derived the raw data from NBA’s REST API. The target variable is the “Shot Result”, whether the player made the shot (“made”) or missed the shot (“missed”). The predictor variables include “Game_ID”, “Matchup”, “Location”, “W”, “Final_Margin”, “Shot Number”, “Period”, “Game_Clock”, “Shot_Clock”, “Dribbles”, “Touch_Time”, “Shot_Dist”, “PTS_Type”, “Closest_Defender”, “Closest_Defender_Player_ID”, “FGM”, “PTS”, “player_name”, and “player_ID”. There is a total of 128,069 data point (or shots attempted), each with 20 variables explaining the shot’s feature. The completeness of the dataset is quite high, but the depth of information on players is quite shallow. We thus decided to find another dataset on players’ personal information.

[Link to the original dataset](https://www.kaggle.com/dansbecker/nba-shot-logs)

### Data Preparation Steps

We followed the 5 essential data preparation steps to create our ideal dataset. First, we gathered NBA players’ seasonal data from Kaggle1 and used Vlookup in Excel to link our original dataset’s variables “Closest Defender’s Name” and “Player” to their seasonal data. Second, we cleaned our dataset through deleting 70 variables that we deem unnecessary, such as offense variables in defenders and defend variables in offenders. We then renamed predictor variable fields so that we could conduct data blending, or matching the correct player data to the shots’ data. Lastly, we did data sampling by taking out data entries that we found to be outliers. Our finalized dataset has **127,951 observations with 46 variables**.

### Data Understanding Using Visualization

This session will illustrate relationship between pairs or small numbers of attributes using different visualization techniques.

#### The Box Plot

The Box Plot illustrates the relationship between the height of players and their positions in teams. Intuitively, players with center positions, who are normally the last line of defense in an offensive attempt, needs to be the tallest. Similarly, players who are point guards usually are ball-handler and requires a relatively smaller physique to agilely move around in the field.

![](/images/plot1.png)

#### Distribution Plot

Figure 2 is a distribution plot of the shot-distance, from which a pattern can be clearly observed. Most of the shots made were concentrated to areas close to the basket or close to the three-point line (7.24 m). This makes intuitive sense because players either want to maximize probability of making the shot by being close to the basket or trying to maximize their points by trying outside the three-point line.

!(/images/plot2.png)

#### The Violin Plot

Above is the violin plot that illustrates the relationship between shot distance and shot results of different positions.




