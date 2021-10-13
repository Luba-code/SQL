# SQlite 練習

---

![](https://i.imgur.com/wLcVikc.jpg)

![](https://i.imgur.com/5oV2QIg.jpg)

![](https://i.imgur.com/vD5nRhr.jpg)

```
.open sale.db
create table product ( pid txt ,cost integer ,price integer );
insert into product (pid,cost,price) values ('a1',100,200),('a2',110,220),('b1',200,400),('b2',210,420);
create table cust ( cid txt ,name integer ,sex txt ,tel integer);
insert into cust (cid,name,sex,tel) values ('001','john','M',0931234567),('002','mary','F',0988765234),('003','victor','M',0923456789);
create table bill ( pid txt ,cid txt ,qty integer);
insert into bill (pid,cid,qty) values ('a1','001',10),('b1','001',20),('a2','002',30),('b2','003',40),('a1','001',50),('a2','002',60),('b1','003',70),('b2','003',80);
```

![](https://i.imgur.com/HajWzmN.jpg)

`select cid,product.pid,product.price,qty from bill inner join product on product.pid = bill.pid;`

![](https://i.imgur.com/05Y93FI.jpg)

`select cid,product.pid,product.price,qty,(product.price*qty) as total from bill inner join product on product.pid = bill.pid;`

![](https://i.imgur.com/dPzJlTV.jpg)

`select cid,product.pid,product.price,qty,(product.price*qty) as total,product.cost,(price-cost)*qty as net from bill inner join product on product.pid = bill.pid;`

![](https://i.imgur.com/ckvNZpF.jpg)


![](https://i.imgur.com/fU3Kejo.jpg)

7.

`select sum(product.price*qty) as total,sum(product.price-product.cost)*qty as net from bill inner join product on product.pid = bill.pid;`

8.

`select sum(product.price*qty) as total,sum(product.price-product.cost)*qty as net from bill inner join product on product.pid = bill.pid group by product.pid;`

9.

`select cust.name,sum(product.price*qty) as total from bill inner join product on product.pid = bill.pid inner join cust on cust.cid=bill.cid group by cust.name;`

10.

`select cust.name,tel from bill inner join product on product.pid = bill.pid inner join cust on cust.cid=bill.cid group by cust.name having sum(product.price*qty) order by (product.price*qty) desc limit 1;`

![](https://i.imgur.com/x69OJWg.jpg)


###### tags: `SQL`
