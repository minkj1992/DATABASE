> https://www.hackerrank.com/challenges/the-blunder/problem?h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen

- 문제가 이상한게, 모든 값을 계산한 후에, ROUND 시키라 했으면서 정답은 `CEILING`시켜야 나오도록 해놓았다.

```SQL
SELECT ROUND(AVG(Salary))-ROUND(AVG(REPLACE(Salary,0,'')))
  FROM EMPLOYEES;
```

```SQL
SELECT CAST(CEILING(AVG(CAST(Salary as Float))-AVG(CAST(REPLACE(CAST(Salary AS VARCHAR(10)),'0','') AS FLOAT))) AS INT)
FROM Employees
```