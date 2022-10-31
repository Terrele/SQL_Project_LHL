What issues will you address by cleaning the data?

The types of issues you will address by cleaning data is removing duplicates, fixing type errors, making string formats consistent e.g. "bags" and "Bags" are considered different.



Queries:
Below, provide the SQL queries you used to clean your data.

alter TABLE session
DROP column itemrevenue

alter TABLE session
DROP column itemquantity

alter TABLE session
DROP column productrefundamount

alter TABLE session
DROP column searchkeyword

alter TABLE analytics
DROP column userid

ALTER TABLE session
ALTER COLUMN productprice TYPE float;

UPDATE session
SET productprice = productprice/1000000