- [What is Data Warehousing?](#what-is-data-warehousing)
- [What is a lock?](#what-is-a-lock)
- [What is meant by normalization and denormalization?](#what-is-meant-by-normalization-and-denormalization)

### What is Data Warehousing?
The process of collecting, extracting, transforming, and loading data from multiple sources and storing them in one database is known as data warehousing.
A data warehouse can be considered as a central repository where data flows from transactional systems and other relational databases and is used for data analytics.
A data warehouse comprises a wide variety of an organization’s historical data that supports the decision-making process in an organization.

### What is a lock?
A database lock is a mechanism to protect a shared piece of data from getting updated by two or more database users at the same time.
When a single database user or session has acquired a lock then no other database user or session can modify that data until the lock is released.

**Shared lock** is also called read lock, used for reading data items only.
Shared locks support read integrity. They ensure that a record is not in process of being updated during a read-only request.
Shared locks can also be used to prevent any kind of updates of record.

For example, consider a case where initially A=100 and there are two transactions which are reading A.
If one of transaction wants to update A, in that case other transaction would be reading wrong value. 
However, Shared lock prevents it from updating until it has finished reading.

**Exclusive Lock** is also called write lock.
An exclusive lock prevents any other locker from obtaining any sort of a lock on the object.
They can be owned by only one transaction at a time.

For example, consider a case where initially A=100 when a transaction needs to deduct 50 from A.
We can allow this transaction by placing X lock on it.
Therefore, when any other transaction wants to read or write, exclusive lock prevent it.

### What is meant by normalization and denormalization?
**Normalization** is a process of reducing redundancy by organizing the data into multiple tables.
Normalization leads to better usage of disk spaces and makes it easier to maintain the integrity of the database.  

**Denormalization** is the reverse process of normalization as it combines the tables which have been normalized into a single table so that data retrieval becomes faster.
JOIN operation allows us to create a denormalized form of the data by reversing the normalization.

