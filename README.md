# Practical Exam: Sample SQL Associate

Tech Solutions Inc. is a leading technology company specializing in software development and IT consulting services. The company prides itself on delivering innovative solutions to clients across various industries. With a dedicated team of skilled professionals, TechSolutions has earned a reputation for excellence in the tech industry.

Tech Solutions Inc. has been experiencing a decline in customer satisfaction ratings over the past few months. Customer feedback surveys and support tickets indicate an increase in dissatisfaction among clients. The company is concerned about this trend as it directly impacts customer retention, reputation, and overall business growth.

You are working with the customer support team to provide data to managers to help the company take proactive measures to address these concerns effectively. 

## Data

The following schema diagram shows the tables available.

<img width="415" height="289" alt="data" src="https://github.com/user-attachments/assets/0ad82990-6b10-4f53-b50b-90ee0ca9319d" />





# Task 1

Before starting any analysis, we need to confirm that the data is accurate and reflects what you expect to see. 

It is known that there are some issues with the `support` table, and the data team have provided the following data description. 

Write a query to return data matching this description. You must match all column names and description criteria.

| Column Name | Criteria                                                |
|-------------|---------------------------------------------------------|
|id | Discrete. The unique identifier of the support ticket. </br>Missing values are not possible due to the database structure.|
| customer_id | Discrete. The unique identifier of the customer. </br>Missing values should be replaced with 0.|
| category | Nominal. The gategory of the support request, can be one of Feedback, Billing Enquiry, Bug, Installation Problem, Other. </br>Missing values should be replaced with Other. |
| status | Nominal. The current status of the support ticket, one of Open, In Progress or Resolved. </br>Missing values should be replaced with 'Resolved'. |
| creation_date | Discrete. The date the ticket was created. Can be any date in 2023. </br>Missing values should be replaced with 2023-01-01. |
| response_time | Discrete. The number of days taken to respond to the support ticket. </br>Missing values should be replaced with 0. |
| resolution_time | Continuos. The number of hours taken to resolve the support ticket, rounded to 2 decimal places. </br>Missing values should be replaced with 0. |





# Task 2

It is suspected that the response time to tickets is a big factor in unhappiness.

Calculate the minimum and maximum response time for each category of support ticket. 

Your output should include the columns `category`, `min_response` and `max_response`. 

Values should be rounded to two decimal places where appropriate. 




# Task 3

The support team want to know more about the `rating` provided by customers who reported `Bugs` or `Installation Problem`s. 

Write a query to return the `rating` from the survey, the `customer_id`, `category` and `response_time` of the support ticket, for the customers & categories of interest. 

Use the original support table, not the output of task 1. 
