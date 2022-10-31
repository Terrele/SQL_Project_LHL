Answer the following questions and provide the SQL queries used to find the answer.

    
**Question 1: Which cities and countries have the highest level of transaction revenues on the site?**


SQL Queries: 

select city, country, SUM(totaltransactionrevenue) as rev
FROM session
WHERE city != 'not available in demo dataset'
GROUP BY city, country
HAVING SUM(totaltransactionrevenue) > 1
ORDER BY rev DESC
LIMIT 1



Answer:

"San Francisco"	"United States"	1564320000




**Question 2: What is the average number of products ordered from visitors in each city and country?**


SQL Queries:

select AVG(SKU.total_ordered), session.city, session.country from session
JOIN SKU ON session.productsku = SKU.productsku
GROUP BY session.city, session.country
ORDER BY avg desc



Answer:

319.0000000000000000	"Riyadh"	"Saudi Arabia"
319.0000000000000000	"Brno"	"Czechia"
250.5000000000000000	"Rexburg"	"United States"
189.0000000000000000	"Lisbon"	"Portugal"
189.0000000000000000	"Sacramento"	"United States"
159.5000000000000000	"not available in demo dataset"	"Hong Kong"
105.0000000000000000	"Kalamazoo"	"United States"
101.2500000000000000	"Saint Petersburg"	"Russia"
100.0000000000000000	"Avon"	"United States"
97.7500000000000000	    "Rome"	"Italy"


**Question 3: Is there any pattern in the types (product categories) of products ordered from visitors in each city and country?**


SQL Queries:



Answer:





**Question 4: What is the top-selling product from each city/country? Can we find any pattern worthy of noting in the products sold?**


SQL Queries:

select products.name, max(products.orderedquantity) as best, session.city, session.country from products 
JOIN report ON products.sku = report.productsku 
JOIN session ON session.productsku = report.productsku
JOIN SKU ON session.productsku = SKU.productsku
GROUP BY session.city, session.country, products.name
ORDER BY best desc




Answer:
Couldn't get distinct cities to work. The pattern is that Kick ball is the best selling product in multiple cities.




**Question 5: Can we summarize the impact of revenue generated from each city/country?**

SQL Queries:

SELECT SUM(session.productrevenue) as rev, country, city 
FROM session 
GROUP BY country, city
HAVING SUM(session.productrevenue) > 0
ORDER BY rev DESC


Answer:

295421666	"United States"	"not available in demo dataset"
120000000	"United States"	"Sunnyvale"






