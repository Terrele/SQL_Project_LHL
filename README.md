# Final-Project-Transforming-and-Analyzing-Data-with-SQL

## Project/Goals
This is my SQL project

## Process
### (Step 1)
1. Import csv to pgadmin

### (Step 2)
2. Do a data cleaning. 

### (Step 3)
3. Answer questions in starting_with_questions

## Results
During data cleaning, I have done the following:
1. Divided the productprice in session by 1,000,000 since the values did not make sense.
2. I removed the columns searchkeyword, productrefundamount, itemquantity, and itemrevenue from the table session since the entire column was null. Also removed the column userid from the table analytics since it was null.


This data could tell you which products were the best selling in each country and city, what was most profitable and which products did not sell.

## Challenges 
It was difficult to import data from excel to pgadmin due to syntax errors or character limits without it showing what kind of error has caused it. The best way was to use the copy function and it would show what kind of error happened in the data output.

Using uppercase on the tables also made it difficult in pgadmin. The query would not recognize the column names unless you put quotations around it if a table had any uppercase in its name.



## Future Goals
(what would you do if you had more time?)
