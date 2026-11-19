# Notes

- Database normalization minimizes duplicate data in any single table, and allows for data in the database to grow independently of each other
- `INNER JOIN` results in a table only containing data that belongs in both of the tables
- If the two tables have asymmetric data, which can easily happen when data is entered in different stages, then we would have to use a LEFT JOIN, RIGHT JOIN or FULL JOIN instead to ensure that the data you need is not left out of the results. When joining table A to table B....
  - a LEFT JOIN includes rows from A regardless of whether a matching row is found in B.
  - a RIGHT JOIN is the same as LEFT JOIN, but reversed, keeping rows in B regardless of whether a match is found in A.
  - a FULL JOIN means that rows from both tables are kept, regardless of whether a matching row exists in the other table.
- common aggregate functions:
  - COUNT
  - MIN
  - MAX
  - AVG
  - SUM
- HAVING is used to filter GROUP BY groups
- Order of execution:
  1. FROM and JOIN
  2. WHERE
  3. GROUP BY
  4. HAVING
  5. SELECT
  6. DISTINCT
  7. ORDER BY
  8. LIMIT and OFFSET
- [PostgreSQL 19 data types](https://www.postgresql.org/docs/19/datatype.html)
- [MySQL 26.10 data types](https://dev.mysql.com/doc/refman/26.10/en/data-types.html)
- Common data types:
  - integer
  - boolean
  - float
  - double
  - real
  - character
  - varchar
  - text
  - date
  - datetime
  - blob
- Common table constraints:
  - primary key
  - autoincrement
  - unique
  - not null
  - check
  - foreign key
- Altering tables:
  - adding columns:
    ```SQL
    ALTER TABLE mytable
    ADD column DataType OptionalTableConstraint
    DEFAULT default_value;
    ```
  - dropping columns:
    ```SQL
    ALTER TABLE mytable
    DROP column_to_be_deleted;
    ```
  - renaming tables:
    ```SQL
    ALTER TABLE mytable
    RENAME TO new_table_name;
    ```