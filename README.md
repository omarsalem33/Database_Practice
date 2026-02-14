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

### Update Record
```sql
UPDATE Products
SET Price = 200
WHERE ProductID = 1;
```
### DELETE Record
```sql
DELETE FROM Products
WHERE ProductID = 1;
```

## Filtering Data (WHERE)
### Price greater than 100
```sql
SELECT * FROM Products
WHERE Price > 100;
```
### Category is Electronics
```sql
SELECT * FROM Products
WHERE Category = 'Electronics';
```

### Stock less than or equal to 20
```sql
SELECT * FROM Products
WHERE StockQuantity <= 20;
```

## Sorting Data (ORDER BY)
### Sort by Price ascending
```sql
SELECT * FROM Products
ORDER BY Price ASC;
```
### Sort by Price descending
```sql
SELECT * FROM Products
ORDER BY Price DESC;
```

### Sort by Category, then Price descending
```sql
SELECT * FROM Products
ORDER BY Category, Price DESC;
```

## DISTINCT
### Unique categories
```sql
SELECT DISTINCT Category
FROM Products;
```

## LIKE (Pattern Matching)
### Names starting with 'S'
```sql
SELECT * FROM Products
WHERE ProductName LIKE 'S%';
```
### Names ending with 'e'
```sql
SELECT * FROM Products
WHERE ProductName LIKE '%e';
```
### Names containing 'Watch'
```sql
SELECT * FROM Products
WHERE ProductName LIKE '%Watch%';
```

## BETWEEN
### Price between 50 and 100
```sq
SELECT * FROM Products
WHERE Price BETWEEN 50 AND 100;
```
## LIMIT (Restrict Results)
### First 5 products
```sql
SELECT * FROM Products
LIMIT 5;
```
### 5 products after skipping first 10
```sql
SELECT * FROM Products
LIMIT 10,5;
```

## Aggregate Functions
### Count all products
```sql
SELECT COUNT(*) FROM Products;
```
### Sum of all stock
```sql
SELECT SUM(StockQuantity) FROM Products;
```
### Average price
```sql
SELECT AVG(Price) FROM Products;
```

### Minimum price
```sql
SELECT MIN(Price) FROM Products;
```

### Maximum price
```sql
SELECT MAX(Price) FROM Products;
```

## GROUP BY

### Count products per category
```sql
SELECT Category, COUNT(*)
FROM Products
GROUP BY Category;
```

### Average price per category
```sql
SELECT Category, AVG(Price)
FROM Products
GROUP BY Category;

```


## HAVING
### Categories with more than 5 products
```sql
SELECT Category, COUNT(*)
FROM Products
GROUP BY Category
HAVING COUNT(*) > 5;
```
### Categories with average price > 100
```sql
SELECT Category, AVG(Price)
FROM Products
GROUP BY Category
HAVING AVG(Price) > 100;

```












