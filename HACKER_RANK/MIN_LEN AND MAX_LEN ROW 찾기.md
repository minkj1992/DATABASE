# MIN_LEN AND MAX_LEN ROW 찾기

> https://www.hackerrank.com/challenges/weather-observation-station-5/problem?h_r=next-challenge&h_v=zen

```SQL
(SELECT CITY, LENGTH(CITY) AS LEN_CITY
  FROM STATION
 ORDER BY LEN_CITY,CITY
LIMIT 1)
UNION
(SELECT CITY, LENGTH(CITY) AS LEN_CITY
  FROM STATION
 ORDER BY LEN_CITY DESC
LIMIT 1);
```

- 한방에 `ORDER BY`한 뒤에, 맨 위와 맨 밑에 있는 값을 가져오면 안되는 걸까?

```SQL
SELECT A.*
  FROM (
      (SELECT CITY, LENGTH(CITY)
         FROM STATION
        ORDER BY LENGTH(CITY),CITY
       LIMIT 1)
      UNION ALL
      (SELECT CITY, LENGTH(CITY)
         FROM STATION
        ORDER BY LENGTH(CITY) DESC
       LIMIT 1)
  ) AS A;
```