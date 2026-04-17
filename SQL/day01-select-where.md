\# Day 1 — SQL Fundamentals



\## Concepts Learned

\- SELECT → picks which columns to show

\- WHERE → filters rows before grouping

\- ORDER BY → sorts results (ASC = low to high, DESC = high to low)

\- DISTINCT → removes duplicate values

\- GROUP BY → groups rows together

\- HAVING → filters after grouping

\- COUNT(\*) → counts rows in each group

\- AND / OR → combine multiple conditions

\- AS → gives a column a nickname (alias)



\## Golden Rule — SQL Clause Order

SELECT → FROM → WHERE → GROUP BY → HAVING → ORDER BY → LIMIT



\## Memory Trick

"Some Friendly Whales Go Home Often Late"



\## Queries I Practiced



\-- Basic SELECT

SELECT \* FROM students;

SELECT name, city FROM students;



\-- WHERE conditions

SELECT \* FROM students WHERE city = 'Dallas';

SELECT \* FROM students WHERE age > 23;



\-- AND / OR

SELECT \* FROM students WHERE city = 'Dallas' AND grade = 'A';

SELECT \* FROM students WHERE city = 'Dallas' OR city = 'Houston';



\-- ORDER BY

SELECT \* FROM students ORDER BY age ASC;

SELECT \* FROM students ORDER BY age DESC;



\-- DISTINCT

SELECT DISTINCT city FROM students;



\-- GROUP BY + COUNT

SELECT city, COUNT(\*) as total\_students

FROM students

GROUP BY city;



\-- HAVING

SELECT city, COUNT(\*) as total\_students

FROM students

GROUP BY city

HAVING COUNT(\*) > 1;



\-- WHERE + GROUP BY + HAVING combined

SELECT city, COUNT(\*) as total\_grade\_a

FROM students

WHERE grade = 'A'

GROUP BY city

HAVING COUNT(\*) > 1

ORDER BY city;



\## Mistakes I Made Today

\- Forgot GROUP BY must come before HAVING

\- Used count(grade='A') instead of WHERE grade='A'

\- Table name typo — "student" instead of "students"



\## What I Will Learn Next

\- JOINs — INNER, LEFT, RIGHT, FULL, SELF, CROSS

