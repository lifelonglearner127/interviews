- [What is a Primary Key?](#what-is-a-primary-key)
- [What is a UNIQUE constraint?](#what-is-a-unique-constraint)
- [What is a Foreign Key?](#what-is-a-foreign-key)
- [What is a Join? List its different types.](#what-is-a-join-list-its-different-types)
- [What is a Self-Join?](#what-is-a-self-join)
- [What is a Cross-Join?](#what-is-a-cross-join)
- [What is an Index? Explain its different types.](#what-is-an-index-explain-its-different-types)
- [What is the difference between Clustered and Non-clustered index?](#what-is-the-difference-between-clustered-and-non-clustered-index)
- [What is Data Integrity?](#what-is-data-integrity)
- [What is a Query?](#what-is-a-query)
- [What is a Subquery? What are its types?](#what-is-a-subquery-what-are-its-types)
- [What is View and Materialized View? Difference between them](#what-is-view-and-materialized-view-difference-between-them)

### What is a Primary Key?
The PRIMARY KEY constraint uniquely identifies each row in a table.
It must contain UNIQUE values and cannot contain NULL values.
A table can have only one primary key in the table
This primary key can consist of single or multiple columns.

### What is a UNIQUE constraint?
A UNIQUE constraint ensures that all values in a column are different.
This provides uniqueness for the column(s) and helps identify each row uniquely.
Unlike primary key, we can have many UNIQUE constraints per table. 

### What is a Foreign Key?
A FOREIGN KEY is a field (or collection of fields) in one table, that refers to the PRIMARY KEY in another table.
Foreign key constraint ensures referential integrity in the relation between two tables.

### What is a Join? List its different types.
The SQL Join clause is used to combine records (rows) from two or more tables in a SQL database based on a related column between the two.
- **(INNER) JOIN**: Retrieves records that have matching values in both tables involved in the join.
- **LEFT (OUTER) JOIN**: Retrieves all the records/rows from the left and the matched records/rows from the right table.
- **RIGHT (OUTER) JOIN**: Retrieves all the records/rows from the right and the matched records/rows from the left table.
- **FULL (OUTER) JOIN**: Retrieves all the records where there is a match in either the left or right table.

### What is a Self-Join?
A self JOIN is a case of regular join where a table is joined to itself based on some relation between its own column(s).
Self-join uses the INNER JOIN or LEFT JOIN clause and a table alias is used to assign different names to the table within the query.

### What is a Cross-Join?
Cross-Join can be defined as a cartesian product of the two tables included in the join.
The table after join contains the same number of rows as in the cross-product of the number of rows in the two tables.

### What is an Index? Explain its different types.
A database index is a data structure that improves the speed of data retrieval operations on a database table at the cost of additional writes and spaces to maintain the index data structure. 

**Unique and non-unique Index**
Unique indexes are indexes that help maintain data integrity by ensuring that no two rows of data in a table have identical key values. Once a unique index has been defined for a table, uniqueness is enforced whenever keys are added or changed within the index.

**Clustered and non-clustered Index**
Clustered indexes are indexes whose order of the rows in the database corresponds to the order of the rows in the index. This is why only on clustered index can exist in a given table, whereas, multiple non-clustered indexes can exist in the table.

### What is the difference between Clustered and Non-clustered index?
- `Clustered` index modifies the way records are stored in a database based on the indexed column. A `non-clustered` index creates a separate entity within the table which references the original table.
- `Clustered` index is used for easy and speedy retrieval of data from the database, whereas, fetching records from the non-clustered index is relatively slower.
- In SQL, a table can have a single `clustered` index whereas it can have multiple `non-clustered` indexes.

### What is Data Integrity?
Data integrity is the assurance of accuracy and consistency of data over its entire life-cycle and is a critical aspect of the design, implementation, and usage of any system which stores, processes, or retrieves data. It also defines integrity constraints to enforce business rules on the data when it is entered into an application or a database.

### What is a Query?
A query is a request for data or information from a database table or combination of tables. A database query can be either a select query or an actioin query.

### What is a Subquery? What are its types?
A subquery is a query within another query, also known as a nested query or inner query. It is used to restrict or enhance the data to be queried by the main query. thus restricting or enhancing the output of the main query respectively. There are 2 types of subquery - `Correlated` and `Non-Correlated`.
- A `correlated` subquery cannot be considered as an independent query, but it can refer to the column in a table listed in the `FROM` of the main query.
- A `non-correlated` subquery can be considered as an independent query and the output of the subquery is substituted in the main query.


### What is View and Materialized View? Difference between them
In SQL, a `view` is a virtual table based on the result-set of an SQL statement. A view contains rows and columns, just like a real table. The fields in a view are fields from one or more real tables in the database.

A `materialized view` is a view whose contents are computed and stored. Materialized view is also a logical virtual table, but in this case the result of the query is stored in the table or the disk. The performance of the materialized view is better than normal view since the data is stored in the disk.

Differences:

- Storage:
    - In Views the resulting tuples of the query expression is not get storing on the disk only the query expression is stored on the disk.	
    - On other hand in case of Materialized views both query expression and resulting tuples of the query get stored on the disk.
- Query Execution:
    - As mentioned above in case of Views the query expression is stored on the disk and not its result so query expression get executed every time when user try to fetch data from it so that user will get the latest updated value every time.
    - While on other hand in case of Materialized Views the result of query is get stored on the disk and hence the query expression did not get executed every time when user try to fetch the data so that user will not get the latest updated value if it get changed in database.
- Cost Effective:
    - As Views does not have any storage cost associated with it so they also does not have any update cost associated with it.
    - On other hand Materialized Views does have a storage cost associated with it so also have update cost associated with it.
- Design:
    - Views in SQL are designed with a fixed architecture approach due to which there is an SQL standard of defining a view.
    - On other hand in case of Materialized Views in SQL are designed with a generic architecture approach so there is no SQL standard for defining it,and its functionality is provided by some databases systems as an extension.
- Usage:
    - Views are generally used when data is to be accessed infrequently and data in table get updated on frequent basis.
    - On other hand Materialized Views are used when data is to be accessed frequently and data in table not get updated on frequent basis.
