## Database process with SQLite3

### 1. Create a database

```python
import sqlite3

# create a database
conn = sqlite3.connect("database.db")
```

### 2. Create a table

```python
import sqlite3

# create a database
conn = sqlite3.connect("database.db")

# create a table
conn.execute("CREATE TABLE IF NOT EXISTS table_name (column1, column2, column3, ...)")
```

### 3. Insert data

```python
import sqlite3

# create a database
conn = sqlite3.connect("database.db")

# insert data
conn.execute("INSERT INTO table_name (column1, column2, column3, ...) VALUES (value1, value2, value3, ...)")
conn.commit()
```

### 4. Select data

```python
import sqlite3

# create a database
conn = sqlite3.connect("database.db")

# select data
cursor = conn.execute("SELECT column1, column2, column3, ... FROM table_name")
for row in cursor:
    print("column1 = ", row[0])
    print("column2 = ", row[1])
    print("column3 = ", row[2], "\n")
```

### 5. Update data

```python
import sqlite3

# create a database
conn = sqlite3.connect("database.db")

# update data
conn.execute("UPDATE table_name SET column1 = value1, column2 = value2, column3 = value3, ... WHERE condition")
conn.commit()
```

### 6. Delete data

```python
import sqlite3

# create a database
conn = sqlite3.connect("database.db")

# delete data
conn.execute("DELETE FROM table_name WHERE condition")
conn.commit()
```

### 7. Delete table

```python
import sqlite3

#create a database
conn = sqlite3.connect("database.db")

# delete table
conn.execute("DROP TABLE table_name")
conn.commit()
```

### 8. Show data

```python
import sqlite3

# create a database
conn = sqlite3.connect("database.db")

# show data
cursor = conn.execute("SELECT * FROM table_name")
for row in cursor:
    print(row)
```

### 9. Close database

```python
import sqlite3

# create a database
conn = sqlite3.connect("database.db")

# close database
conn.close()
```

### - fetchall

```python
# fetchall
cursor = conn.execute("SELECT * FROM table_name")print(cursor.fetchall())
```
