# Trek_300 Style Guide

### Use indented upper case SQL-commands

It is more readable, because you can see the structure of the SQL clearly

```sql
-- Good
SELECT * 
FROM users

-- Bad
SELECT * FROM users

-- Bad
Select * From users
```

### Put each selected column on a new line

Put each column in a line to better see the involved column, start each column with a comma to better see when a new colum starts

```sql
-- Good
SELECT ID
     , NAME
FROM users 

-- Bad
SELECT ID, NAME
FROM users 
```

### Indent the WHERE Clausel and start AND in a new line

```sql
-- Good
SELECT ID
     , NAME
FROM users 
WHERE 1 = 1
  AND ID = 200
  AND Name = 'Smith'

-- Bad
SELECT ID
     , NAME
FROM users 
WHERE ID = 200 AND Name = 'Smith'
```

### Use space inside of parenthesis

```sql
-- Good
SELECT ID
     , NAME
FROM users 
WHERE 1 = 1
  AND ID in ( 200, 300, 400 )


-- Bad
SELECT ID
     , NAME
FROM users 
WHERE 1 = 1
  AND ID in (200,300,400)
```
