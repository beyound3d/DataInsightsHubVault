-------------------------creating multiple servers in database


--------------------------delete a server



--------------------------for showing/seeing all tables in database

```
SELECT TABLE_SCHEMA, TABLE_NAME, TABLE_TYPE
FROM INFORMATION_SCHEMA.TABLES;
```

--------------------------create tables in database

**Frmat**
```
CREATE TABLE TableName (
    Column1 DataType [CONSTRAINT ConstraintName] [NOT NULL | NULL],
    Column2 DataType [CONSTRAINT ConstraintName] [NOT NULL | NULL],
    Column3 DataType [CONSTRAINT ConstraintName] [NOT NULL | NULL],
    ...
    PRIMARY KEY (Column1) -- Optional, define a primary key
);
```


```
CREATE TABLE Employees (
    EmployeeID INT PRIMARY KEY,
    FirstName NVARCHAR(50) NOT NULL,
    LastName NVARCHAR(50) NOT NULL,
    BirthDate DATE,
    HireDate DATETIME,
    Salary DECIMAL(18, 2)
);
```

-----------------------adding new column in table

**Format**
```
ALTER TABLE table_name
ADD column_name data_type [constraints];
```

ex:
```
ALTER TABLE Employees
ADD 
DateOfBirth DATE,	
PhoneNumber VARCHAR(15) NOT NULL,
Status VARCHAR(10) DEFAULT 'Active',
Address NVARCHAR(100),
DepartmentID INT NOT NULL;
```

### Points to Ponder
- Data Types: Choose appropriate data types for your columns, such as INT, NVARCHAR, DATE, DECIMAL, etc.
- Constraints: Add constraints like PRIMARY KEY, FOREIGN KEY, UNIQUE, or CHECK as needed.
- Indexes: Add indexes for better query performance.
