# SQL - Structured Query Language
## SELECT QUERIES
--> SELECT => to retrieve data from SQL database

Syntax :

SELECT column1,column2,.... 

FROM table;

--> SELECT all queries

SELECT * 

FROM table;

###
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
```
   Operator	                          Condition	                                        SQL Example
=, !=, < <=, >, >=	    Standard numerical operators	                         col_name != 4
BETWEEN … AND …	          Number is within range of two values (inclusive)	       col_name BETWEEN 1.5 AND 10.5
NOT BETWEEN … AND …	    Number is not within range of two values (inclusive)   	 col_name NOT BETWEEN 1 AND 10
IN (…)	                Number exists in a list	                               col_name IN (2, 4, 6)
NOT IN (…)	                Number does not exist in a list	                         col_name NOT IN (1, 3, 5)
```
###
1. Find the movie with a row id of 6
```
SELECT * FROM movies WHERE id = 6;
```
2. Find the movies released in the years between 2000 and 2010
```
SELECT * FROM movies WHERE year BETWEEN 2000 AND 2010;
```
3. Find the movies not released in the years between 2000 and 2010
```
SELECT * FROM movies WHERE year NOT BETWEEN 2000 AND 2010;
```
4. Find the first 5 Pixar movies and their release year
```
SELECT title, year FROM movies WHERE year <= 2003;
```
##
```
Operator	                         Condition	                                                   Example
=	            Case sensitive exact string comparison (notice the single equals)	            col_name = "abc"
!= or <>	      Case sensitive exact string inequality comparison	                        col_name != "abcd"
LIKE	            Case insensitive exact string comparison	                                    col_name LIKE "ABC"
NOT LIKE	      Case insensitive exact string inequality comparison	                        col_name NOT LIKE "ABCD"
%	            only with LIKE or NOT LIKE(0 or more)                                         col_name LIKE "%AT%"
_	            only with LIKE or NOT LIKE(1)                                                 col_name LIKE "AN_"
IN (…)	      String exists in a list	                                                      col_name IN ("A", "B", "C")
NOT IN (…)	      String does not exist in a list	                                          col_name NOT IN ("D", "E", "F")
```
###
1. Find all the Toy Story movies
```
SELECT title FROM movies WHERE title LIKE "Toy Story%";
```
2. Find all the movies directed by John Lasseter
```
SELECT title FROM movies WHERE director = "John Lasseter";
```
3. Find all the movies (and director) not directed by John Lasseter
```
SELECT title FROM movies WHERE director != "John Lasseter";
```
4. Find all the WALL-* movies
```
SELECT title FROM movies WHERE title LIKE "WALL-_"
```
