# An Analysis of Kickstarter Campaigns

## Overview

The purpose of this analysis is to inform future Kickstarter campaign launches about the month to launch and goal to set by analyzing past theater Kickstarter campaign's final outcomes and pledges based on their month launched and goals set.


## Analysis and Challenges


Using Excel spreadsheets and given Kickstarter campaign data, a new pivot chart was created to display outcomes of successful, failed, and cancelled theater campaigns in 
comparison to the month of each campaign's launch date.  A line graph showing the results is shown below under 'Theater Outcomes by Launch Date'.  An additional worksheet was 
created using COUNTIFS() and other Excel functions to compare a range of initial fundraising goals for kickstarter campaigns categorized as "plays" 
with the final outcomes of successful, failed or cancelled. For each range of fundraising goal, the number of campaigns for each outcome were added together to find the total 
number of campaigns, and this number was used to calculate the percentage of successful, failed or cancelled campaigns for that fundraising goal range.  This data was used to 
create a line graph comparing the initial fundraising goal with the final outcome, either successful, failed, or cancelled.  This graph is shown below under "Outcomes Based on 
Goals."         


### Theater Outcomes by Launch Date


![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/78699521/111227930-99692b00-85a0-11eb-9e60-b4b98588960b.png)


### Outcomes Based on Goals


![Outcome_vs_Goals](https://user-images.githubusercontent.com/78699521/111227846-6de64080-85a0-11eb-908d-ff27f08d9011.png)


### Challenges


The first challenge with this analysis was configuring the COUNTIFS function correctly for the "Outcomes based on Goals" worksheet.  This was a challenge because of the 12 
different ranges and the need for using >= and <= symbols.  The second challenge was creating a line graph with only the goal and percent outcome columns.  I wasn't able to 
select non continuous columns to create a graph, so I ended up creating another table with the data from just the goals and percent outcomes and then creating a graph with 
that.  The third challenge was formatting the graphs with colors that matched the formatting used in the Kickstarter database; green for successful, red for failed, and yellow 
for cancelled.  I used the pagelayout tab and customized the colors to change the legend colors shown on the graph.


## Results


### Theater Outcomes by Launch Date


As displayed in the previous graph, May, June, and July were the top three months respectively to launch successful theater campaigns.  Interestingly, there were more 
successful than failed or cancelled theater campaigns for every month in the year.  The least number of successful campaigns were launched in December.  Failed theater 
campaigns varied less by month than successful campaigns.  Suprisingly, like successful campaigns, May was also the month with the most failed campaigns of the year. Throughout 
the summer months May through August, 
failed campaigns were close to the same ranging from 52 to 47 over those months.  The month with the least failed campaigns was November, followed closely by January, March, 
and September.  Cancelled outcomes were the least likely overall.  October had no cancelled theater outcomes and the highest number of cancelled outcomes happened in January 
with a total of  7 cancelled campaigns.


### Outcomes Based on Goals


Initial campaign fundraising goals appear to have an impact on the success or failure of campaigns categorized as plays.  Campaigns with goals less than $1000 were the most 
successful (%76) followed by goals between $1000 to $4999 (%73).  Interestingly, after declining in success to a near low of %20 in the 25k to 30k range, campaigns in the 35k 
to 45k range were the third most successful coming in at 67% successful outcomes.  The least successful outcomes had goals between 45k and 50k at 0% successful. There were no 
cancelled campaigns in the plays category for this subset.  


### Summary of limitations and additional recommendations


For the Outcomes Based on Goals, the data used to determine percent outcome was based on different numbers of total projects for each goal range.  The high percentage of 
succesful campaigns seen at the higher goals of 35k to 45k were only based on 3 total projects while the first goal of <$1000 was based on over 500 projects.  With this dataset 
it is hard to know if campaigns in the 35k to 45k goal range would show the same percent of success if there were more datapoints.  Looking at different goal ranges with a 
similar number of total campaigns would provide more reliable data.  Also, different categories, theater or plays, were used to compare outcomes by launch date and outcomes 
based on goals, doing each analysis for each category would give more comparable results for those categories.  
