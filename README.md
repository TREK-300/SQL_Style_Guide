# Trek_300 Style Guide

The goal is to improve readability and seeing the structure of the sql more clearly.

* Write clausels (SELECT, FROM, WHERE) uppercase. 
* Put comma before each column
* Indent AND in WHERE Clausel
* Put spaces inside parenthesis
* Use the as clausel
* Indent ON in JOIN clausel
* Use the term INNER JOIN instead of JOIN
* Write Aliases small

```sql
SELECT us.ID
     , us.AME
     , us.LAST_NAME
FROM USER_TABLE as us
LEFT JOIN oders as or
  ON us.ID = or.ID
WHERE 1 = 1
  AND ID in ( 200, 300, 400 )
  AND Country = 'USA'
