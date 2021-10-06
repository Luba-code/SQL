# Mariadb 匯入檔案

---

![](https://i.imgur.com/upa2xc7.jpg)

`sudo mariadb`

![](https://i.imgur.com/wBiAxPc.jpg)

`show variables like "%character_set%";`

![](https://i.imgur.com/x7lyTj2.jpg)

建立資料庫，使用資料庫

![](https://i.imgur.com/p3sANLA.jpg)

```
use test
create table cust (name varchar(10),age integer(3), sex varchar(1));
```

```
LOAD DATA LOCAL INFILE  '/home/bigred/datac1.csv'
INTO TABLE cust
CHARACTER SET UTF8
FIELDS TERMINATED BY ','
ENCLOSED BY '"'
LINES TERMINATED BY '\n'
IGNORE 1 ROWS;
```

![](https://i.imgur.com/OkCx2vQ.jpg)

###### tags: `SQL`
