# TOP Earners

> https://www.hackerrank.com/challenges/earnings-of-employees/problem?h_r%5B%5D=next-challenge&h_r%5B%5D=next-challenge&h_r%5B%5D=next-challenge&h_r%5B%5D=next-challenge&h_v%5B%5D=zen&h_v%5B%5D=zen&h_v%5B%5D=zen&h_v%5B%5D=zen

```SQL
SELECT A.sm, A.cnt
    FROM (SELECT salary * months AS sm , COUNT(*) as cnt
            FROM Employee
           GROUP BY sm
          ORDER BY sm DESC
          LIMIT 1) A
```
- MYSQL에는 RANK() 함수가 없다고?? 헐 ..
- [PARTITION BY를 대체하는 ,공부하면 좋을 링크](https://rampart81.github.io/post/mysql_get_row_position/)

```SQL
SELECT MAX(salary * months), COUNT(*)
  FROM employee
 GROUP BY salary*months
ORDER BY salary*months DESC;
```

```SQL
SELECT salary * months as sm, COUNT(*)
  FROM employee
 GROUP BY sm
ORDER BY sm DESC
LIMIT 1;
```

- **MAX를 사용하지 않고, ORDER 이후 LIMIT 1 넣어주는 것이 훨씬 깔끔하다.**