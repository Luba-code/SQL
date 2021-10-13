# Mariadb 練習

---

![](https://i.imgur.com/30lA1rJ.jpg)

```
create database data;
use data;
create table member (name char(8),tel char(10),email char(20));
show databases;
show tables;
insert into member values ("john","0912345678","john@gmail.com"),("marry","0987654321","marry@gmail.com"),("tom","0987098765","tom@gmail.com"),("wang","0966684281","wang@gmail.com");
select * from member;
```

![](https://i.imgur.com/rI3P5AR.jpg)


![](https://i.imgur.com/bOmL2NL.jpg)

```
alter table member add sex char(1);
update member set sex='M' where name='john';
update  member set sex="F" where name="marry";
update  member set sex="M" where name="tom";
update  member set sex="M" where name="wang";
```

![](https://i.imgur.com/IStY7yl.jpg)

```
insert into member (name,tel,email,sex) values ('victor','0968765123','victor@gmail.com','M');
update member set tel='0986345678' where name='john';
alter table member add id char(3);
update member set id='001' where name='john';
update member set id='002' where name='marry';
update member set id='003' where name='tom';
update member set id='004' where name='wang';
update member set id='005' where name='victor';
```

![](https://i.imgur.com/LkKrV8G.jpg)

* 6

`select count(*) from member;`

* 7

`select count(*) from member where sex="M";`

* 8

`select * from member where id="003";`

* 9

`select tel,email from member where name="victor";`

* 10

`delete from member where id='003';`

* 11

`desc member;`

![](https://i.imgur.com/pranfw1.jpg)

![](https://i.imgur.com/1tgXWLx.jpg)

* 12

`alter table member modify name char(10);`

* 13

`desc member;`

* 14

`alter table member change id no integer;`

* 15

`desc member;`

* 16

`select * from member;`

![](https://i.imgur.com/UvYh0Jm.jpg)


###### tags: `SQL`
