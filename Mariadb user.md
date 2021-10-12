# Mariadb user

---

![](https://i.imgur.com/OsYXx1z.jpg)

```
CREATE USER '新使用者'@'localhost' IDENTIFIED BY '新使用者密碼';
GRANT ALL PRIVILEGES ON *.* TO '使用者'@'localhost';
GRANT SELECT,INSERT,UPDATE,DELETE,CREATE ON db_name.* TO 'username'@'localhost';
GRANT ALL ON *.* TO '新使用者'@'localhost' IDENTIFIED BY '密碼' WITH GRANT OPTION;
```

![](https://i.imgur.com/BWlpqtW.jpg)

```
SELECT User,Host FROM mysql.user;
SHOW GRANTS FOR 'newuser'@'localhost';
```

![](https://i.imgur.com/Mfyk8vS.jpg)

![](https://i.imgur.com/DgthSZF.jpg)

![](https://i.imgur.com/kMfgswl.jpg)

```
DROP USER '既有使用者'@'localhost';
revoke all privileges on *.* from '使用者'@'localhost';
```

###### tags: `SQL`
