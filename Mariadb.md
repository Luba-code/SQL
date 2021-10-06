# Mariadb 安裝

---

![](https://i.imgur.com/LX9Unvz.jpg)

```
sudo apt update
sudo apt upgrade  -y
sudo apt install mariadb-server 
sudo mysql_secure_installation
```

![](https://i.imgur.com/tRoU8qS.jpg)

![](https://i.imgur.com/5nyFYsF.jpg)

![](https://i.imgur.com/cDvkpl7.jpg)

![](https://i.imgur.com/K7rMxQa.jpg)

![](https://i.imgur.com/bkpUIMA.jpg)

![](https://i.imgur.com/c25vthO.jpg)

![](https://i.imgur.com/zgi2Npj.jpg)

---

* # 建立具有root權限的帳號

![](https://i.imgur.com/X7Tb9oA.jpg)

![](https://i.imgur.com/a92a9Na.jpg)

`sudo mariadb`

![](https://i.imgur.com/XGAMNAv.jpg)

```
GRANT ALL ON *.* TO 'admin'@'localhost' IDENTIFIED BY 'password' WITH GRANT OPTION;
FLUSH PRIVILEGES;
exit
```
![](https://i.imgur.com/Cyt8T0O.jpg)

```
sudo systemctl status mariadb
sudo systemctl start mariadb
```

![](https://i.imgur.com/MJzALVh.jpg)

開啟Mariadb的狀態

![](https://i.imgur.com/FxWszSq.jpg)

關閉Mariadb的狀態

###### tags: `SQL`
