# Project Name: Descriptive-Data-Analysis-With-PowerBI

![furniture-store](https://user-images.githubusercontent.com/108130729/181108393-45e9ff2d-0f77-4153-abd0-2c4acbc8a8d5.jpg)

----
# Project Objective: Problem Statement
An hypothetical Superstore in the U.S.A that majors in selling household and office furnitures, technology gadgets and office supplies have been facing significant but not-so-obvious revenue problems. The managers also feel as though, they are not taking full advantage of the very promising United States market.
Below are the 5 business questions that need to be addressed critically,
1. The management of Showtime superstores are concerned about the substantial figures of cost of production and carriages, they want a diagnostic of the causes.
2. They want to know the peak sales period in the last 4 years as the minimum sales periods and the factors behind both metrics.
3. They will like to rebrand in the area of shipping and delivery, they want to know which shipping modes are most patronized and most profitable, because there are theories that the company's shipping model is taking a huge chunk of the business capital.
4. Which States or Region are not performing up to expectations, supposedly to add to our total revenue?
5. Who are our most consistent and best customers per state?
----
# Data Sourcing
Got the dataset from a Microsoft learning platform which I registered and participated in. The program was called '30 days of learning'. The Following Data was Provided https://github.com/theoyinbooke/30Days-of-Learning-Data-Analysis-Using-Power-BI-for-Students/tree/main/Data%20Modelling%20Dataset
----
# Data Transformation
Got the dataset in XLS format primarily. It was in 'wide data' format.
I transformed it into a relational format such that each table can relate with one another with Excel by using Copy, Paste and 'Remove duplicates' functions. 
The sales table is the FACT table that keeps all the numeric data that may be aggregated in the report. 
The DIMENSION tables are customers, sales reps, location, product, they keep all our descriptive information that can slice data in the fact table

I finally imported the tables into power BI and did my remaining data cleaning and transformation on Power BI power query. Some of the cleaning steps i did include giving each column the appropriate data type, make some of the non-default first rows as headers, checked for any blanks and null values to make sure that our data was finally ready to be loaded to Power BI for analysis. 
I created another custom column to the sales table, “Days to Ship” which would help the business ascertain which shipping mode was most effective and most Profitable as part of the insights we hope to draw.

![powerquery](https://user-images.githubusercontent.com/108130729/180669669-b7417e5f-14ac-4e5e-9a86-5a32908d7e89.png)

First thing after successfully loading the tables to Power BI was to create relationships between the FACT table and the four DIMENSIONAL tables. Power BI recognized and created the relationships automatically. But there was one more crucial table left, 
“DATE TABLE” which would create dynamic date types for each unique transaction using DAX functions.

I created the date table using two primary DAX functions primarily ADDCOLUMNS and CALENDARAUTO consisting unique columns for YEARS, QUARTER, MONTH NAME and MONTH NUMBER.
Finally, I marked it as a date table for my model and the proceed to create a relationship with our fact table ‘Sales’.

![datetable](https://user-images.githubusercontent.com/108130729/180670285-b7389b7a-5fba-4ac0-9f91-dd2ef70a3092.png)

![Screenshot (47)](https://user-images.githubusercontent.com/108130729/180670296-fa7c034a-5980-44b1-8273-2a9b42192252.png)

Next step in the data transformation was to create Measures that will be crucial for our analysis.

•	Total sales 
•	Total Profit
•	Total cost
•	Profit Margin
•	Previous Period Sales
•	YOY % Change in sales

Total Cost wasn’t ascertained in the dataset so I had to use the Total sales and Total profit measures to calculate the total costs for the period.
Below are screenshots of the power of DAX as it was instrumental for me in solving a very crucial project problem of ascertaining sales of same date of the previous year (Used DAX function 'SAMEPPERIODLASTYEAR') which is very important in computing and visualizing how sales changed from past year. This Measure could easily tell us the percentage increase or decrease in sales by year, I used the 'IF' statement and 'HASONEVALUE' here.

Previous Period Sales
![prevpresales](https://user-images.githubusercontent.com/108130729/180670743-9f7b7d16-99e7-45a0-a175-b89c4393913e.png)
Year on Year Change in Sales
![yoy](https://user-images.githubusercontent.com/108130729/180670754-6278a576-7981-4073-b738-3f5f7e96f3fa.png)

# Results of Analysis
I built a user friendly homepage using buttons and inserted textboxes to help stakeholders navigate through my findings seamlessly in the resultant Power BI file while trying to interact with my reports.

![Screenshot (71)](https://user-images.githubusercontent.com/108130729/181114638-2fb4bf6e-2838-447e-8e82-cc7917062e74.png)

Below is my final dashboard which at first look will give my stakeholders insights of my comprehensive reports

![Screenshot (165)](https://user-images.githubusercontent.com/108130729/201121051-a9c4eb91-9cfb-4f31-bdcb-fcd7f2b3fb8c.png)

Sales Performance and Profitability

![Screenshot (167)](https://user-images.githubusercontent.com/108130729/201130859-0611db7c-8577-40df-86be-78f3268e5c28.png)

Comprehensive Insights

![Screenshot (166)](https://user-images.githubusercontent.com/108130729/201131004-2f2eab31-aba1-442c-a8ba-1abd73daf7ba.png)

Other visualizations generated to help address the business problems

![Screenshot (158)](https://user-images.githubusercontent.com/108130729/201121417-907f25db-1d01-465c-9570-69ef5c18e303.png)

![Screenshot (159)](https://user-images.githubusercontent.com/108130729/201121433-662df099-2eb4-49dd-b238-819ea9e7e6d4.png)

![Screenshot (160)](https://user-images.githubusercontent.com/108130729/201121485-d96a66f9-5184-4622-8178-acf74729bbdb.png)

![Screenshot (161)](https://user-images.githubusercontent.com/108130729/201121591-104c6dee-682a-4789-9df5-3a3258c1cf35.png)

![Screenshot (162)](https://user-images.githubusercontent.com/108130729/201121630-dca6fe25-ba78-46d4-83ae-e874730219e5.png)

![Screenshot (163)](https://user-images.githubusercontent.com/108130729/201121703-fd727aa2-062d-402b-8820-c86496b3a962.png)

One Challenge was sorting months in chronological order in this line chart during visualization, What I did was to switch off concatenate labels and use sort by column functions, with the use of Month number in my Date table which was created earlier, It really came in handy.

# Recommendations

•	The marketing department needs to step up their activities in the highlighted states with eye catching vogue advertisements on-net and offline. Sales are far below expectations and surprisingly there is a growing market for our products in those states.

Effective sales promotions should also be considered but in line with the department's budget because the business needs to generally cut actual costs going forward as against budgeted costs.


•	The big reveal in the cost analysis is that Furniture, one of the 3 categories of products has been a big burden on our revenue. Possibly costs of carriages/shipping, loading, sales team float need to be looked into as all these furniture costs accounts for 36% of our overall costs, but only yielding 3% return on investment over the 4 year period.
The establishment furniture products are also responsible for a 1.7% loss in the central region of the country in the last 4 years, 2.8% and 1.5% losses in the central and southern regions respectively in the immediate past year 2017. 

I suggest that there is a need to stop outsourcing carriages to shipping companies and logistic agencies, the time has come to set up a logistics department subservient to the company, this will help reduce costs and maximize profit 


•	The sales trend over the last 4 years show that November is our peak sales period in the last 5 years while December is a close second. They both account over 30% of our total revenue in a 12 month calendar. Major cause of this has to be our target customers preparing for the new work year, most technology gadgets are launched in those periods and lastly for our furniture products, there is always a wave of people moving to new homes and apartments in anticipation of a fresh year. Another contributing factor is the influx of winter session international students and immigrants in America in November and December.

Going forward, The store needs to beef up staffing by employing short term employees to reduce backlog of orders as we have found out in this analysis engagement.
February being the lowest in sales in our trend analysis probably has to do with it being a 28 days month.

# I Appreciate you taking time to give my analysis a read.

# You can connect with me on
https://twitter.com/KamalBI_ and ktaiwobiz@gmail.com
