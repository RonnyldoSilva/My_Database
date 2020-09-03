# My notes about Database

This repository is about databases technologies.

## How to install MySQL and config an user root with simple password:
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

If your password does not satisfy the current policy requirements, on mysql prompt runs:
```sql
SHOW VARIABLES LIKE 'validate_password%';

+--------------------------------------+-------+
| Variable_name                        | Value |
+--------------------------------------+-------+
| validate_password.check_user_name    | ON    |
| validate_password.dictionary_file    |       |
| validate_password.length             | 6     |
| validate_password.mixed_case_count   | 1     |
| validate_password.number_count       | 1     |
| validate_password.policy             | LOW   |
| validate_password.special_char_count | 1     |
+--------------------------------------+-------+

SET GLOBAL validate_password_length = 4;
SET GLOBAL validate_password_number_count = 0;
```
