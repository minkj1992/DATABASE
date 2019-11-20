# 총 ROW - 총 UNQ ROW
> https://www.hackerrank.com/challenges/weather-observation-station-4/problem

```SQL
SELECT COUNT(CITY)- (SELECT COUNT(DISTINCT CITY) FROM STATION)
  FROM STATION;
```

```SQL
SELECT COUNT(CITY)-COUNT(DISTINCT CITY)
  FROM STATION;
```

