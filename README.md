# My notes about Database

This repository is about databases technologies.

## MySQL, how to install and config an user root with simple password, just for train:
Install on Ubuntu:
```sql
sudo apt update
sudo apt install mysql-server
sudo mysql_secure_installation
### set password "root"
```

Config the user root with "root" as password, on terminal runs `mysql -u root -p`. On mysql prompt runs:
```mysql
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'root';
flush privileges;
```
