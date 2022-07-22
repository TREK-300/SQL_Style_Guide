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
SELECT 
     em.BUSINESSENTITYID 
   , pe.TITLE 
   , pp.PHONENUMBER 
   , pe.NAME              AS PhoneNumberType 
   , ea.EMAILADDRESS 
   , ad.ADDRESSLINE1 
   , sp.NAME              AS StateProvinceName 
   , cr.NAME              AS CountryRegionName
FROM humanresources.EMPLOYEE               as em
INNER JOIN   person.PERSON                 as pe   ON  pe.BUSINESSENTITYID = em.BUSINESSENTITYID
INNER JOIN   person.BUSINESSENTITYADDRESS  as be   ON  be.BUSINESSENTITYID = em.BUSINESSENTITYID
LEFT JOIN    person.ADDRESS                as ad   ON         ad.ADDRESSID = be.ADDRESSID
LEFT JOIN    person.STATEPROVINCE          as sp   ON   sp.STATEPROVINCEID = ad.STATEPROVINCEID
WHERE 1 = 1
  AND ID in ( 200, 300, 400 )
  AND Country = 'USA'
