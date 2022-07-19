- [What is a Primary Key?](#what-is-a-primary-key)
- [What is a UNIQUE constraint?](#what-is-a-unique-constraint)
- [What is a Foreign Key?](#what-is-a-foreign-key)
- [What is a Join? List its different types.](#what-is-a-join-list-its-different-types)
- [What is a Self-Join?](#what-is-a-self-join)

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
