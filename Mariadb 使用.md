# Mariadb 

---

![](https://i.imgur.com/g5kql4Q.jpg)

`sudo mariadb`

![](https://i.imgur.com/A9rF0VH.jpg)

---

* # 建

![](https://i.imgur.com/hb5gcSS.jpg)

```
CREATE TABLE person ( name varchar(20) , tel varchar(15) , sex varchar(1) , salary integer );
ALTER TABLE Customer ADD Gender char(1);
```

![](https://i.imgur.com/tv2PZwM.jpg)

```
insert into Table01 (name,email) values ('Jeannie','Jeannie@test.com') ;
```

![](https://i.imgur.com/tVlKW6N.jpg)

`insert into test values ('11','1111111111'),('22','2222222222'),('33','3333333333');`

![](https://i.imgur.com/exyVFql.jpg)

```
GRANT ALL PRIVILEGES ON *.* TO 'username'@'localhost';
GRANT SELECT,INSERT,UPDATE,DELETE,CREATE ON db_name.* TO 'username'@'localhost';
GRANT ALL PRIVILEGES ON db_name.* TO 'username'@'127.0.0.%';
GRANT ALL ON *.* TO ‘新使用者'@'localhost' IDENTIFIED BY '密碼' WITH GRANT OPTION;
```

---

* # 列

![](https://i.imgur.com/gnNk9P5.jpg)

```
show databases ;
show tables ;
show create table table名稱 ;
desc table名稱 ;
show variables like “%character_set%” ;
show engines ;
show storage engines ;
```

![](https://i.imgur.com/hByIYZh.jpg)

```
select 欄位1,欄位2,… from table名 ;
select * from table名 ;
select * from table名 where 條件 ;
```

![](https://i.imgur.com/wbBfmR7.jpg)

```
SELECT User,Host FROM mysql.user;
SHOW GRANTS FOR 'newuser'@'localhost';
```

---

* # 改

![](https://i.imgur.com/oZPmZjO.jpg)

```
alter table Customer modify sex char(6);
ALTER TABLE Customer CHANGE Address Addr char(50);
```

![](https://i.imgur.com/rhAyblD.jpg)

```
update Table01 set name='Judy',email='Judy@test.com' where id='6‘ ;
```

![](https://i.imgur.com/mMNU1jb.jpg)

![](https://i.imgur.com/9uh22qZ.jpg)

```
mariadb –u登入使用者  -p
SET PASSWORD FOR ‘登入使用者 ’@‘主機’ = PASSWORD(‘新密碼');

sudo mariadb
SET PASSWORD FOR ‘登入使用者 ’@‘主機’ = PASSWORD(‘新密碼');

mysqladmin -u 使用者 -p‘原密碼' password '新密碼'
```

---

* # 存

![](https://i.imgur.com/O0FIx00.jpg)

`flush privileges;`

---

* # 取

![](https://i.imgur.com/OmoR7PC.jpg)

---

* # 清

![](https://i.imgur.com/qWxeOVz.jpg)

```
ALTER TABLE Customer DROP Gender;
delete from table名
delete from customer where id='1'
```

---

* # 字元

![](https://i.imgur.com/XmVrDjw.jpg)

![](https://i.imgur.com/VTEcska.jpg)

![](https://i.imgur.com/5BPz9Ra.jpg)

![](https://i.imgur.com/YcZVpNX.jpg)

![](https://i.imgur.com/dVHMzrb.jpg)

![](https://i.imgur.com/0Hs6yHg.jpg)

###### tags: `SQL`
