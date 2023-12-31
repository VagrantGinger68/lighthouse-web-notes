## POSTGRESQL

PostgreSQL is an advanced, enterprise-class, and open-source relational database system. PostgreSQL supports both SQL (relational) and JSON (non-relational) querying.

Data is stored in tables
```sql
CREATE TABLE famous_people (
  id SERIAL PRIMARY KEY,
  first_name VARCHAR(50),
  last_name VARCHAR(50),
  birthdate DATE
);
```

Data is inserted into the tables
```sql
INSERT INTO famous_people (first_name, last_name, birthdate)
  VALUES ('Abraham', 'Lincoln', '1809-02-12');
INSERT INTO famous_people (first_name, last_name, birthdate)
  VALUES ('Mahatma', 'Gandhi', '1869-10-02');
INSERT INTO famous_people (first_name, last_name, birthdate)
  VALUES ('Paul', 'Rudd', '1969-04-06');
INSERT INTO famous_people (first_name, last_name, birthdate)
  VALUES ('Paul', 'Giamatti', '1967-06-06');
```

The tables can be searched for specific data
```sql
SELECT * FROM famous_people; -- should give us back all 4
```

```sql
SELECT * FROM famous_people WHERE birthdate < '1920-01-01';
```

Tables can be joined
```js
SELECT students.name as student_name, email, cohorts.name as cohort_name
FROM cohorts JOIN students ON cohort_id = cohorts.id;
```
An INNER JOIN will only give us rows where there is a match between the two tables.

Left Outer Join
```sql
SELECT students.name as student_name, email, cohorts.name as cohort_name
FROM students LEFT OUTER JOIN cohorts ON cohorts.id = cohort_id;
```
The LEFT OUTER JOIN will return all of the students, even ones without a cohort_id.

Right Outer Join
```sql
SELECT students.name as student_name, email, cohorts.name as cohort_name
FROM students RIGHT OUTER JOIN cohorts ON cohorts.id = cohort_id;
```
The RIGHT OUTER JOIN will return all cohorts, even ones without any students enrolled.

Full Outer Join
```sql
SELECT students.name as student_name, email, cohorts.name as cohort_name
FROM students FULL OUTER JOIN cohorts ON cohorts.id = cohort_id;
```
The FULL OUTER JOIN will return all cohorts and all students, even when there is no match.

Visual representation of Joining tables: 
https://blog.codinghorror.com/a-visual-explanation-of-sql-joins/

Group by:
```sql
SELECT students.name as student, count(assignment_submissions.*) as total_submissions
FROM assignment_submissions
JOIN students ON students.id = student_id
WHERE students.end_date IS NULL
GROUP BY students.name;
```

Having:
```sql
SELECT students.name as student, count(assignment_submissions.*) as total_submissions
FROM assignment_submissions
JOIN students ON students.id = student_id
WHERE students.end_date IS NULL
GROUP BY students.name
HAVING count(assignment_submissions.*) < 100;
```

Using sub queries can be done as a column in SELECT,FROM sub select table, or search within a result set IN.

As a column in SELECT:
```sql
SELECT (
  SELECT count(*)
  FROM table_name
) as total, other_column
FROM other_table_name
ORDER BY total;
```

FROM sub select table:
```sql
SELECT avg(total_students) as average_students
FROM (
  SELECT count(students) as total_students, cohorts.name as cohort_name
  FROM students
  JOIN cohorts on cohorts.id = cohort_id
  GROUP BY cohorts.name
) as totals_table;
```

Search within a result set IN:
```sql
SELECT * FROM table
WHERE id IN (
  SELECT something_id
  FROM someTable
  WHERE something
);
```