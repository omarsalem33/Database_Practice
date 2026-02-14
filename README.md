# Database_Practice
##Table: Products
| Column        | Type          | Description       |
| ------------- | ------------- | ----------------- |
| ProductID     | INT (PK)      | Auto-increment ID |
| ProductName   | VARCHAR(100)  | Product name      |
| Category      | VARCHAR(50)   | Product category  |
| Price         | DECIMAL(10,2) | Product price     |
| StockQuantity | INT           | Available stock   |

##Table Commands (DDL)
`
CREATE TABLE Products (
    ProductID INT AUTO_INCREMENT PRIMARY KEY,
    ProductName VARCHAR(100),
    Category VARCHAR(50),
    Price DECIMAL(10,2),
    StockQuantity INT
);
`
##View tables
`
SHOW TABLES;
`

##View structure
`
DESCRIBE Products;
`
##CRUD Operations
###INSERT multiple
`
INSERT INTO Products VALUES
(NULL,'Mouse','Electronics',25,50),
(NULL,'Keyboard','Electronics',45,30);
`

###SELECT
`SELECT * FROM Products;
  `







## Example SQL Query

Get all expensive products:

```sql
SELECT ProductName, Price
FROM Products
WHERE Price > 500
ORDER BY Price DESC;













