# Kickstarting with Excel

## Overview of Project

### Purpose

Client requested an analysis of Kickstarter data in order better prepare for her upcoming play Kickstarter. Data set was obtained from Kickstarter.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date

To begin, the Launched_at column was converted from UNIX to a standard date format using the following equation. =(((X/60)/60)/24)+DATE(1970,1,1).
The year was then extracted into its own column using the YEAR() function.
The Category and Subcategory field was also used to create two new variables Parent Category and Subcategory to allow for more thorough filtering options.
A pivot table was then created using the entire data set and placed in the Theater Outcomes by Launch Date tab.
The count of success, failure, and canceled outcomes were then compared to the month that they were launched in with a filter applied to limit the analysis to Kickstarters in the theater category.  
![Theater_Outcomes_vs_Launch_pivot.png](https://github.com/justinkirk8/kickstarter-analysis/blob/main/Resources/Theater_Outcomes_vs_Launch_pivot.png)  
A pivot chart was then used to create a line graph with markers in order to visualize the date observed on the pivot table.  
![Theater_Outcomes_vs_Launch.png](https://github.com/justinkirk8/kickstarter-analysis/blob/main/Resources/Theater_Outcomes_vs_Launch.png)

### Analysis of Outcomes Based on Goals

A tab was created titled Outcomes Based on Goals.
A table was then created which split the totals of successful, failed, and canceled play Kickstarters into bins of under 1000, 1000 to 4999, and then 5000 bin increments up to 50000 and above. This can be seen in the image below.  
![Outcomes_vs_Goals_table.png](https://github.com/justinkirk8/kickstarter-analysis/blob/main/Resources/Outcomes_vs_Goals_table.png)  
The values of these cells were obtained using the COUNTIFS() function. An example of this code can be observed in the image above in the red box.
The total number of play Kickstarters were then calculated for each bin using the SUM() function.
The percentage of successes, failures, and canceled Kickstarter was then calculated by using a simple ratio equation. =[success/failed/canceled count]/[total count].
The data was the visualized in the line graph located below.  
![Outcomes_vs_Goals.png](https://github.com/justinkirk8/kickstarter-analysis/blob/main/Resources/Outcomes_vs_Goals.png)

### Challenges and Difficulties Encountered

The time units beginning in UNIX was a minor challenge since the time variables could not immediately be used.

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

When examining the Theater Outcomes Based on Launch Dates, the data suggests the following. In general, more theater Kickstarters succeed then those that fail. However, the ratio of success to failure is higher in the months of May, June, and July with May being the best. It should also be noted that there are more Kickstarters starting in these months which indicates a larger pool of competition in these months.

- What can you conclude about the Outcomes based on Goals?

Examining Play Outcomes Based on Goals indicates that the higher the goal amount, the less likely the Kickstarter is to succeed. Best results are observed at $5000 and below. The data does show a spike in 35000 to 39999, and 40000 to 44999, however, the sample sizes at these points are small and unreliable. 

- What are some limitations of this dataset?

One large limitation of this dataset is that it doesn't consider how well the individual marketed the Kickstarter. Did they do outreach on other social media? Was there description of the Kickstarter more than "I want to make this play, here is my blurb"?

- What are some other possible tables and/or graphs that we could create?

An analysis of Play Outcomes Based on Launch Dates could be useful to show that plays to show whether plays follow the same general trend as the overall plays. Reformatting the data and adding a month filter to the Play Outcomes Based on Goals would provide a single interactive excel graph to combine the two graphs provided in this analysis. Further examination into what the staff_pick and spotlight variables indicate. If this indicates the Kickstarter vetting and approving and results in more successful Kickstarters, then these Kickstarters could be examined further for successful traits. 
