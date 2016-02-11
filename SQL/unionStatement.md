# Union Statment

The **UNION** statement in SQL (T-SQL) is used to concatenate the contents of two or more queries. This functionality is different than a join in a sense that it will return the first query and then the results of the second query. Whereas a **JOIN** makes a cartesian product and creates a subset of the data being returned. 

```SQL
USE [AdventureWorks]
GO
SELECT ProductModelID, Name
FROM Production.ProductModel
WHERE ProductModelID NOT IN (3, 4)
UNION
SELECT ProductModelID, Name
FROM dbo.Gloves
ORDER BY Name;
GO
```

Two things to note about using the **UNION** statement:
 * The number and order of the columns must be the same in all queries.
 * The data types must be compatible.
