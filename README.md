# dbchronic

## Resources
- [w3School](https://www.w3schools.com/sql)
  

<img src="https://github.com/beyound3d/DataInsightsHubVault/blob/master/tcl.png" height="50dp" width="400dp" />

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


