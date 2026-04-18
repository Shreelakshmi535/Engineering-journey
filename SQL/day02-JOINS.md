\# Day 2 — SQL JOINs



\## 4 Types of JOINs



INNER JOIN → only matching rows from both tables

LEFT JOIN  → all rows from left + matching from right

RIGHT JOIN → all rows from right + matching from left

FULL JOIN  → everyone from both tables



\## Golden Rule

No match = NULL appears in result



\## Syntax

SELECT s.name, c.course\_name

FROM students s

INNER JOIN courses c ON s.id = c.student\_id;



\## When to use which

INNER → when you need only complete matches

LEFT  → when you need all records from main table

RIGHT → when you need all records from second table

FULL  → when you need everything from both tables

