# Database_Practice
## Table: Products
| Column        | Type          | Description       |
| ------------- | ------------- | ----------------- |
| ProductID     | INT (PK)      | Auto-increment ID |
| ProductName   | VARCHAR(100)  | Product name      |
| Category      | VARCHAR(50)   | Product category  |
| Price         | DECIMAL(10,2) | Product price     |
| StockQuantity | INT           | Available stock   |

## Table Commands (DDL)
```sql
CREATE TABLE Products (
    ProductID INT AUTO_INCREMENT PRIMARY KEY,
    ProductName VARCHAR(100),
    Category VARCHAR(50),
    Price DECIMAL(10,2),
    StockQuantity INT
);
```
## View tables
```sql
SHOW TABLES;
```

## View structure
```sql
DESCRIBE Products;
```
##CRUD Operations
### INSERT multiple
```sql
INSERT INTO Products VALUES
(NULL,'Mouse','Electronics',25,50),
(NULL,'Keyboard','Electronics',45,30);
```

### SELECT
```sql
SELECT * FROM Products;
```





















