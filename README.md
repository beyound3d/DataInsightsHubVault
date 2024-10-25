# dbchronic

## Keyword for MYSQL
```
FROM
```

```
SELECT
```

```
SELECT DISTINCT
```

```
WHERE
```

```
ORDER BY
```

```
AND
```

```
LIKE 'G%'
```

```
OR
```

```
NOT
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



