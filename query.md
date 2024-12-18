### partially case-sensitive-------------sql

## -------------------------creating multiple servers in database


##  --------------------------delete a server



## --------------------------for showing/seeing all tables in database

```
SELECT TABLE_SCHEMA, TABLE_NAME, TABLE_TYPE
FROM INFORMATION_SCHEMA.TABLES;
```
### ------------------------Deleting table
```
DROP TABLE Table1, Employees;
```

## -----------------------Deleting all data from table
```
DELETE FROM Employees;
```

## --------------------------create tables in database

**Format**
```
CREATE TABLE TableName (
    Column1 DataType [CONSTRAINT ConstraintName] [NOT NULL | NULL],
    Column2 DataType [CONSTRAINT ConstraintName] [NOT NULL | NULL],
    Column3 DataType [CONSTRAINT ConstraintName] [NOT NULL | NULL],
    ...
    PRIMARY KEY (Column1) -- Optional, define a primary key
);
```

ex:
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

## -----------------------adding new column in table

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
## ----------------------Adding data in tables
***Use Transactions for Bulk Inserts: For critical operations, wrap your INSERT statement in a transaction to maintain consistency.***
```
BEGIN TRANSACTION;
INSERT INTO Employees (EmployeeID, FirstName, LastName, BirthDate, HireDate, Salary, DateOfBirth, PhoneNumber, Status, Address, DepartmentID)
VALUES 
(1, 'John', 'Doe', '1985-05-20', '2020-06-15', 60000.00, '1985-05-20',1234567890, 'Active', '123 Main St, Cityville', 101),
(2, 'Jane', 'Smith', '1990-11-12', '2019-03-01', 70000.00, '1990-11-12',1234567890, 'Active', '456 Elm St, Townsville', 102),
(3, 'Emily', 'Jones', '1982-02-18', '2021-01-20', 58000.00, '1982-02-18',1234567890, 'On Leave', '789 Oak St, Villagetown', 103);

COMMIT TRANSACTION;
```

## ---------------------Delete data / or delete row / delete Employee data
```
DELETE FROM Employees
WHERE EmployeeID = 1;
```

### Points to Ponder
- Data Types: Choose appropriate data types for your columns, such as INT, NVARCHAR, DATE, DECIMAL, etc.
- Constraints: Add constraints like PRIMARY KEY, FOREIGN KEY, UNIQUE, or CHECK as needed.
- Indexes: Add indexes for better query performance.
