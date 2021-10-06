# SQLite

---

* 前言

![](https://i.imgur.com/ydtDc8e.jpg)

![](https://i.imgur.com/sqEyuUP.jpg)

![](https://i.imgur.com/lJjuG7E.jpg)

![](https://i.imgur.com/ArHo1xW.jpg)

![](https://i.imgur.com/SGDmTlh.jpg)

---

* 安裝

![](https://i.imgur.com/9QoxhUW.jpg)

`sudo apt-get install sqlite3 libsqlite3-dev`

---

* 使用

![](https://i.imgur.com/ieBZVfx.jpg)

![](https://i.imgur.com/1CRoxST.jpg)

![](https://i.imgur.com/JK1f3Sr.jpg)

```
sqlite3
.quit
```

---

* # 建

![](https://i.imgur.com/596Z5tJ.jpg)

```
sqlite3 資料庫名.db
.open 資料庫名.db
create table person ( name varchar(20) , tel varchar(15) , sex varchar(1) , salary integer );
insert into Table01 (name,email) values ('Jeannie','Jeannie@test.com') ;
```

![](https://i.imgur.com/1XuwJoE.jpg)

```
insert into test values ('11','1111111111'),('22','2222222222'),('33','3333333333');
.schema
```

![](https://i.imgur.com/Oj5QaAI.jpg)

```
.clone
.backup
```

![](https://i.imgur.com/80pOf6m.jpg)

![](https://i.imgur.com/44CohrR.jpg)

```
.headers on 
.Mode csv
.Output  檔名
Select * from table名;
.Quit 
```

到Select * from table名;才算結束

![](https://i.imgur.com/7lg1zdl.jpg)

`sqlite3 -header -csv c:/sqlite/chinook.db "select * from tracks;" > tracks.csv`

![](https://i.imgur.com/zX090YH.jpg)

---

* # 列

![](https://i.imgur.com/TwAXFWh.jpg)

```
.database
.table
select name,id from student;
select * from student;
select * from student where name='Tom';
```

![](https://i.imgur.com/mcYmilx.jpg)

![](https://i.imgur.com/LtQiPB4.jpg)

![](https://i.imgur.com/kDnXcVW.jpg)

`select school.name,school.class,data.name,data.sex,data.year from school inner join data on school.name=data.name;`

---

* # 改

![](https://i.imgur.com/gsRi5Q3.jpg)

`update Table01 set name='Judy',email='Judy@test.com' where id='6' ;`

![](https://i.imgur.com/ZrGMsfA.jpg)

```
ALTER TABLE Customer ADD Gender char(1);
ALTER TABLE Customer change Gender txt;
```

---

* # 存取

![](https://i.imgur.com/aKNMGTo.jpg)

```
sqlite3 資料庫名.db
.open 資料庫名.db
```

---

* # 清

![](https://i.imgur.com/URJvOzW.jpg)

```
delete from student;
delete from person where id='1';
```

![](https://i.imgur.com/TvshjZa.jpg)

```
drop table "表格名";
delete from "表格名;
```

---

* # 條件(where,order by,group by,case...end)

![](https://i.imgur.com/1u9GVSw.jpg)

![](https://i.imgur.com/kVBnrGi.jpg)

![](https://i.imgur.com/05CaInU.jpg)

![](https://i.imgur.com/FeG0X7W.jpg)

`SELECT firstname, lastname, coalesce(company, 'Individual') as entity FROM customers ORDER BY firstname;`

![](https://i.imgur.com/dA5vDxR.jpg)

![](https://i.imgur.com/fVrqQAp.jpg)

![](https://i.imgur.com/26BDIH1.jpg)

![](https://i.imgur.com/pIp98ho.jpg)

`select name,chi ,case when chi>=80 then 'a grade' when chi>=60 then 'b grade' else 'c grade' end as gradechi from school;`

## 統整

![](https://i.imgur.com/bYUOLlm.jpg)

![](https://i.imgur.com/NtHVOyF.jpg)

![](https://i.imgur.com/JwW5FbK.jpg)

---

* # select 數學邏輯運算

![](https://i.imgur.com/tfE9JlI.jpg)

![](https://i.imgur.com/BiuLnwQ.jpg)

![](https://i.imgur.com/kppzJAT.jpg)

![](https://i.imgur.com/FpmOgRg.jpg)

![](https://i.imgur.com/95HR0ld.jpg)

![](https://i.imgur.com/7zU2J8p.jpg)

---

* # .mode 顯示樣式

![](https://i.imgur.com/7Hnm2Ko.jpg)

```
.mode list
.mode
```

![](https://i.imgur.com/5W8ZyzD.jpg)

![](https://i.imgur.com/OdXdNgF.jpg)

![](https://i.imgur.com/KKV9PqX.jpg)

![](https://i.imgur.com/nUK5a1U.jpg)

![](https://i.imgur.com/kfpeZdb.jpg)

![](https://i.imgur.com/fqPCmXN.jpg)

![](https://i.imgur.com/EFVaCTI.jpg)

---

* # 函數

![](https://i.imgur.com/7ZoWsu0.jpg)

![](https://i.imgur.com/y7CQ334.jpg)

![](https://i.imgur.com/qTFkZW2.jpg)

---

* # 字元

![](https://i.imgur.com/lN0GuMY.jpg)

![](https://i.imgur.com/xt2vNgn.jpg)

![](https://i.imgur.com/Yzk06BB.jpg)

![](https://i.imgur.com/4K6MzIM.jpg)

###### tags: `SQL`
