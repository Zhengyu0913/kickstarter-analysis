# Kickstarting with Excel

## Overview of Project
Analyze a dataset consisting of 4000 crowdfunding projects to discover hidden trends.
### Purpose

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
I noticed the data in the launched date and deadline columns are not easy to read. They contain Unix timestamps, which measure time as the number of seconds since midnight of January 1, 1970. So I use this formula =(((J2/60)/60)/24)+DATE(1970,1,1) to convert it into a day/month/year format that we can easily read. And then use year() function to extract year for the following pivot table. I found successful projects and failed projects have the same trend over time after analyzing the pivot table.
### Analysis of Outcomes Based on Goals
I use countifs function to complete the outcomes based on goals table. In this formula =COUNTIFS(Sheet1!D:D,"<1000",Sheet1!F:F,"successful",Sheet1!Q:Q,"plays"), I set up three filter conditions to count the successful projects which have goal less than 1000 dollars and change these parameters according to the columns and rows. I found that the bigger the goal of crowdfunding,the lower the success rate, when the amount is under 25000.
### Challenges and Difficulties Encountered
I was confused about the countifs function when making the outcomes based on goals sheet. After searching some documents about it online, I finally mastered this countifs function in Excel
## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

1.We have most successful projects on May. After May, the successful projects are getting lower and lower.

2.There is no canceled project on Oct. Successful projects and failed projects have the same trend over time.

- What can you conclude about the Outcomes based on Goals?

1.The bigger the goal of crowdfunding,the lower the success rate, when the amount is under 25000.

2.When the amount of the goal is less than 1000, the success rate of projects is the highest.

- What are some limitations of this dataset?

1.We can not find the cost of these projects to evaluate the feasibility

2.We can not find the duration of these projects directly in the speadsheet.

- What are some other possible tables and/or graphs that we could create?

1.The line graph showing the relationship between percentage funded and categories.

2.The line graph showing the relationship between backers and time 

3.The line graph showing the relationship between backers and categories.