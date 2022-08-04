# UNION:-

The UNION operator is used to combine the result-set of two or more ```SELECT statements```.

- Every SELECT statement within UNION must have the same number of columns
- The columns must also have similar data types
- The columns in every SELECT statement must also be in the same order

## Syntax:-

```SELECT column_name(s) FROM table1
UNION
SELECT column_name(s) FROM table2;
```

# CASE:-

The CASE statement goes through conditions and return a value when the first condition is met (like an IF-THEN-ELSE statement). So, once a condition is true, it will stop reading and return the result.

If no conditions are true, it will return the value in the ELSE clause.

If there is no ELSE part and no conditions are true, it returns NULL.

## Syntax:-
```
CASE
    WHEN condition1 THEN result1
    WHEN condition2 THEN result2
    WHEN conditionN THEN resultN
    ELSE result
END;
```

# LIMIT:-

MySQL Limit query is used to restrict the number of rows returns from the result set, rather than fetching the whole set in the MySQL database.

_To get only the specified rows from the table, MySQL uses the LIMIT clause, whereas SQL uses the TOP clause, and Oracle uses the ROWNUM clause with the SELECT statement._

## Syntax:-

```
SELECT column_list  
FROM table_name  
LIMIT offset, count;  
```

In the above syntax, we can see:

- Column_list: It is the name of the column that you want to return.

- Table_name: It is the name of the table that contains your column name.

- Offset: It specifies the number of a row from which you want to return. The offset of the row starts from 0, not 1.

- Count: It specifies the maximum number of rows you want to return.

## VERY VERY IMPO:-

**MySQL LIMIT to get the nth highest or lowest value**

**Sometimes we want to get the rows of nth highest or lowest value. In that case, we can use the following MySQL LIMIT clause to get the expected result:**

```
SELECT column_list  
FROM table_name  
ORDER BY expression  
LIMIT n-1, 1;  
```
In this syntax, the **LIMIT n-1, 1 clause returns 1 row that starts at the row n.**

For example, the following query returns the employee information who has the **SECOND HIGHEST- INCOME:**

```
SELECT emp_name, city, income FROM employees  
ORDER BY income  
LIMIT 1, 1;  
```
