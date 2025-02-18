
Data Definition Language




New tables are created using `CREATETABLE` statement


```sql
CREATE TABLE instructor (

)
```



#### DML
Insert
- Add new rows into a table
```sql
INSERT into indtructor
VALUES (333, 'Peter Petersen', 'Comp. Sci.', 40000)
```
```
```
Update
- Modify rows in a table
```sql
UPDATE student SET deptname = 'CS'
	WHERE deptname = 'Computer Science';
```
Delete
- Delete rows from a table
```sql
DELETE FROM instructor WHERE name = 'Prince';
```



#### Type System
- Domain Types
	- int - integer
	- char(n) - fixed length character string (exactly *n* characters)
	- varchar(n) - variable length string (up to *n* characters)
	- date - a date
	- numeric (p, d)
		- Fixed point number with up to p digits and d digits precision (after the dot)
		- e.g. numeric(7, 4) can encode 100.0005 but not 1000.0003 or 100.00005




### Strict Typing
SQL employs a **strict** type systems


###[[ Query Blocks]]
	