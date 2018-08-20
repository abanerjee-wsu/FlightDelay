# Digitas Data Science: Take-Home Case

This case is designed to be a brief examination of your skills. Please complete problem A using an open-source software package, such as R or Python, and complete problem B using a SQL standard of your choice in your solutions. Please also submit all of your work, including code and commentary, via a single PDF file.

Note: This document and any supporting materials are STRICTLY CONFIDENTIAL. Do not copy, share or discuss any of these materials or your work with anyone.

## **A.** Flight Delays
A large travel agency has asked us to predict whether a ﬂight will be canceled based on several factors. The agency can sell tickets for only three airlines (AA,UA, and DL) and would like to be able to advise its customers on which airline has the least risk of cancellation. Using the dataset provided:
1. Build a model to predict whether a flight will be canceled.
2. Write your own function that uses the model output to predict whether a future ﬂight will be canceled.
3. Provide fully commented code and model output for your analysis.
4. Provide a recommendation on which airline is most reliable.
5. Use the ppt template provided to create a few slides (10-15 minutes of content) - assume content will be used to present to client (travel agency). Client is non-technical, but wants to understand not only the recommendations but also how you arrived at such recommendations.  

The dataset includes the following fields.

Field            | Name Type | Description
-----------------|-----------|----------------------------------
Canceled         | Binary    | Canceled = 1
Month            | Integer   | Jan = 1
DepartureTime    | Integer   | Military Time (1:00 PM = 1300)
UniqueCarrier    | String    | Airline Carrier Code
SchedElapsedTime | Integer   | Scheduled Flight time in minutes
ArrDelay         | Integer   | Arrival delay in minutes
DepDelay         | Integer   | Departure delay in minutes
Distance         | Integer   | Distance in miles

## **B.** SQL Assignment

You are presented with sample rows of the following 3 tables:

**Table1: purchases**

visitor | transaction 
--------|-----------
Mary 	| 120   
Mary    | 98   
aaron   | 70   
henry   | 153   
Amy     | 10   
...

**Table2: demos**

name    | age 
--------|-----------
Mary 	| 26
Mary    | 26   
alice   | 29   
alice   | 32   
henry   | NULL   
...

**Table3: fraud**

visitor |  
--------|
bill 	|	
Ella 	|   
...   


There are some data quality issues, so you’ll have to be careful when handling data. The following apply to all of the questions that follow.
1. First, there are some duplicates in the “demos” table, so if someone has multiple age entries, use their max age. 
2. There are also people with no listed age (NULL), or who do not appear in the “demos” table, which you will need to keep in mind.
3. Finally, some visitors committed fraud (those listed in the “fraud” table), in which case we don’t want to use their data in either of the following questions.

Note that the visitor column is referred to as name in the “demos” table.

You may use a SQL standard of your choice in your solutions. If unsure about any specifics in the data or the questions, make assumptions as needed and note them in your solutions.

Questions:

1. 

In order to understand the demographic of visitors, output a distribution of age by % of total visitors (i.e. for each age, what % of the total population is that age?). Do not include NULLs/missing ages in your calculation and output. 

Also, since many ages might appear infrequently in the data, only return those ages that appear at least 5% in the population.

2. 

Create a table that shows the mean of transactions per visitor in the “purchases” table, but only for those visitors who begin with the letter A (in uppercase or lowercase), for example aaron and Amy (assuming neither of them committed fraud). 

Also, add an indicator (0/1) column that indicates whether the visitor had at least one single transaction of over 100 (For example, Mary would be assigned a 1 for this column, as she has at least one transaction over 100.)

Return this table sorted by the mean of transactions in descending order, showing only the top 10 results.


