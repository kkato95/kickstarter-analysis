# kickstarter-analysis
Data Analysis
  ## Overview of Project
  The Kickstarter Challenge dataset is a collection of donation campaigns that lists the donation's goals, the donations pledged and other data related to the donation campaigns. The analysis will be performed exclusively on the observations with the category “theater.” We analyzed over 1,393 “theater” donation campaigns that were labeled with 3 possible outcomes:
  1. Successful – surpassed the target donation goal
  2. Failed – did not meet the target donation goal
  3. Canceled – did not receive enough donations to continue campaign

  ## Analysis and Challenges
  
To begin our analysis of the subcategory “plays”, we created two new columns called “Date Created Conversion” and “Years.” The purpose of the Date Created Conversion was to convert the date format in “deadline” column into the short date format. The “Years” column is derivation of the “Date Created Conversion,” printing only the year into cell.
    
### Theater Outcomes by Launch Date Analysis
We will be analyzing how the number of successful, failed, and canceled outcomes, located on the y-axis, are related to the month the donation campaign began, located on the x-axis, for the observations of the category “theater”. 
The most successful donation campaigns for “theater” are at the end of Spring. By the end of the year the success wanes and the number of “successful” and “failed” outcomes match. As we can see in the graph, from March to April the number of successful outcomes is increasing quickly and maxes out at approximately 70% more “successful” campaigns than “failed” campaigns in May. Over the second half the year, success slowly drops equal with the failed outcome and to its lowest point all year in December. There are only a few “canceled” campaigns each month, if not 0, throughout the year.

- Challenges
One challenge encountered was formatting the “deadline” and “launch_at” column dates. In order to display a short date we had to convert this date to new units: =(((J526/60)/60)/24) +DATE(1970,1,1)
The formula essentially adds the elapsed time in seconds, which is represented by the deadline value, to the date 01/01/1970. The formula divides the deadline value (seconds) by 60 second, then divides by 60 minutes, then divides by 24 hours to generate the number of days and adds the numbers of days 01/01/1970 to generate the short date.
    
### Outcomes Based on Goals
We will be observing the percent successful, failed, and canceled outcomes and grouping them by their donation goal ranges located on the x-axis of the graph. Only observing the sub-category “plays.” We can see the 11 different intervals; We begin with the interval “less than 1,000”, then the intervals increase at increments of $5,000, until $50,000 is reached. The last interval is “greater than 50,000”. Using this graph below, we can visualize the percentage of outcomes as successful in blue and failed in green, as the donation goal amount is increasing on the x-axis.
When the donation goal is “less than 1,000” the outcome for the campaign is 77% successful. As we near the 20,000 goal the successful and failed percentages are narrowing till 50% of the campaigns fail and 50% succeed at 20,000. Interval 25,000 to 34,000 we are more likely to have a failed campaign than a successful one, with a failure rate of 80%. Once the goal is above 45,000, failure increases quickly.

- Challenges
Regarding the Outcomes Based on Goal graph, on the y-axis it shows the percentage of successes and failures out of the total number of outcomes. Because the graph is essentially a stacked line graph it will not distinguish the total number of successes, failures, and cancelations. Only shows the ratio to one another at each interval.

## Results
### Conclusions of the Theatre Outcomes by Launch Date
- Conclusion 1 - After analyzing the outcomes of the donation campaigns by month, the graph demonstrates that April and May are the best time to launch a donation campaign for the category theatre. The increase in successful outcomes trends up toward to end of Spring then trends down throughout the Summer and Winter.
- Conclusion 2 – Over the winter the total number of campaigns drop more than 50% to 75 total campaigns in Decemeber from a high of 166 in May indicating the holidays see a decrease in the demand for donations. The expenses of the holidays may reduce the disposable income, reducing donation activity.

### Conclusion of the Outcomes based on Goals
- Conclusion – Most campaigns with a goal of under $10,000 have high success rates, but as you approach 20,000 the success rate dwindles. This is likely due to the randomness of the donations being spread amongst the various campaigns evenly causing the campaign with a low goal more likely to be succesful. If a campaign made their goal high, like 30,000, then they will be unlikely to reach their goal. Why the success goes up after the 35,000 goal is exceeded? This could be due to a limitation of the graph. The graph does not show the number of campaigns at each interval. This can skew the graph because vast majority of the campaigns fall under the 10,000 goal. 

### Limitations of Data
- The limitation of the Kickstarter dataset lacks specificity in regards to when the donations were made. The whole analysis revolved around the start date and end date of the donation campaign. There may be many more nuances as to when donations are made and what may be driving donations. 
