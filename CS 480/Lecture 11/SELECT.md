
the <font color="#9bbb59">SELECT</font> clause consists of a list of projection expressions and optional renaming `(AS)`

determines what will be returned by the query

also handles aggregation

`SELECT name AS age / 10 AS decades`

``` SQL
SELECT name
	FROM student
LIMIT 3;
```

| name    |
| ------- |
| Zhang   |
| Shankar |
| Brandt  |


```SQL
SELECT credits * 12 AS morecred, title
	FROM course
LIMIT 3;
```



