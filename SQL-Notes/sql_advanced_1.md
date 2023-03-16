## SQL Advanced - 1 🚀👩‍🚀

### 1. SQL - Data Types

- **Numeric** - `INT`, `FLOAT`, `DECIMAL`
- **String** - `CHAR`, `VARCHAR`, `TEXT`
- **Date/Time** - `DATE`, `DATETIME`, `TIMESTAMP`
- **Boolean** - `BOOLEAN`

### 2. SQL - Operators

- **Arithmetic** - `+`, `-`, `*`, `/`, `MOD`
- **Comparison** - `=`, `!=`, `<>`, `>`, `<`, `>=`, `<=`
- **Logical** - `AND`, `OR`, `NOT`

### 3. SQL - Functions

- **Aggregate** - `COUNT`, `SUM`, `AVG`, `MIN`, `MAX`
- **String** - `CONCAT`, `LENGTH`, `LOWER`, `UPPER`, `SUBSTRING`
- **Date/Time** - `CURDATE`, `CURTIME`, `NOW`, `YEAR`, `MONTH`, `DAY`

### 4. SQL - Constraints

- **NOT NULL** - Ensures that a column cannot have a NULL value
- **UNIQUE** - Ensures that all values in a column are different
- **PRIMARY KEY** - A combination of a NOT NULL and UNIQUE. Uniquely identifies each row in a table
- **FOREIGN KEY** - Uniquely identifies a row/record in another table
- **CHECK** - Ensures that all values in a column satisfies a specific condition
- **DEFAULT** - Sets a default value for a column when no value is specified
- **CREATE INDEX** - Used to create and retrieve data from the database very quickly

### 5. SQL - Joins

- **INNER JOIN** - Returns records that have matching values in both tables
- **LEFT JOIN** - Returns all records from the left table, and the matched records from the right table
- **RIGHT JOIN** - Returns all records from the right table, and the matched records from the left table
- **FULL JOIN** - Returns all records when there is a match in either left or right table

### 6. SQL - Distinct

- **DISTINCT** - Returns only distinct (different) values

### 7. SQL - Wildcards

- **%** - The percent sign represents zero, one, or multiple characters
- **\_** - The underscore represents a single character
- **[charlist]** - The bracket represents any single character within the brackets
- **[!charlist]** - The exclamation mark represents any single character not in the brackets

### 8. SQL - Aliases

- **AS** - Used to give a table, or a column in a table, a temporary name

### 9. SQL - Comments

- **--** - Single line comment
- **/\* \*/** - Multi-line comment

### 10. SQL - Order By

- **ORDER BY** - Used to sort the result-set in ascending or descending order

### 11. SQL - Group By

- **GROUP BY** - Used in conjunction with the aggregate functions to group the result-set by one or more columns
- example: `SELECT COUNT(*), country FROM customers GROUP BY country;`

### 12. SQL - Having

- **HAVING** - Used with the GROUP BY clause to filter groups of rows that have a common column value
- example: `SELECT COUNT(*), country FROM customers GROUP BY country HAVING COUNT(*) > 5;`

### 13. SQL - Top

- **TOP** - Used to specify the number of records to return
- example: `SELECT TOP 3 * FROM customers;`

### 14. SQL - Subqueries

- **Subquery** - A query within another query and embedded within the WHERE clause
- example: `SELECT * FROM customers WHERE country = 'USA' AND city IN (SELECT city FROM customers WHERE country = 'UK');`
