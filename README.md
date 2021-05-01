# kickstarter-analysis
Performing analysis on Kickstarter data to uncover trends.
## Overview:
With the help of the [kickstarter.com](https://www.kickstarter.com/) community, Louise almost reached her fundraising goal for her *Fever* play, we will analyze data from 
different campaigns, launch dates and funding goals, compare their outcomes to predict when could be the best dates to launch another theater fundraiser and have more probability 
to reach the goal. 

### Purpose
Using the kickstarter data we will analyze based on the category, specifically, theater, compare the different goals each fundraiser had, launch date, and calculate the percentage 
of successful or failed campaigns, creating visuals with excel pivot tables and charts.  


## Analysis: 
First, it is important to analyze when are the best dates to launch fundraisers, predict when are the best seasons or months when people are more willing to donate to theater in kickstarter campaings.

-we will start by creating a new column where we will only have the years of the campaigns, using
```
=YEAR()
```
to extract the year from the "*Date Created Conversion*" column.

-Using this information, we will create a pivot table, with filtered categories “*Theater*” and “*Years*”
-On our rows we’ll be able to see the “*successful*”, “*Failed*”, “*Canceled*” and “*Total*” campaigns by month

![Theater_Outcomes_vs_Launch_Table](https://user-images.githubusercontent.com/78781719/116791355-56471680-aa7f-11eb-939f-b2c53c6f916c.PNG)


### Outcomes Based on Launched Date

Looking on past data, and creating a visual with pivot charts we can find opportunities to be successful on launching a theater kickstarter. 
Based on the charts created by the results on the data,our recommendation is to start the kickstarter campaigns after the months of April and no later than August, since we can see the lowest participation of this season on the month of September. 
It is highly suggested that no theater campaign should be done during the months between September through March, Fall and Winter seasons, as we can see very low funding participation during these months.


![Theater_Outcomes_vs_Launch png](https://user-images.githubusercontent.com/78781719/116791676-a3c48300-aa81-11eb-8ad2-11cbb5582ca7.PNG)


### Outcomes Based on Goals

![Outcomes_vs_Goals](https://user-images.githubusercontent.com/78781719/116791766-1afa1700-aa82-11eb-91ea-a5a96ff747c0.png)


### Challenges and Difficulties 

## Results 


