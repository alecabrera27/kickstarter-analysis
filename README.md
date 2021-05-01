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

For our next analysis we want to compare what are the funding goals that have being more successful, and compare them with the failed funding goals, so that our client can set realist and successful funding goals for her theater kickstarter campaign.

we will set different ranges of goals and is the function on excel
```
COUNTIFS()
```
We'll be using this function for columns we created named “*Number Successful*”, “*Number Failed*”, and “*Number Canceled*”

Below are the the formulas used for each row of the "*Number Successful*" Column filtered by the category "*Plays*"
```
=COUNTIFS(Kickstarter!$D:$D,"<1000",Kickstarter!$F:$F,"successful",Kickstarter!R:R,"plays")
=COUNTIFS(Kickstarter!$D:$D,">=1000",Kickstarter!$F:$F,"successful",Kickstarter!$D:$D,"<=4999",Kickstarter!$R:$R,"plays")
=COUNTIFS(Kickstarter!$D:$D,">=5000",Kickstarter!$F:$F,"successful",Kickstarter!$D:$D,"<=9999",Kickstarter!$R:$R,"plays")
=COUNTIFS(Kickstarter!$D:$D,">=10000",Kickstarter!$F:$F,"successful",Kickstarter!$D:$D,"<=14999",Kickstarter!$R:$R,"plays")
=COUNTIFS(Kickstarter!$D:$D,">=15000",Kickstarter!$F:$F,"successful",Kickstarter!$D:$D,"<=19999",Kickstarter!$R:$R,"plays")
=COUNTIFS(Kickstarter!$D:$D,">=20000",Kickstarter!$F:$F,"successful",Kickstarter!$D:$D,"<=24999",Kickstarter!$R:$R,"plays")
=COUNTIFS(Kickstarter!$D:$D,">=25000",Kickstarter!$F:$F,"successful",Kickstarter!$D:$D,"<=29999",Kickstarter!$R:$R,"plays")
=COUNTIFS(Kickstarter!$D:$D,">=30000",Kickstarter!$F:$F,"successful",Kickstarter!$D:$D,"<=34999",Kickstarter!$R:$R,"plays")
=COUNTIFS(Kickstarter!$D:$D,">=35000",Kickstarter!$F:$F,"successful",Kickstarter!$D:$D,"<=39999",Kickstarter!$R:$R,"plays")
=COUNTIFS(Kickstarter!$D:$D,">=40000",Kickstarter!$F:$F,"successful",Kickstarter!$D:$D,"<=44999",Kickstarter!$R:$R,"plays")
=COUNTIFS(Kickstarter!$D:$D,">=45000",Kickstarter!$F:$F,"successful",Kickstarter!$D:$D,"<=49999",Kickstarter!$R:$R,"plays")
=COUNTIFS(Kickstarter!$D:$D,">50000",Kickstarter!$F:$F,"successful",Kickstarter!$R:$R,"plays")
```
For the columns "*Number Failed*" and "*Number Canceled*" we used the same formula, but changed the "*successful*" to the corresponding colum.
Now, having the number of successful, failed and canceled projects, we can use 
```
SUM()
```
to populate a column named “*Total Projects*”  and find the percentages 
Using pivot Charts we can create a visual and analyse the results. 

![Outcomes_vs_Goals](https://user-images.githubusercontent.com/78781719/116791766-1afa1700-aa82-11eb-91ea-a5a96ff747c0.png)

What we can learn about this line chart is that projects with large goals have a higher risk of failing. 
The higher percentage of successful goals are in the range of less than $1000 USD and $4999 USD.


## Results 

-We can conclude that if we want to be successful on our theater kickstarter project we should launch it during the month of April and May. 
The seasons of the year when we should definitely avoid launching these type of kickstarter campaigns should be during fall and winter, since people are not very likely to participate. 

-The probability of being succesful increases if we set our goal between $1000 USD and $4000 USD.

-In the futures, for other analysis,  we could compare the success of the theater kickstarter campaigns with other countries, to analyze where are the people more willingly to participate on these types of categories 
