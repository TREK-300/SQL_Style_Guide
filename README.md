# Trek_300 Style Guide

The goal is to improve readability and seeing the structure of the sql more clearly.

```sql
SELECT 
     em.BUSINESSENTITYID 
   , pe.TITLE 
   , pp.PHONENUMBER 
   , pe.NAME              as PhoneNumberType 
   , ea.EMAILADDRESS 
   , ad.ADDRESSLINE1 
   , sp.NAME              as StateProvinceName 
   , cr.NAME              as CountryRegionName
FROM humanresources.EMPLOYEE               as em
INNER JOIN   person.PERSON                 as pe   ON  pe.BUSINESSENTITYID = em.BUSINESSENTITYID
INNER JOIN   person.BUSINESSENTITYADDRESS  as be   ON  be.BUSINESSENTITYID = em.BUSINESSENTITYID
LEFT JOIN    person.ADDRESS                as ad   ON         ad.ADDRESSID = be.ADDRESSID
LEFT JOIN    person.STATEPROVINCE          as sp   ON   sp.STATEPROVINCEID = ad.STATEPROVINCEID
WHERE 1 = 1
  AND ID in ( 200, 300, 400 )
  AND Country = 'USA'
_______________________________________________________
* Write clausels (SELECT, FROM, WHERE) uppercase -> Define the border of a SQL statement 
* Join Table at the same Point                   -> Fast to see the joined tables
* Put comma before each column                   -> The most important element in a statement
* Indent AND in WHERE Clausel
* Put spaces inside parenthesis
* Write Aliases small mit two words               -> less important therefor small
