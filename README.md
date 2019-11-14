# HandUpAmerica Dashboard

## Overview
This is the repository for a project in which I created an Excel dashboard to help drive business decisions for a fictional nonprofit using income tax data. 

## Project Takeaways
This dataset pushed me harder than any I had worked with before due to the number of columns and how separated the data was. Having to pluck out one cell in every 11 was a mental exercise I hadn't done before and I am better for having done it.   
I am extremely grateful that I set my sights high and really committed to creating a zero-scroll dashboard because it forced me to go learn something new: array formulas. Not just Vlookup, not just index/match, but index-match-match to use multiple indices to define my searches.  
I also had not really worked with data validation dropdown menus and they really helped make my dynamic maps and charts work. It's a useful tool and one I won't forget. It's easy to overlook them when a fancy slicer is available but I plan to use it regularly from now on.  

## The Pitch
You have been tasked with creating an interactive dashboard for an organization that provides assistance for low income and elderly taxpayers. You have been asked to create this dashboard using the 2016 IRS individual tax return data provided.

Minimally, the organization (Hand Up America) wants to be able to see the following information for each state as part of the dashboard:

 - What percentage of tax returns filed are elderly returns? Include a plot showing the states with the ten highest percentage of elderly returns.

 - How does the distribution of single, joint, and head-of-household returns filed differ by income bracket? How does this compare to the national picture?

 - How do active vs passive sources of income differ for each income bracket?
 - Add any other charts or visualizations you think might help guide the decision-making at HUA.
 
## The Data
We used data from the IRS 2016 income tax. This included all income tax data for the entire US, data for each state individually, and data for US territories.

## Approach to the Problem
With a deliverable that was both specific and vague, I first worked through finding the underpinnings for my dashboard. These included:
 - Created a table containing the state names, the number of total returns filed, and the number of elderly returns filed.
 - For each state, calculated the total tax liability per person. (Used the number of exemptions as a proxy for the number of people in the household). *Note that tax liability is given in thousands of dollars.* Create a map to illustrate top and bottom 10 states.
 - Pull the list of top 10 states with the highest percentage of < $1 tax returns. Do this also for the highest percentage of > $1,000,000 returns.

 After performing this analysis, I planned out my dashboard. I decided I wanted to confine the dashboard to the visible screen without requiring scrolling. To this end, I figured out that I could combine my charts to 2 types: State data compared to national data, and groups of 10 states plotted on a map (such 10 states with the highest tax liability). I created a pull table for each of these using array formulas(Index-match-match) so that I could display all the info for groups of 10 states on a single dynamic heatmap, and State VS national on a combination chart. I then created supplemental visualizations to help interpretational and comprehension, like a written list of the maps displayed on the heatmap, as well as an at-a-glance bar chart that provided a very simple relationship touchstone. I rounded it out with a custom logo (created in canva)and a basic Venn diagram to highlight my recommendations and the reasons I chose those states.
