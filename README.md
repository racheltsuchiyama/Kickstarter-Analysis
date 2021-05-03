# An Analysis of Kickstarter Campaigns
Louise started a Kickstarter campaign for her play, and wanted to determine the success of her campaign compared to other plays. Specifically, she wanted to compare how the launch dates and funding goals effected the outcome of the various plays. Therefore, I created a visualization to showcase the success, failure, or cancellation of the theater productions depending on their start dates. Then, I created another chart to display the success, failure, or cancellation of plays depending on their funding goals.
## Analysis Performed
### Theater Outcomes by Launch Date
To look at just the theater Kickstarter campaigns, I created a pivot table and filtered the data such that only the theater campaigns were included. The columns of the pivot table were the possible outcomes of the campaign: successful, failed, and canceled. The rows of the table contained the number of outcomes for each month. The resulting table is displayed below.
<img width="326" alt="Screen Shot 2021-05-02 at 7 53 39 PM" src="https://user-images.githubusercontent.com/83552696/116837639-1caa0480-ab80-11eb-88c5-7316beed551c.png">
This table was summarized into a marked line graph.
### Outcomes Based on Goals
To determine how the funding goal effected the outcome of the plays, I utilized the COUNTIFS excel function. First, I specified monetary ranges of about $5000. Then, I counted the number of successful, failed, or canceled plays within each range using the following code:
  =COUNTIFS(Kickstarter!$F:$F, "successful", Kickstarter!$D:$D, "<1000",  Kickstarter!$R:$R, "plays")
I converted the number of each outcome into percentages by dividing them by the total projects (sum of outcomes for each range) and multiplying by 100%. Then, I put this analysis into a line graph with the x-axis as the goal ranges and the y-axis as the outcome percentages. 
The COUNTIFS function could have resulted in inaccurate information if the columns were not locked.

## Results
