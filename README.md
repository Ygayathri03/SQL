# SQL - Structured Query Language
## SELECT QUERIES
--> SELECT => to retrieve data from SQL database

Syntax :

SELECT column1,column2,.... 

FROM table;

--> SELECT all queries

SELECT * 

FROM table;

# SQL query practice : (6002526)
- from [sqlbolt](https://sqlbolt.com/lesson)

# Lesson 1 : SELECT queries 101
1. Find the title of each film
```
SELECT title FROM movies;
```
2. Find the director of each film
```
SELECT director FROM movies;
```
3. Find the title and director of each film
```
SELECT title, director FROM movies;
```
4. Find the title and year of each film
```
SELECT title, year FROM movies;
```
5. Find all the information about each film
```
SELECT * FROM movies;
```

## QUERIES WITH CONSTRAINTS
-->WHERE => The clause is applied to each row of data by checking specific column values to determine whether it should be included in the results or not.

Syntax :

SELECT column1,column2,....

FROM table

WHERE condition
      AND/OR another condition
      AND/OR...;

   Operator	                          Condition	                                        SQL Example
=, !=, < <=, >, >=	    Standard numerical operators	                         col_name != 4
BETWEEN … AND …	          Number is within range of two values (inclusive)	       col_name BETWEEN 1.5 AND 10.5
NOT BETWEEN … AND …	    Number is not within range of two values (inclusive)   	 col_name NOT BETWEEN 1 AND 10
IN (…)	                Number exists in a list	                               col_name IN (2, 4, 6)
NOT IN (…)	                Number does not exist in a list	                         col_name NOT IN (1, 3, 5)

