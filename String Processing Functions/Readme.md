# About String Functions in MySQl

## 1. Using ```Sub String``` function:-

We will be using four functions here that are present in SQL

- ```UPPER(A)``` where A is string
- ```LOWER(A)``` where A is string
- ```SUBSTR(A,index,length)``` where **A** is string, **index** is starting index(1 index insead of 0 index) and **length** which is optional
   So to get first letter we can use SUBSTR(name,1,1)
   To get the remaining string we can use SUBSTR(name,2) // length is not required here
- ```CONCAT(A,B)``` where we concat two strings A+B

## 2. Using Group Concatenation:-

**It is basically used to concatenate diff. values into a single row using function ```"GROUP_CONCAT"```**

-->Basic Info:-

- The ```GROUP BY``` statement groups rows that have the same values into summary rows.
- The GROUP BY statement is often used with ```aggregate functions (COUNT(), MAX(), MIN(), SUM(), AVG())``` to group the result-set by one or more columns.
- Another group method we use is ```GROUP_CONCAT```, which concat items of grouped rows and joins them by using "," seperator.
