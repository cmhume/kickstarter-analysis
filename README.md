# An Analysis of Kickstarter Campaigns

## Overview

The purpose of this analysis is to inform future Kickstarter campaign launches about the month to launch and goal to set by analyzing past theater Kickstarter campaign's final outcomes and plays Kickstarter campaign's pledges based on their month launched and goals set.


## Analysis and Challenges


Using Excel spreadsheets and given Kickstarter campaign data, a new pivot chart was created to display outcomes of successful, failed, and cancelled theater campaigns in 
comparison to the month of each campaign's launch date.  In order to create the pivot table a new "Years" column was created in the original Kickstarters worksheet. The conversion command was used to automatically show the year from the given "Date created conversion" column.  An additional worksheet was created using COUNTIFS() and other Excel functions to compare a range of initial fundraising goals for kickstarter campaigns categorized as "plays" with the final outcomes of successful, failed or cancelled. For each range of fundraising goal, the number of campaigns for each outcome were added together to find the total number of campaigns, and this number was used to calculate the percentage of successful, failed or cancelled campaigns for that fundraising goal range.  This data was used to create a line graph comparing the initial fundraising goal with the final outcome, either successful, failed, or cancelled.  Screenshots from the previous steps mentioned are shown below:

### Step 1: Add years column

![years_column_added](https://user-images.githubusercontent.com/78699521/111915021-a15a1c80-8a31-11eb-969d-cc72f3695a84.png)



### Step 2: Create pivot table in new sheet "Theater Outcomes by Launch Date" and graph data


![launch_date_pivot_table](https://user-images.githubusercontent.com/78699521/111914603-d82f3300-8a2f-11eb-81ea-0fd048854840.png)



### Step 3: Create new sheet "Outcomes Based on Goals" and graph data


#### 3a) using COUNTIFS function to find number of campaigns within set goal ranges


![goal_chart_COUNTIFS](https://user-images.githubusercontent.com/78699521/111914654-10367600-8a30-11eb-9eea-dbc81f496e01.png)


#### 3b) using SUM function to find total number of campaigns for each goal range


![goal_chart_sum_function](https://user-images.githubusercontent.com/78699521/111914663-19bfde00-8a30-11eb-9461-36c95e14c5ec.png)


#### 3c) finding percent of succesful, failed or cancelled campaigns out of total campaigns for the goal ranges


![goal_chart_percent_equation](https://user-images.githubusercontent.com/78699521/111914666-204e5580-8a30-11eb-8f41-970561a2b5f3.png)




## Theater Outcomes by Launch Date


![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/78699521/111227930-99692b00-85a0-11eb-9e60-b4b98588960b.png)


## Outcomes Based on Goals


![Outcome_vs_Goals](https://user-images.githubusercontent.com/78699521/111227846-6de64080-85a0-11eb-908d-ff27f08d9011.png)


### Challenges


The first challenge with this analysis was configuring the COUNTIFS function correctly for the "Outcomes based on Goals" worksheet.  This was a challenge because of the 12 
different ranges and the need for using >= and <= symbols.  The second challenge was creating a line graph with only the goal and percent outcome columns.  I wasn't able to 
select non continuous columns to create a graph, so I ended up creating another table with the data from just the goals and percent outcomes and then creating a graph with 
that.  The third challenge was formatting the graphs with colors that matched the formatting used in the Kickstarter database; green for successful, red for failed, and yellow 
for cancelled.  I used the pagelayout tab and customized the colors to change the legend colors shown on the graph.

#### Challenge of configuring COUNTIFS function:


![goal_chart_table](https://user-images.githubusercontent.com/78699521/111914187-39ee9d80-8a2e-11eb-89f0-3a57271f2763.png)



#### Challenge of customizing chart colors:


![customize_chart_colors](https://user-images.githubusercontent.com/78699521/111914547-aae28500-8a2f-11eb-9722-9e359c465cdb.png)


## Results


### Theater Outcomes by Launch Date


As displayed in the previous graph, May, June, and July were the top three months respectively to launch successful theater campaigns.  Interestingly, there were more 
successful than failed or cancelled theater campaigns for every month in the year.  The least number of successful campaigns were launched in December.  Failed theater 
campaigns varied less by month than successful campaigns.  Suprisingly, like successful campaigns, May was also the month with the most failed campaigns of the year. Throughout 
the summer months May through August, failed campaigns were close to the same ranging from 52 to 47 over those months.  The month with the least failed campaigns was November, 
followed closely by January, March, and September.  Cancelled outcomes were the least likely overall.  October had no cancelled theater outcomes and the highest number of 
cancelled outcomes happened in January with a total of  7 cancelled campaigns.


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
based on goals, doing each analysis for each category would give more comparable results for those categories.  Also the addition of central tendency statistics and graphing IGR would give additional insight into how strong the relationship between launch date or goals set and final outcome.
