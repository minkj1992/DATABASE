# Average Population of Each Continent
> [link](https://www.hackerrank.com/challenges/average-population-of-each-continent/problem)

- `FROM A,B`: A와B에 대한 INNER JOIN을 뜻하게 된다.
    - `A,B`의 경우 FOREIGN KEY는 WHERE을 통하여
    - `A JOIN B`의 경우 `ON`을 활용하여 테이블을 JOIN시켜준다.
    
    - 
    ```sql
    SELECT COUNTRY.CONTINENT, FLOOR(AVG(CITY.POPULATION))
    FROM COUNTRY, CITY
    WHERE COUNTRY.CODE = CITY.COUNTRYCODE
    GROUP BY COUNTRY.CONTINENT;
    ```

    - 
    ```sql
    SELECT COUNTRY.CONTINENT, FLOOR(AVG(CITY.POPULATION))
    FROM COUNTRY JOIN CITY ON COUNTRY.CODE = CITY.COUNTRYCODE
    GROUP BY COUNTRY.CONTINENT;

    ```

