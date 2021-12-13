# Module 1 Challenge
Analysis on kickstarter campaigns.

## Overview of Project
The purpose of this analysis is to analyze kickstarter campaigns all across the world to help identify what factors lead to successful and failed campaigns. After viewing the data, one will be able to determine the appropriate times to launch a kickstarter campaign. Furthermore the data can be filtered to such a fine degree that we will be able to view the subcategories (plays, documentaries, television, etc.) of kickstarters to aid us in any decision making process. 

### Analysis and Challenges
The first part of this challenge was to analyze theater outcomes by their launch date. To do this, we created a pivot chart based off of the data in the Kickstarter sheet and added this pivot chart to a seperate sheet and named it "Theater Outcomes By Launch Date". 

Since we were only concerned about outcomes for the parent category of *theaters*, I made sure to include the parent category in the filters section of the PivotTable Fields. This allows us to only see data on kickstarters for theater fundraisers. We also put "Years" in the filters section of the PivotTable Fields so that we could view the data by their respective months. 

In order to have the PivotTable show data by months, once we added "Date Created Conversion" to the Rows field, two more fields will populate automatically in the Rows field. These fields are "Years2" and "Quarters". Since we only want to view the data by the month it was launched in, we clicked and dragged both "Years2" and "Quarters" out of the field so that only months will show. 

Now that our pivot table is showing data by the month, we add "outcomes" to both the Columns field and the Values field. This will populate our pivot table and give us the data we need so that we can view all of the successful, failed, and canceled kickstarter campaigns for **theater** fundraisers. Once we are finished our pivot table should look like this:

 ![TheaterOutcomesPTChart](https://user-images.githubusercontent.com/95515322/145733130-fca2f7eb-d355-436a-ae02-4afbd16799fb.png)

The final step with our PivotTable is creating a Line Chart. In order to do so, we put our cursor in one of the cells in the pivot chart, go to the ribbon in Excel and click insert, and finally we click the down arrow next to the line chart button and select the first line chart displayed.

#### Deliverable 2: Outcomes Based on Goals Charts
The second part of this challenge was to filter our data from the Kickstarters sheet to show us how successful these fundraisers were based off of the goal they had set. We categorized the goals by the amount of money they targeted to raise, starting at "less than a $1,000" and moving up by $5,000 each row until we hit "$50,000". See below for a visual: 

![OutcomesBasedOnGoals$Rows](https://user-images.githubusercontent.com/95515322/145733389-3a65d487-c7e3-40e2-b90e-81f71b83cdfa.png)

The first challenge I ran into during this analysis was finding an accurate count for each row. When I first attempted the COUNTIFS formula, I thought if I filtered the original sheet for Kickstarters I would not have to add filters into my COUNTIFS formula. This proved to be wrong as my data showed to be inaccurate. After realizing I would have to add extra subsets to my COUNTIFS formula, I added in an extra criteria for the outcome which was based on row "F" and had the formula look for the respective result I was looking for (successful, failed, or canceled). The last criteria told the formula to only count subcategories that had "plays" in the cell. My formula looked something like this: 

![COUNTIFS1000Formula](https://user-images.githubusercontent.com/95515322/145733881-f803d380-3eff-46c0-ae9d-13eb2529fb2a.png)

##### Results
When viewing the data from our **Theater Outcomes by Launch Date** sheet, the first outcome that comes to mind is that the best time to start a fundraiser and it end up being successful is in May. May had the highest amount of successful kickstarters, 11 more than the next highest which was June. The summer months of May, June, and July proved to be the best season to launch a kickstarter. 

The second outcome I learned from this data set is that the worst time to launch a campaign for theaters is in October. While it wasn't the lowest point for "successful" campaigns, October was still in the bottom half of successful campaigns. The main reason why I feel that October is the worst month to launch a campaign is because October also had the highest amount of "failed" kickstarters. In my opinion this combination proves to be too unsuccessful and it would be best to avoid this month. The winter months of November, December, and January proved to be a bad time to launch a campaign. 

![Theater_Outcomes_Vs_Launch](https://user-images.githubusercontent.com/95515322/145734265-102adbcc-38e1-447a-ad82-29157c1fda7d.png)

When looking at the **Outcomes Based on Goals** data sheet, the first conclusion that comes to mind is that any goal between $45,000 and $49,999 is a waste of a campaign. This goal proved to have a 0% success rate and a 100% failure rate. This seemed odd that there weren't any successful goals in this range considering there were 2 successful campaigns that had goals above $50,000. 

![Outcomes_Vs_Goals](https://user-images.githubusercontent.com/95515322/145734409-0599de52-06cd-47bd-8ab6-e887e0061c0e.png)

One limitation I found with this data set is that it only goes back to the year 2009 for Kickstarter Campaigns. This does not give us a lot of years to gather data, and could limit the conclusions we find. 

Another graph that I thought could help us visualize this data would be a bar graph. Both analyses of "outcomes by date" and "outcomes based on goals" would work well visualizing this data on a bar graph. 


[Kickstarter_Challenge.xlsx](https://github.com/jacoblgarrison/Module_1_Challenge/files/7700129/Kickstarter_Challenge.xlsx)
