# dbchronic
Types-
- Relational-->MySQL, PostgreSQL, Oracle, SQL Server.
- Non- relational-->Mongo db

| **Feature**              | **Relational Databases (SQL)**               | **Non-relational Databases (NoSQL)**       |
|--------------------------|----------------------------------------------|-------------------------------------------|
| **Data Model**            | Tables with rows and columns (structured)    | Flexible formats (documents, key-value, graph, column-family) |
| **Schema**                | Fixed, predefined schema                     | Flexible or schema-less                   |
| **Scaling**               | Vertical scaling (adding resources)          | Horizontal scaling (distributing data across nodes) |
| **Consistency**           | ACID (strong consistency)                    | BASE (eventual consistency)              |
| **Query Language**        | SQL                                          | NoSQL-specific query languages (e.g., MongoDB Query Language, CQL) |
| **Transactions**          | Complex, ACID-compliant transactions         | Typically simpler, may not support full ACID transactions |
| **Best for**              | Structured data with complex relationships   | Unstructured data, flexible, scalable systems |

![image](https://github.com/user-attachments/assets/5491a1bc-18d9-42f6-b845-d0c6e7fada5b)
![image](https://github.com/user-attachments/assets/5bf590d6-ac5d-4d92-822a-a471ddc3892c)
![image](https://github.com/user-attachments/assets/9db0ede4-c5c6-4778-aa00-e5459ea4657a)



## Mongodb   <img src="https://cdn.worldvectorlogo.com/logos/mongodb-icon-1.svg" alt="MongoDB" width="50" height="50">

**Resources**
- https://www.mongodb.com/


| Feature              | MongoDB Atlas                            | MongoDB Compass                        |
|----------------------|------------------------------------------|----------------------------------------|
| **Type**             | Cloud-based managed database service     | Desktop GUI for MongoDB                |
| **Purpose**          | Hosting and managing MongoDB databases   | Visual interface for interacting with MongoDB data |
| **Deployment**       | Cloud (AWS, Azure, GCP)                  | Local or remote MongoDB databases      |
| **Main Use Case**    | Production database management           | Query building, data exploration, schema visualization |
| **Management**       | Fully managed service (backups, scaling, monitoring) | Local database management (not managed by Compass) |
| **Security**         | Advanced security features (encryption, VPC, IP whitelisting) | Security managed by the database itself |
| **Access**           | Web interface or API                     | Desktop app for database exploration   |
| **Scalability**      | Automatic scaling of resources           | N/A (depends on the underlying database) |

You might use MongoDB Atlas to host your MongoDB database in the cloud, while using MongoDB Compass to interact with and manage that database or any other MongoDB instance.

## Resources
- [w3School](https://www.w3schools.com/sql)
  

<img src="https://github.com/beyound3d/DataInsightsHubVault/blob/master/tcl.png" width="900dp" height="300dp" />

# TCL
- COMMIT: Saves all the changes made during the current transaction. Once committed, these changes are permanent and visible to other users.
```
COMMIT;
```

- ROLLBACK: Undoes all changes made in the current transaction if it hasn't been committed yet. This command is used to revert to the last committed state.
```
ROLLBACK;
```

- SAVEPOINT: Creates a point within a transaction to which you can later roll back. This allows for more granular control over transactions.

```
SAVEPOINT savepoint_name;
```

- SET TRANSACTION: Configures the properties of a transaction, such as its isolation level.
```
SET TRANSACTION ISOLATION LEVEL READ COMMITTED;
```

## Keys

- Primary |  Unique |  Candidate | Alternate |  Surrogate 
- Foreign  |  Composite
- Natural

 **Primary Key:**

1. A unique identifier for each record in a table.
2. Cannot contain NULL values.
3. Each table can have only one primary key.

   ```
   CREATE TABLE customers (
    customer_id INT PRIMARY KEY,
    name VARCHAR(100),
    email VARCHAR(100) UNIQUE
);
```


 **Foreign Key:**

1. A field (or collection of fields) in one table that uniquely identifies a row of another table.
2. Establishes a relationship between the two tables.
3. Can contain duplicate values and can be NULL.

```
CREATE TABLE orders (
    order_id INT PRIMARY KEY,
    customer_id INT,
    order_date DATE,
    FOREIGN KEY (customer_id) REFERENCES customers(customer_id)
);
```

**Unique Key**
1. Ensures that all values in a column (or a set of columns) are unique.
2. Unlike primary keys, a table can have multiple unique keys.
3. Can contain NULL values (though only one NULL per unique column).

```
CREATE TABLE products (
    product_id INT PRIMARY KEY,
    product_name VARCHAR(100) UNIQUE,
    price DECIMAL(10, 2)
);
```

**Composite Key:**

1. A key that consists of two or more columns used together to uniquely identify a record.
2. At least one of the columns in a composite key can be a foreign key.

```
CREATE TABLE enrollment (
    student_id INT,
    course_id INT,
    enrollment_date DATE,
    PRIMARY KEY (student_id, course_id)
);
```

# TCL







