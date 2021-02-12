# Analysis of Kickstarter Campaigns
Uncovering trends in Kickstarter data through excel analysis. 
The goal is to answer if the start date affects the success or failer of theater production kickstartes.

## Project overview
Challenge #1 of Data Analytics Boot Camp from Columbia Engineering
---
This project was an Excel analysis of Kickstarter data to identify trends in successful Kickstarter campaigns. The concern was if Kickstarter is a good fundraising platform for a theater production campaign with a target of $10,000. If it was the goal was to provide a campaign outline that mirrors successfully funded Kickstarter based on the identified trends.
---
## Analysis and challenges
### Preparing the Data
The analysis was completed using LINK WORKBOOK in Microsoft Excel 365. Initial data cleaning included date conversion from the provided time code in the deadline and launch_at columns to new columns Date Created Conversion and Date End Conversion. A column, Year, was created from the Date Created Conversion column using the YEAR formula. Color coded conditional formatting was assigned to the outcomes column. The Parent Category/Subcategory column was split into separate columns for future filtering by Parent Category and Subcategory. 
---
### Is Kickstarter a good platform for this campaign?
To understand the outcomes of the Kickstarter campaigns a PIVOT table was created with the Parent Category as rows and the outcomes as the columns. The data was filtered to show the data from the US. The chart Parent Category Outcomes represents the PIVOT table. INSERET IMAGE The parent category theater includes 525 successful, 349 failed, and 26 canceled campaigns. Overall theater campaigns are successful based on this data. The outcomes were then evaluated by subcategory. INSERET IMAGE The chart Outcomes by Subcategory represent the count of the successful, failed and canceled Kickstarter by the three subcategories; musicals, plays, and spaces. Based on the chart more Kickstarter for plays succeed than failed. These two charts helped to answer the concern of if Kickstarter is a good platform for a theater production campaign. Based on the data presented that most theater play Kickstarters were successful it is a good platform for fundraising. The next step was to analysis the trends of the successful Kickstarter campaigns to develop an outline that mirrors them.
---
### Does the Launch Date influence Kickstarter Outcomes?
To answer the question of is there a good period to launch a Kickstarter for a successful outcome a PIVOT table was created with the rows indicating the launch month and the columns indicating the outcome. This PIVOT table excluded Kickstarters with a live outcome as they have not concluded. Two filters were used in the PIVOT table. The first was to filter by the parent category: theater. The second filter, years, was used to include data from every year in the rows by month. The chart Theater Outcomes Based on Launch Data was created from this PIVOT table. INSERET IMAGE
---
### Does the Goal influence Kickstarter Outcomes?
To answer the question if goals of the Kickstarter campaign influence the outcomes a new workbook was created to organize the information of total outcomes of the subcategory plays by goals. Twelve ranges for goals was created as seen in the Kickstarter Goal Ranges image. INSERT IMAGE Separate columns were created for the number of successful, the number of failed and the number of canceled Kickstarters. The count for each column was calculated using the COUNTIFS formula. Then the column for total number was created using the SUM formula. Three separate columns were created for the percentage of successful, failed, and canceled Kickstarters and calculated by dividing the count by the total number. The chart Theater Outcomes based on Goals was created from these percentages. INSERET IMAGE
---
### Challenges
I encountered a challenge when creating the chart Theater Outcomes based on Goals. The chart originally produced did not reflect the correct dips and pikes. I realized that my calculated percentages were incorrect by the formula had no errors. I returned to the main Kickstarter worksheet to reassess the count columns. I realized I had not used greater or equal to in my original COUNTIFS formulas. INSERET IMAGE My formula missed Kickstarters that had a goal of exactly 5000, 10000, 15000 and so on. I was able to fix the formula relatively easily and my chart showed the correct dips and pikes afterwards. 
---
## Results
### Theater Outcomes based on Launch Date
More Kickstarter campaigns were launched in May than the other months. The month with the highest count of successful theater campaigns was May. However, May was also the month with the highest count of failed theater campaigns. In total about two thirds of the theater Kickstarters lunched in May succeed and one third failed. The second highest number of Kickstarter launches occurred during the month of June and during June the second highest count of successful Kickstarters occurred. The second highest count of failed outcomes occurred for theater Kickstarters launched in October.A planned launch date in the fall would reduce the likelihood that the campaign was successful.  Based on the outcomes launching a theater Kickstarter in May or June would result in a larger pool of competing fundraisers, but the likelihood that the campaign is successful is greater than any of the months of the year. 
---
### Outcomes based on Goals
The range a goal of a Kickstarter campaign with the subcategory plays was greatly affected the percentage of successful and failed outcomes. For example Kickstarters with a goal below $4999 have a successful percentage outcome from 76% to 73%, while Kickstarters with a goal in the  $5000 and $9999 range had a successful outcome percentage of 37%. That was a significant drop based on goal range. Theater play Kickstarters with a goal between $10,000 to $14,999 had a successful outcome percentage of  54% and the successful outcome percentage increases to 86% when the range increases to $15,000 to $19,999. Based on the data launching a Kickstarter for a theater play with a goal of $10,000 or higher is more likely to succeed than fail. 
---
### Limitations of this Dataset
The most recent date included in the dataset if from March, 2017. The dataset is almost five years old. The age of the dataset could limit how accurate the data is related to the trend of crowdfunding is in the year 2021. The sample size of the data is over one thousand for plays but that number may have increased in the past five years. There are several Kickstarters with goals of $1.00 that received much larger pledge amounts. The inclusion of these impact the percentage of successful outcomes of goals below $1000.
---
### Other Possible Comparisons
A table on the average donation and the percentage of outcomes would help identify how the two factors interact and how many donors are needed to reach the campaign goal. This could help the Kickstarter by suggesting an amount to a site visitor reading the fundraising page. Another table focused on the theater Kickstarters with a goal between $10,000 and $14,999 and the launch date may revel more insights when the most successful outcomes are reached for that specific goal. 
