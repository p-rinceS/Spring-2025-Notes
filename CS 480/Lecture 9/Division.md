


### Intuition


Compare integer division **$n \div m$** is the largest u such that  $u * m < n$


### **Takes**

| Student | Course |
| ------- | ------ |
| Bob     | CS480  |
| Bob     | CS100  |
| Alice   | CS480  |

$\div$

### **Courses**

| Course |
| ------ |
| CS480  |
| CS100  |

### **Output**:

| Student |
| ------- |
| Bob     |

---

#### When you hear "All"

Think division.
The example above shows that the output is only any student that has taken ALL of the courses in table *courses*



---
## Formal Definition


Division $R \div S$

$— Sch(S) ⊂ Sch(R)$

Given a relational algebra expression $R \div S$ and database $D$. Let $U$ = $Sch(R) - Sch(S)$.
	
$E1 ← πU(R)$
$E2 ← πU((E1 × S) − πU,Sch(S) (R ▷◁ S))$
$R  ÷  S ≡ E1 − E2$




