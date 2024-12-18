-------------------------creating multiple servers in database


--------------------------delete a server



--------------------------for showing/seeing all tables in database

```
SELECT TABLE_SCHEMA, TABLE_NAME, TABLE_TYPE
FROM INFORMATION_SCHEMA.TABLES;
```

--------------------------create tables in database

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

### Points to Ponder
- Data Types: Choose appropriate data types for your columns, such as INT, NVARCHAR, DATE, DECIMAL, etc.
- Constraints: Add constraints like PRIMARY KEY, FOREIGN KEY, UNIQUE, or CHECK as needed.
- Indexes: Add indexes for better query performance.
