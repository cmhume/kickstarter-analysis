# An Analysis of Kickstarter Campaigns

## Overview of Project

The purpose of this analysis is to inform future Kickstarter campaign launches about the relationships between launch date and final outcome and between initial goals set and ultimate pledges recieved.  This was done by analyzing past Kickstarter campaign's final outcomes from the "theater" parent category, and Kickstarter campaign's pledges based on their month launched and goals set from the "plays" subcategory. The dataset used in this analysis was from campaigns launched between the years 2009-2017. The original data used to perform the analysis incuded information such as name, goal, pledges, launch date, deadline, country, and category among others. The "theater" and "plays" campaign data was from a larger dataset including other campaign categories.  The complete Kickstarter dataset is available here: [Kickstarter_Challenge.zip](https://github.com/cmhume/kickstarter-analysis/files/6178596/Kickstarter_Challenge.zip)
   

### Purpose


This data will help inform decisions on when to launch and what goals to set for a successful campaign.  This analysis focuses on theater based campaigns to align with the client's likely future campaign launches.


## Analysis and Challenges


Using Excel spreadsheets and given Kickstarter campaign data, a new pivot chart was created to display outcomes of successful, failed, and cancelled theater campaigns in 
comparison to the month of each campaign's launch date.  In order to create the pivot table a new "Years" column was created in the original Kickstarters worksheet. The conversion command was used to automatically show the year from the given "Date created conversion" column.  After filtering the Parent Category to "theater" and selecting the columns for Year, Parent Category, and outcome, a pivot table was made by choosing pivot table in the Insert tab. A line chart was made from the data in the pivot table after assigning values for columns, rows, and filters.  After the pivot table, an additional worksheet was created using COUNTIFS() and other Excel functions to compare a range of initial fundraising goals for kickstarter campaigns categorized as "plays" with the final outcomes of successful, failed or cancelled. For each range of fundraising goal, the number of campaigns for each outcome were added together to find the total number of campaigns, and this number was used to calculate the percentage of successful, failed or cancelled campaigns for that fundraising goal range.  This data was used to create a line graph comparing the initial fundraising goal with the final outcome, either successful, failed, or cancelled.  Line graphs from "Theater Outcomes by Launch Date" and "Outcomes by Goal" are shown below under their subsequent headings. In summary, the steps completed for this analysis were:


### Step 1: Add years column to Kickstarter sheet

![years_column_added](https://user-images.githubusercontent.com/78699521/111915021-a15a1c80-8a31-11eb-969d-cc72f3695a84.png)



### Step 2: Create pivot table from "Kickstarter" in new sheet "Theater Outcomes by Launch Date" and graph data


#### Step 2a) Create pivot table


![launch_date_pivot_table](https://user-images.githubusercontent.com/78699521/111923004-4d176280-8a5a-11eb-9916-58397ec722ca.png)


#### Step 2b) Create line graph


![make_line_graph](https://user-images.githubusercontent.com/78699521/111922996-3ec94680-8a5a-11eb-8cc0-17424fd8c2be.png)



### Step 3: Create new sheet "Outcomes Based on Goals" and graph data


#### 3a) use COUNTIFS function to find number of each outcome type from campaigns categorized as "plays" within set goal ranges


![goal_chart_COUNTIFS](https://user-images.githubusercontent.com/78699521/111914654-10367600-8a30-11eb-9eea-dbc81f496e01.png)


#### 3b) use SUM function to find total number of campaigns for each goal range


![goal_chart_sum_function](https://user-images.githubusercontent.com/78699521/111914663-19bfde00-8a30-11eb-9461-36c95e14c5ec.png)


#### 3c) find percent of succesful, failed or cancelled campaigns out of total campaigns for the goal ranges


![goal_chart_percent_equation](https://user-images.githubusercontent.com/78699521/111914666-204e5580-8a30-11eb-8f41-970561a2b5f3.png)



## Theater Outcomes by Launch Date


![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/78699521/111227930-99692b00-85a0-11eb-9e60-b4b98588960b.png)


## Outcomes Based on Goals


![Outcome_vs_Goals](https://user-images.githubusercontent.com/78699521/111227846-6de64080-85a0-11eb-908d-ff27f08d9011.png)


### Challenges


The first challenge with this analysis was configuring the COUNTIFS function correctly for the "Outcomes based on Goals" worksheet.  This was a challenge because of the 12 
different ranges and the need for using >= and <= symbols.  I looked up how to write greater than or equal to and less than or equal to in the COUNTIFS formula in the Microsoft Excel documentation available online.  The second challenge was creating a line graph with only the goal and percent outcome columns.  I wasn't able to 
select non continuous columns to create a graph, so I ended up creating another table with the data from just the goals and percent outcomes and then creating a graph with 
that.  The third challenge was formatting the graphs with colors that matched the formatting used in the Kickstarter database; green for successful, red for failed, and yellow 
for cancelled.  I used the pagelayout tab and customized the colors to change the legend colors shown on the graph.


#### Challenge of graphing "Outcomes Based on Goals":


![goal_chart_table](https://user-images.githubusercontent.com/78699521/111914187-39ee9d80-8a2e-11eb-89f0-3a57271f2763.png)



#### Challenge of customizing chart colors:


![customize_chart_colors](https://user-images.githubusercontent.com/78699521/111914547-aae28500-8a2f-11eb-9722-9e359c465cdb.png)


## Results


### Theater Outcomes by Launch Date


As displayed in the earlier graph "Theater Outcomes by Launch Date", May, June, and July were the top three months respectively to launch successful theater campaigns.  Overall, there were more successful than failed or cancelled theater campaigns for every month in the year.  The least number of successful campaigns were launched in December.  Failed theater campaigns varied less by month than successful campaigns.  Suprisingly, like successful campaigns, May was also the month with the most failed campaigns of the year. Throughout the summer months May through August, failed campaigns were close to the same, ranging from 52 to 47.  The month with the least failed campaigns was November, followed closely by January, March, and September.  Cancelled outcomes were the least likely overall.  October had no cancelled theater outcomes and the highest number of cancelled outcomes happened in January with a total of  7 cancelled campaigns.  Overall, May seems to be the best month to launch a campaign and December appears to be the worst month to launch a campaign.  In general, theater campaigns appear to be more likely to succeed than fail for any launch month.


### Outcomes Based on Goals


Initial campaign fundraising goals appear to have an impact on the success or failure of campaigns categorized as plays.  Campaigns with goals less than $1000 were the most successful (76%) followed by goals between $1,000 to $4,999 (73%).  Interestingly, after declining in success to a near low of 20% in the $25,000 to $29,999 range, campaigns in the $35,000 to $44,999 range were the third most successful coming in at 67% successful outcomes.  The least successful outcomes had goals between $45,000 and $49,999 at 0% successful. There were no cancelled campaigns in the plays category for this subset.  


### Summary of limitations and additional recommendations

For "Theater Outcomes Based on Launch Date," the datavisualization is based on all campaign years (2009-2017) with the Parent Category of "theater."  With out going through each year's campaign outcomes, it is hard to say with certainty that the outcomes by month shown on the chart are not  showing outlier data from one particularly successful or unsuccesful year.  Also, looking through the campaigns by year show a difference in the total number of theater campaigns launched. The number of campaigns launched in a year or a month may have an impact on their success.  Further analysis with central tendency statistics and inter quartile range could show how strong the relationships are between launch month and final outcome. In addition, the use of the parent category "theater" includes data from the subcategories "musical, plays, and spaces". If the subcategory "plays" was used in "Outcomes Based on Launch Date" instead of "theater," the data would be more comparable to the results in the "Outcomes Based on Goals" analysis.  Adding information on percent outcome as was done in the "Outcomes Based on Goals" sheet would also provide additional insight into the relation between outcomes and launch month.

For the "Outcomes Based on Goals" chart, the data used to determine percent outcome was based on different numbers of total projects for each goal range.  The high percentage of succesful campaigns seen at the higher goals of $35000 to $44,999 were only based on 3 total projects while the first goal of <$1000 was based on 186 projects.  With this dataset it is hard to know if campaigns in the $35,000 to $44,999 goal range would show the same percent of success if there were more datapoints.  Looking at different goal ranges with a similar number of total campaigns would provide more reliable data. Also, the linechart used to visualize the "Outcomes Based on Goals" was misleading, suggesting a gradation between goal points on the x-axis, when in fact each x-axis label was itself a range. A bar graph would communicate the data and inclusion of range with in each x-value more clearly.  

