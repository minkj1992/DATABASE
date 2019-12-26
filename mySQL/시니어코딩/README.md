# 시니어코딩
> https://www.youtube.com/watch?v=5Iw8ijN5coc&list=PLEOnZ6GeucBU7FR26mn9d3Mxqc8V81yHX

## MySQL 01 - Database 및 User 생성하기
> https://docs.google.com/presentation/d/1Z4Ny2Izts9RZBFNq-0zmCeKTFocJSbcD2i88jrdcX-4/edit#slide=id.g48636eabed_0_13
- DB 생성하기
```sql
> mysql -u root -p
> create database dooodb;
> show databases;
> drop database doodb;
> use doodb;
> show tables;
```

- USER + HOST 생성하기
    - User 생성
        ```sql
        mysql> create user <user-name>@'<host>' identified by '<password>';
        mysql> create user dooo@'%' identified by 'dooo!';
        mysql> create user dooo@'211.234.55.66' identified by 'dooo!';
        ```

## MySQL 02 - Table생성, 한글 설정, Session개념
> https://docs.google.com/presentation/d/1Z4Ny2Izts9RZBFNq-0zmCeKTFocJSbcD2i88jrdcX-4/edit#slide=id.p

- [time_zone 에러](http://infondgndg91.blogspot.com/2018/01/mysql-timezone-asiaseoul.html)

```sql
-- 현재 db가 연결되어있는 세션들 리스트
> show processlist;
```