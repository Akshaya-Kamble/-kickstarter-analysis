# Module 1 challenge : Helping Lousie with the Analysis

## Overview of Project
	Lousie is interested to know how different campaigns fared in relation to their launch dates and their funding goals.
	For theater outcomes vs the launch dates,pivot table is generated and this pivot table is used further to make pivot chart for visulizations. 
	The conclusions from theses visulizations helped Lousie to know which months are good for launching successful events and which months have less successful events.
	For the plays outcomes based on goals,a table is created with required fields and a line graph is made for visulization. The conclusions helped Lousie know
	the relationship between the play outcomes and the goal ranges.
	Using the above fiters, pivot tables, charts and graphs Lousie will be able to get better insights of the data and will be able to use them to plan for future
	events considering the launch dates and goal ranges for Theater and plays.
	
### Purpose 
	The purpose of this Project is to help Lousie find the outcomes based on launch dates for the theater category and find the outcomes based on goals for plays 
	category. By end of the project using different methods of data filtering, sorting and visulizations Lousie will be able to make conclusions and can use them 
	for future plannings.


## Analysis and Challenges
### Analysis of Outcomes Based on Launch Date
#### Steps for getting data ready for visualization using pivot table and pivot chart. 
	- Rename the file to Kickstarter_Challenge.xlsx
	- Created folder named "resource " to store PNG files.
	- Added a year colum to our kickstarter data using the year()
	- Created pivot table on a new sheet"Outcomes Based on Launch Date."
	- Filtered the pivot table based on "Parent Category" and "Years."
	- Filtered the column labels to show only "successful," "failed," and "canceled."
	- With excel version 365 the date was already grouped and so deleted the days and quarters to get the data in months.
	- Filtered the "Parent Category" to show only the data for "theater."
	- Sorting the campaign outcomes in descending order.
	- This pivot table is now ready to be used for getting our visulizations using line chart.
	- Created the line chart with months on x axis and number of outcomes on the y axis. 
	- Image named Theater_Outcomes_vs_Launch.png available in resource folder.

#### Outcomes of the analysis
	1.The blue line indicates successful events and is at a peak in May with a count of 111.May and June have the most successful events and is a good time to launch 
	the theatre events.Whereas December has the least number of successful events that is 37 and is not a good time to launch theatre events.This concludes that
	the launch date can be considered as a factor for successful events and can be used for planning future events.
	2.The orange line represents the failed events.The failed events have been in a range of 31 to 52 per month and have been in a similar pattern throughout the year.
	This concludes that the launch date did not affect the failed events.
	3.The gray line indicates canceled events.This line has also been in a range of 1 to 7 per month and has followed similar pattern throught the year.
	This concludes that launch date did not affect the cancelled events.
	4.The final conclusion is that the launch dates can be used for planning successful events.	

### Analysis of Outcomes Based on Goals
#### Steps for getting data ready for visualization using tables and graphs. 
	- Created new sheet named "Outcomes Based on Goals."
	- Created titles for each column naming Goal,Number Successful,Number Failed,Number Canceled,Total Projects Percentage Successful,Percentage Failed,Percentage Canceled,
	- Filled goal column with ranges.
	- Using the COUNTIFS() Populated the "Number Successful," "Number Failed," and "Number Canceled" columns by filtering on the Kickstarter "outcome" column,
	  on the "goal" amount column using the ranges, and on the "Subcategory" column using "plays" as the criteria.
	  Using this function =COUNTIFS(Kickstarter!$D:$D,">=1000",Kickstarter!$F:$F,"=successful",Kickstarter!$R:$R,"plays",Kickstarter!$D:$D,"<=4999")
	- Used $ for the range reference cell to make this data constant for all the required calculations.
	- Changed the range numbers for every cell.
	- Using SUM() populated the "Total Projects" column with the number of successful, failed, and canceled projects for each row.
	- Calculated the percentage of successful, failed, and canceled projects for each row by diving the event(successful,failed,canceled) by 
	the total no of events and using the % sign.
	-With all the required data available created a line chart with the goal amount range on the x axis and percentage of successful, failed, or canceled projects on the y-axis.
	- Image named Outcomes_vs_Goals.png available in resource folder.

#### Outcomes of the analysis
	1. The blue line indiactes percentage successful events.388 events were successful when the goal was 1000 to 5000 that is 73% successful events and the number 
	of events were also reduced as range of goal increased.This concludes that smaller range of goal had more successful events.
	2.The orange line indicates percentage failed events. 146 events failed in the same range of 1000 to 5000 that is 27 % ,Similarly the number of events also
	 reduced as range of goal increased.This concludes that smaller range of goal had more failed events.
	3.The successful and failed events cannot be determned by the goal range but the outcome is inversely proportional to the goal range can be concluded.


### Challenges and Difficulties Encountered
	This is with reference to deliverable 2 : Analysis of Outcomes Based on Goals
	1.  While using COUNTIFS() to calculate the number of successful events,the same COUNTIFS ()function had to be copied for every cell in the 
	column and editted on the range of goal. This was a challenge for this data set and could be an even bigger challenge when there are more 
	number of rows.
	2. Another challenge was that the same COUNTIFS() is required to populate the data for failed and cancelled events. The copy and paste does not give 
	required results because the refrence to all the columns is shifted to one column ahead and wrong answers are generated. 
	Eg : When using COUNTIFS() the criteria used for successful events is
	" =COUNTIFS(Kickstarter!D:D,"<1000",Kickstarter!F:F,"=successful",Kickstarter!R:R,"plays")"
	and for failed events these can be coppied as all the reference columns we need (goal,outcomes,subcategory)are same and outcomes can be 
	eddited changing the second criteria to "failed" and we get
	  "=COUNTIFS(Kickstarter!E:E,"<1000",Kickstarter!G:G,"=failed",Kickstarter!S:S,"plays")"
	As we see here after the copy and paste the cell references are changed (D to E,F to G,R to S) so in order to fix this challenge we can make the 
	cell references as constant by adding "$" in front of the cells and it can be copied now.
	After copying this function the paste will look like 
	"=COUNTIFS(Kickstarter!$D:$D,">=1000",Kickstarter!$F:$F,"=successful",Kickstarter!$R:$R,"plays",Kickstarter!$D:$D,"<=4999") "
  	
## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
	1. May and June have the most successful events and is a good time to launch the theatre events.
	2. Whereas December has the least number of successful events and is not a good time to launch theatre events.

- What can you conclude about the Outcomes based on Goals?
	The final conclusion is that the number of events are reduced as the goal range increases.They are inversely proportional.

- What are some limitations of this dataset?
	1. The range for goal column had to be written manually for each cell.
	2. The criteria for COUNTIFS() had to be copied and eddited for the required outcomes in each cell.
	3. The copy for COUNTIFS() did not work until the reference cells were made constant.


- What are some other possible tables and/or graphs that we could create?
	Attached 2 images for recommendation, named Theater_Outcomes_vs_launch_recommendation.png and Outcomes_vs_Goals_recommendation.png in the resource folder.

 
