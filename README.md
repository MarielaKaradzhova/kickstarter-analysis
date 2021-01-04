# Kickstarting with Excel

Performing Various Analyses on Kickstarter Data to Uncover and Visualize Trends

## Overview of Project
Louise is an up and coming playwright who wants to start a crowdfunding campaign to help fund her play “Fever”. She has already estimated a budget of over $10000, but she’s hesitant to jump into her first crowdfunding campaign. 
### Purpose
The purpose of this project is to help Louise set up her first crowdfunding campaign. Using Excel to analyze and visualize current site data, I will help her gain a greater understanding of campaigns from start to finish. With the help of my analysis, she will be able to achieve a favorable outcome for her first crowdfunding campaign by replicating other successful ones in the same category. 
## Analysis and Challenges
I used Excel to organize, sort and analyze crowdfunding data to determine whether there are specific factors that make crowdfunding campaigns successful.
### Analysis of Outcomes Based on Launch Date
The purpose of this analysis was to find out which kickstarter campaigns were successful based on their launch date. To do that, I had to initially convert the timestamped values from the "date created" column to a date format into a new column named "Date Created Conversion". Using the "YEAR()" function, I extracted the year from "Date Created Conversion" into a new column "Years". To organize the data and be able to visualize my analysis, I created a pivot table where I placed the "Date Created Conversion" in "Rows", the "Outcomes" in "Columns", the "Count of Outcomes" in "Values", and the " Parent Category"/"Years" in "Filters". Once the pivot table was complete I adjusted the "Parent Category" filter to show just the "Theather" category. I also adjusted the column labels to only show "Successful", "Failed" and "Canceled" campaigns which I then sorted in descending order since I am most interested in the "Successful" campaigns. Finally, I removed the "Years" and "Quarters" fields from the "Rows" area because I wanted my pivot table to show the month in the rows labels, which made my line chart easier to read.

Below is the line chart I created to visualize the relationship between the outcome categories of  "Successful", "Failed", or "Canceled" projects on the x-axis and the month representative of their launch date on the y- axis.

![Theather_Outcomes_vs_Launch](path/to/Theater_Outcomes_vs_Launch.png)

### Analysis of Outcomes Based on Goals

The purpose of this analysis was to find out how many campaigns were successful in relation to their goal amount. To perform the analysis I created a new sheet in the Kickstarter workbook labeled " Outcomes Based on Goals", with columns:
- Goal
- Number Successful
- Number Failed
- Number Canceled
- Total Projects
- Percentage Successful
- Percentage Failed
- Percentage Canceled

In the "Goal" column I grouped the projects based on their goal amount with the following dollar-amount ranges:
- Less than 1000
- 1000 to 4999
- 5000 to 9999
- 10000 to 14999
- 15000 to 19999
- 20000 to 24999
- 25000 to 29999
- 30000 to 34999
- 35000 to 39999
- 40000 to 44999
- 45000 to 44999
- Greater than 5000

To populate the number of "Successful", "Failed", and "Canceled" campaign columns I used the "COUNTIFS()" function by filtering on the Kickstarter "outcome" column, on the "goal" amount column,  using the goal amount ranges I created. I then filtered the "Subcategory" column set to only "plays" as the criteria.
The next step was to populate the "Total Projects" column with the number of "Successful", "Failed", and "Canceled" projects for each row by using the 'SUM()" function. After that, I calculated the percentage of "Successful", "Failed", and "Canceled" projects for each row using the "SUM()" function , divinding each category by the total amount of projects respectively.

Finally, I created a line chart which is inserted below, to visualize the relationship between the goal-amount ranges on the x-axis and the percentage of "Successful", "Failed", or "Canceled" projects on the y-axis.

![Outcomes_vs_Goals](path/to/Outcomes_vs_Goals.png)

### Challenges and Difficulties Encountered

This dataset was easy to work with, however one challenge I encountered when filtering data was getting a reoccuring error of "#DIV/0!". I quickly overcame this challenge by using the "IFERROR" functing to replace the value with 0 in cells containing the error. This easy fix cleaned up the data I was working with and made it easier for me to read and understand what the problem was that I initially encountered. 
## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

The first conclusion is that the most successful camppaings were launched during the month of May. Therefore, Louise has a higher chance of launching a succesful campaign in May, compared to all other months of the year.

The second conclusion is that December is not a good time to launch a campaign since the lowest point of the succesful campaigns category was during that month. Louise should wait for another time to launch her campaign, since the data shows she will have the lowest chance of kickstarting a succesful campaing in December. 


- What can you conclude about the Outcomes based on Goals?

The results of the analysis on Outcomes based on Goals show that there is a 50% chance of campaings being successful or failed, which may indicate that there are other factors other than the goal, which determine the success of a kickstarter campaign. As shown in the line chart, the number of successful campaings mirrors the number of failed campaigns, where 20% of successful campaings with a goal of $25000-$29000 is mirrored by %80 of failed campaings with the same goal. Another example to note is the results of successful and failed campaings with a goal of $45000-$49999, where 0% were successul and 100%  were failed. These results indicate that the goal may be too high for a kickstarter campaign and that Louise should be mindful of the effects that a higher goal amount may have on the success of her kickstarter campaing.

- What are some limitations of this dataset?
One limitation of this dataset is the source of kickstarter campaings. It would be helpful to collect data from sources such as social media which may influence the results from the analysis above. 
?
