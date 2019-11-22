# Truncate
>
```SQL
SELECT TRUNCATE(SUM(LAT_N),4)
  FROM STATION
 WHERE 38.7880<LAT_N AND LAT_N<137.2345;
```

> https://www.hackerrank.com/challenges/weather-observation-station-14/problem?h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen
```SQL
SELECT TRUNCATE(LAT_N,4)
  FROM STATION
 WHERE LAT_N < 137.2345
ORDER BY LAT_N DESC
LIMIT 1;
```