# Analysis of Kickstarter Campaigns
Uncovering trends in Kickstarter data through excel analysis.

## Project overview
Challenge #1 of Data Analytics Boot Camp from Columbia Engineering

This project was an Excel analysis of Kickstarter data to identify trends in successful Kickstarter campaigns. The concern was if Kickstarter is a good fundraising platform for a theater production campaign with a target of $10,000. If it was the goal was to provide a campaign outline that mirrors successfully funded Kickstarter based on the identified trends.

## Analysis and challenges
### Preparing the Data
The analysis was completed using [Kickstarter_Challenge](https://github.com/RuthLD/kickstarter-analysis/blob/main/Kickstarter_Challenge.zip) in Microsoft Excel 365. Initial data cleaning included date conversion from the provided time code in the deadline and launch_at columns to new columns Date Created Conversion and Date End Conversion. A column, Year, was created from the Date Created Conversion column using the YEAR formula. Color-coded conditional formatting was assigned to the outcomes column. The Parent Category/Subcategory column was split into separate columns for future filtering by Parent Category and Subcategory.

### Is Kickstarter a good platform for this campaign?
To understand the Kickstarter campaigns’ outcomes, a PIVOT table was created with the Parent Category in the rows and the outcomes in the columns. The data was filtered to show the data from the US. The chart Parent Category Outcomes represents the PIVOT table. ![Parent Category_Outcomes](https://github.com/RuthLD/kickstarter-analysis/blob/main/resources/Parent%20Category_Outcomes.png) The parent category theater includes 525 successful, 349 failed, and 26 canceled campaigns. Overall, theater campaigns are successful based on this data. The outcomes were then evaluated by subcategory. ![Subcategory_Outcomes](https://github.com/RuthLD/kickstarter-analysis/blob/main/resources/Subcategory_Outcomes.png) The chart Outcomes by Subcategory represents the count of the successful, failed, and canceled Kickstarter by the three subcategories; musicals, plays, and spaces. Based on the chart, more Kickstarter for plays succeed than fail. These two charts helped answer the concern of whether Kickstarter is a good platform for a theater production campaign. The data indicated that most theater play Kickstarters were successful meaning it is good for this type of fundraising. The next step was to analyze the successful Kickstarter campaigns’ trends to develop an outline that mirrors them.

### Does the Launch Date influence Kickstarter Outcomes?
To answer the question of is there a reasonable period to launch a Kickstarter for a successful outcome, a PIVOT table was created with the rows indicating the launch month and the columns displaying the outcome. This PIVOT table excluded Kickstarters with a live outcome as they have not concluded. Two filters were used in the PIVOT table. The first was to filter by the parent category: theater. The second filter, years, was used to include data from every year in the rows by month. The chart Theater Outcomes Based on Launch Data was created from this PIVOT table. 
![Theater_OUtcomes_vs_Launch](https://github.com/RuthLD/kickstarter-analysis/blob/main/resources/Theater_Outcomes_vs_Launch.png)

### Does the Goal influence Kickstarter Outcomes?
To answer whether Kickstarter campaign’s goals influence outcomes, a new workbook was created to organize the information of total outcomes of the subcategory plays by goals. Twelve ranges for goals were created, as seen in the Kickstarter Goal Ranges image.
![Kickstarter_Goal_Range](https://github.com/RuthLD/kickstarter-analysis/blob/main/resources/Kickstarter_Goal_Ranges.png) Separate columns were made for the number of successful, the number of failed, and the number of canceled Kickstarters. The count for each column was calculated using the COUNTIFS formula. Then the column for the total number was created using the SUM formula. Three separate columns were made for the percentage of successful, failed, and canceled Kickstarters and calculated by dividing the count by the total number. The chart Theater Outcomes based on Goals was created from these percentages. ![Outcomes_vs_Goals](https://github.com/RuthLD/kickstarter-analysis/blob/main/resources/Outcomes_vs_Goals.png)

### Challenges
I encountered a challenge when creating the chart Theater Outcomes based on Goals. The chart initially produced did not reflect the correct dips and pikes. I realized that my calculated percentages were incorrect but that formula had no errors. I returned to the main Kickstarter worksheet to reassess the count columns. I realized I had not used greater or equal to in my original COUNTIFS formulas. ![Challenges](https://github.com/RuthLD/kickstarter-analysis/blob/main/resources/Challenges.png) 
My formula missed Kickstarters that had a goal of precisely 5000, 10000, 15000, and so on. I was able to fix the formula relatively quickly, and my chart showed the correct dips and pikes afterward.

## Results
### Theater Outcomes based on Launch Date
More Kickstarter campaigns were launched in May than in the other months. The month with the highest count of successful theater campaigns was May. However, May was also the month with the highest count of failed theater campaigns. In total, about two-thirds of the theater Kickstarters launched in May succeed, and one third failed. The second-highest number of Kickstarter launches occurred during June, and June had the second-highest count of successful Kickstarters. The second-highest count of failed outcomes occurred in October. A planned launch date in the fall would reduce the likelihood that the campaign would succeed. Based on the outcomes launching a theater Kickstarter in May or June would result in a larger pool of competing fundraisers, but there is a greater likelihood that the campaign will succeed compared to any of the other months.

### Outcomes based on Goals
The goal of a Kickstarter campaign with the subcategory plays dramatically affected the percentage of successful and failed outcomes. For example, Kickstarters with a goal below $4999 had a successful outcome between 76% to 73%, while Kickstarters with a goal between $5000 to $9999 were only 37% successful. That was a significant drop based on goal range. Theater plays Kickstarters with a goal between $10,000 to $14,999 had a successful outcome of 54%, and the successful outcome increases to 86% when the range increases to $15,000 to $19,999. Based on the data launching a Kickstarter for a theater play with a $10,000 or higher goal, is more likely to succeed than fail.

### Limitations of this Dataset
The most recent date included in the dataset is from March 2017. The dataset is almost five years old. The age of the dataset could limit how accurate the data is related to crowdfunding in the year 2021. The data sample size is over one thousand for plays, but that number may have increased in the past five years. There are several Kickstarters with goals of $1.00 that received much larger pledge amounts—the inclusion of these impact the percentage of successful outcomes of goals below $1000.

### Other Possible Comparisons
A table on the average donation and the percentage of outcomes would help identify how the two factors interact and how many donors are needed to reach the campaign goal. This could help the Kickstarter by suggesting an amount to a site visitor reading the fundraising page. Another table focused on the theater Kickstarters with a goal between $10,000 and $14,999, and the launch date may reveal more insights when the most successful outcomes are reached for that specific goal.
