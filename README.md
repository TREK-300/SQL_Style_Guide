# SQL_Style_Guide

### Use indented upper case SQL-commands

It is more readable, because you can see the structure of the SQL better

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


```sql
-- Good
SELECT ID
     , NAME
FROM users 

-- Bad
select 
    id,
    email
from users 

-- Bad
select id
from users 

-- Bad
select id, email
from users 
```
