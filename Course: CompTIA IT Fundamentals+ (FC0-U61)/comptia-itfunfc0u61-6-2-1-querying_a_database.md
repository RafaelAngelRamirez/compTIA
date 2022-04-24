Filename: comptia-itfunfc0u61-6-2-1-querying_a_database
Show Name: CompTIA IT Fundamentals (Exam FC0-U61)
Topic Name: Databases
Episode Name: Querying a Database
Show Description: In this episode, Ronnie and Don explain how to communicate with a database using SQL queries. They then give multiple examples of adding, retrieving and modifying data in a SQL database. 

#### Querying a Database
---

* How do we talk to a database?
	+ Direct/manual access
		- Not typical
		- Can lead to corruption
	+ Programmatic access
		- Very common
		- Via an API or protocol stack
	+ User interface/utility access
		- Useful for R&D
		- Does not scale well
	+ Query/report builders
		- Useful for repetitious queries
* What commands do we use with a database? 
	+ Data manipulation language (DML)
	+ Data definition language (DDL)

**Create a table**

```sql
CREATE TABLE USStates(
	state_name nvarchar(50),
	state_abr nchar(2)
)
```

**Insert data into the table**

```sql
INSERT INTO USStates (state_name,state_abr)
VALUES 
	('Florida','FL'),
	('Georgia','GA'),
	('Alabama','AL')	
```

**View data in the table**

```sql
SELECT * FROM USStates ORDER BY state_name;
SELECT state_name FROM USStates WHERE state_abr = 'FL'
```

**Change data in the table**

```sql
INSERT INTO USStates (state_name,state_abr) VALUES ('NewYork','NY');
UPDATE USStates SET
	state_name = 'New York'
WHERE state_abr = 'NY';
```

**Delete data from the table**

```sql
DELETE FROM USStates WHERE state_abr = 'NY';
```

**Delete the table**

```sql
DROP TABLE USStates;
``` 
