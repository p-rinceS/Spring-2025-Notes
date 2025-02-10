

Allows us to reference tuples from table R' from in table R. Similar to pointers/references in programming languages.



R1

| ID  | Name     | Deptname |
| --- | -------- | -------- |
| 1   | Juan     | CS       |
| 2   | Ahmed    | CS       |
| 3   | Sung-woo | STATS    |
| 4   | Onyinye  | CS       |

R'

| dName | building | budget  |
| ----- | -------- | ------- |
| CS    | Taylor   | 1000000 |
| STATS | Taylor   | 300000  |
| CHEM  | Westin   | 600000  |


R1's DeptName is a foreign key referencing table R'.