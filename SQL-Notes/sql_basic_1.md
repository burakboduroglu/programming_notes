## SQL Basics - 1 🚀👩‍🚀

### - Data Manipulation Commands

- `SELECT` - used to retrieve data from a database
  example:

```sql
SELECT column1, column2, ...
FROM table_name;
```

- `UPDATE` - used to update existing data within a database
  example:

```sql
UPDATE table_name
SET column1 = value1, column2 = value2, ...
WHERE condition;
```

- `DELETE` - used to delete records from a database
  example:

```sql
DELETE FROM table_name
WHERE condition;
```

- `INSERT INTO` - used to insert new data into a database
  example:

```sql
INSERT INTO table_name (column1, column2, column3, ...)
VALUES (value1, value2, value3, ...);
```

- `TRUNCATE TABLE` - used to remove all records from a table, including all spaces allocated for the records are removed
  example:

```sql
TRUNCATE TABLE table_name;
```

---

### - Database Manipulation Commands

- `CREATE DATABASE` - used to create a new database
  example:

```sql
CREATE DATABASE database_name;
```

- `ALTER DATABASE` - used to modify a database
  example:

```sql
ALTER DATABASE database_name
MODIFY COLUMN column_name datatype;
```

- `DROP DATABASE` - used to delete a database
  example:

```sql
DROP DATABASE database_name;
```

- `CREATE TABLE` - used to create a new table
  example:

```sql
CREATE TABLE table_name (
    column1 datatype,
    column2 datatype,
    column3 datatype,
     ....
    );
```

- `ALTER TABLE` - used to modify a table
  example:

```sql
ALTER TABLE table_name
ADD column_name datatype;
```

- `DROP TABLE` - used to delete a table
  example:

```sql
DROP TABLE table_name;
```

- `CREATE INDEX` - used to create an index (search key)
  example:

```sql
CREATE INDEX index_name
ON table_name (column_name);
```

- `DROP INDEX` - used to delete an index
  example:

```sql
DROP INDEX index_name
ON table_name;
```

---
