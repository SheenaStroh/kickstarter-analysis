# Kickstarting with Excel

## Overview of Project

### Purpose
After the completion of her play *Fever*, Louise has asked for an analysis of other Kickstarter campaigns and how well they
did based on their launch dates and funding goals. The following analysis was completed to review the data from Kickstarter 
theater ventures from 2009-2017. The outcomes of these ventures were reviewed with respect to launch date and goal to review any
correlations.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
To begin this analysis a pivot table of all available Kickstarter data was created and filtered by 
parent category and year launched. The parent category was set to "Theater" to ensure only the theater
data was being analyzed. The data was then broken down by outcome to assess how many were successful, failed, or canceled.
At this point ventures that were still live were filtered out of the data being analyzed. The following visualization was
created based on the filtered data. ![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/85318060/123525042-03ef3400-d683-11eb-9dc9-62c0e18813a9.png)


### Analysis of Outcomes Based on Goals
To complete this portion of the analysis a separate table was created which broke the Kickstarter data down by specific goal ranges.
The number of campaigns that were successful, failed, and canceled was tabulated from the parent data using the COUNTIFS() function
of Excel to filter by goal range, outcome, and the subcategory "plays". Then percentages were calculated using the collected data.
The following visualization was created based on this calculated data. ![Outcomes_vs_Goals](https://user-images.githubusercontent.com/85318060/123524976-9b07bc00-d682-11eb-9bf0-60160d381081.png)

### Challenges and Difficulties Encountered
As there is not a specific column for month launched, it was challenging to get the breakdown to show the outcomes by month. 
The date launched was entered into the pivot table as a row, and Excel automatically breaks it down by year, quarter, and then
month. It was a matter of removing the year and quarter fields from the rows, to leave only the months remaining.

Finding the total number of campaigns within the given goal ranges proved difficult, especially in the ranges that were between 
two different dollar amounts. Finding the number of campaigns above or below a single number was simple utilizing the COUNTIFS()
function, it took additional research to determine how to use the same function for the in-between values. In addition, copying the
formula across each data point was tricky due to Excel's predictive feature. Each time the formula was copied from one column to the
next it was necessary to go into the formula and manually change the criteria for the function to ensure the correct data was still 
being utilized.

## Results

- The most striking conclusion in the outcomes based on Launch date is that campaigns that were launched in May had a much greater success
rate than campaigns launched in any other month. The graph shows that not only is the overall number of successful campaigns greater, but
the difference between the successful and failed campaigns is much higher, meaning there is a higher likelihood of success. In addition the
data appears to show that the likelihood of a campaign being cancelled does not have much of a correlation to when it was launched.

- For the most part, campaigns that have a goal of less than $15000 are the most likely to be successful. There is an interesting spike in
the data from $35000 to $45000, and it could be useful to do further analysis in this area to see if there is any true correlation.

- For the outcomes based on launch date, we are looking at all of the theater projects together, there could be differences in the data if 
the all of the theater data was broken down by subcategory. Given additional time for analysis it would be useful to break down 
this data based on subcategory, as well, to see if there are any signficant differences. For all of the given data there was no 
statistical analysis complete, so there is also a chance of outliers or bad data that could be skewing the results. It would be beneficial
to perform some statistical analysis on all of this data, find standard deviations, IQR, and using that find any potential outliers to
get a fuller picture of what we are looking at. In addition most of the data from these datasets is from the
most recent years, which makes sense given when Kickstarter began, but it also means there are possibly a large number of live campaigns
that we don't yet know the outcome of, and those could also change the data. It would be interesting to add in the live data and compare 
results from years where most of the campaigns are complete to the years where there are still many live campaigns. Given more time, 
finding the outcomes of the live campaigns and integrating that data would also give a more complete picture.
