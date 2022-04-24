Filename: comptia-itfunfc0u61-6-1-1-database_concepts
Show Name: CompTIA IT Fundamentals (Exam FC0-U61)
Topic Name: Databases
Episode Name: Database Concepts
Show Description: In this episode, Ronnie and Don explore what makes up a modern database. They discuss the different types of databases, the advantages for using databases, and even some of the alternatives to using a database. 

#### Database Concepts
---

* What is a database?
	+ Repository of information
	+ Ordered for quick access
	+ Supports data-driven business decisions
		- Data capture and collection 
		- Data correlation
		- Meaningful reporting
	+ Records 
	+ Storage
* What can you do with a database?
	+ Input data
		- Data entry
	+ Output data
		- Query
	+ Represent data
		- Reports
	+ Archive data
		- Data persistence
* Why not use a flat file like Excel?
	+ Multiple concurrent users
	+ Scalability
	+ Speed
	+ Variety of data
* What types of databases are there?
	+ Structured vs. semi-structured vs. non-structured
	+ Relational databases
	+ Non-relational databases
		- Key/value databases 
		- Document databases

**Generate a list of employees with their hire date**

```sql
SELECT p.FirstName,p.LastName,h.JobTitle,h.HireDate
FROM Person.Person AS p
JOIN HumanResources.Employee AS h ON p.BusinessEntityID=h.BusinessEntityID;
```

**Ranking employees by bonus amount**

```sql
SELECT 
  s.BusinessEntityID,
  p.FirstName,
  p.LastName,
  s.Bonus,
  RANK() OVER (ORDER BY Bonus DESC) AS Ranking
FROM Sales.SalesPerson AS s
JOIN Person.Person AS p
ON s.BusinessEntityID=p.BusinessEntityID
ORDER BY Ranking
```