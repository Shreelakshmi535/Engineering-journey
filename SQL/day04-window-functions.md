\# Day 4 — Window Functions



\## Syntax

FUNCTION() OVER (PARTITION BY col ORDER BY col)



\## Functions

ROW\_NUMBER() → unique number, resets per partition

RANK()       → ties get same rank, skips next number

DENSE\_RANK() → ties get same rank, no skipping

LAG(col)     → previous row value (NULL for first row)

LEAD(col)    → next row value (NULL for last row)



\## Key difference

GROUP BY  → collapses rows, lose detail

Window    → keeps all rows, adds calculation



\## Real use cases

LAG → month over month comparison

ROW\_NUMBER → get top 1 per group

RANK → leaderboard rankings

