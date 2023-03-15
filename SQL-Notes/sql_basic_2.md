## SQL Basics - 2 🚀👩‍🚀

### - "WHERE" clause

- "WHERE" clause is used to filter the records based on some condition.
  example:

```sql
SELECT * FROM table_name WHERE column_name = value;
```

- "WHERE" clause can be used with "AND" and "OR" operators.
  example:

```sql
SELECT * FROM table_name WHERE column_name = value AND column_name = value;
SELECT * FROM table_name WHERE column_name = value OR column_name = value;
```

- "WHERE" clause can be used with "IN" operator.
- "IN" operator is used to specify multiple values in a "WHERE" clause.
  example:

```sql
SELECT * FROM table_name WHERE column_name IN (value1, value2, value3);
```

- "WHERE" clause can be used with "BETWEEN" operator.
- "BETWEEN" operator is used to specify a range of values in a "WHERE" clause.
  example:

```sql
SELECT * FROM table_name WHERE column_name BETWEEN value1 AND value2;
```

- "WHERE" clause can be used with "LIKE" operator.
- "LIKE" operator is used to search for a pattern in a "WHERE" clause.
  example:

```sql
SELECT * FROM table_name WHERE column_name LIKE 'value%';
```

- "WHERE" clause can be used with "NOT" operator.
  example:

```sql
SELECT * FROM table_name WHERE NOT column_name = value;
```

- "WHERE" clause can be used with "IS NULL" operator.
  example:

```sql
SELECT * FROM table_name WHERE column_name IS NULL;
```

- "WHERE" clause can be used with "IS NOT NULL" operator.
  example:

```sql
SELECT * FROM table_name WHERE column_name IS NOT NULL;
```

- "WHERE" clause can be used with "ORDER BY" clause.
  example:

```sql
SELECT * FROM table_name WHERE column_name = value ORDER BY column_name;
```

- "WHERE" clause can be used with "GROUP BY" clause.
- "GROUP BY" clause is used to group the result-set by one or more columns.
  example:

```sql
SELECT * FROM table_name WHERE column_name = value GROUP BY column_name;
```

### Table of Where Clause Operators

| Operator | Description                                                                 |
| -------- | --------------------------------------------------------------------------- |
| =        | Equal                                                                       |
| >        | Greater than                                                                |
| <        | Less than                                                                   |
| >=       | Greater than or equal                                                       |
| <=       | Less than or equal                                                          |
| <>       | Not equal. Note: In some versions of SQL this operator may be written as != |
| BETWEEN  | Between a certain range                                                     |
| LIKE     | Search for a pattern                                                        |
| IN       | To specify multiple possible values for a column                            |
