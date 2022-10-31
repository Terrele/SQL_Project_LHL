Question 1: Starting with the first question: Question 1: Which cities and countries have the highest level of transaction revenues on the site?, I have found the city and country with the highest level of transaction but are there any duplicates which caused it to have the highest?

SQL Queries:

select fullvisitorid, city, country, totaltransactionrevenue
FROM session
WHERE city = 'San Francisco' and country = 'United States' and totaltransactionrevenue is not null

Answer: 

As we can see, the fullvisitorid are all distinct values so there are no duplicate totaltransactionrevenues.


Question 2: 

SQL Queries:

Answer:



Question 3: 

SQL Queries:

Answer:



Question 4: 

SQL Queries:

Answer:



Question 5: 

SQL Queries:

Answer:
