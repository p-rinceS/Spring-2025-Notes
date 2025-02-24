
if <font color="#9bbb59">DISTINCT</font> is specified in the [[SELECT]] clause then duplicate results are eliminated

(similar to [[set]])

```SQL
SELECT DISTINCT deptname FROM student;
```


| deptname   |
| ---------- |
| Physics    |
| Biology    |
| Elec. Eng. |
| Finance    |
| Comp. Sci. |
| History    |
| Music      |


[[UNIQUE]] keyword vs DISTINCT 

Unique prevents two records from having identical values in a column. The DISTINCT keyword in SQL helps to eliminate duplicate values while retrieving the data

DISTINCT is for [[QUERIES]]

[[UNIQUE]] is for [[CONSTRAINTS]]