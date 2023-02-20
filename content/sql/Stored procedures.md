---
title: "Stored Procedures"
date: 2023-02-20T15:14:52+08:00
weight: 4
draft: false
---

### Defining Stored Programs in MySQL

If you use the mysql client program to define a stored program containing semicolon characters, a problem arises. By default, mysql itself recognizes the semicolon as a statement delimiter, so you must redefine the delimiter temporarily to cause mysql to pass the entire stored program definition to the server. To redefine the mysql delimiter, use the delimiter command. See also [MySQL Reference manual](https://dev.mysql.com/doc/refman/8.0/en/stored-programs-defining.html).

``` bash
mysql> delimiter //

mysql> CREATE PROCEDURE dorepeat(p1 INT)
    -> BEGIN
    ->   SET @x = 0;
    ->   REPEAT SET @x = @x + 1; UNTIL @x > p1 END REPEAT;
    -> END
    -> //
Query OK, 0 rows affected (0.00 sec)

mysql> delimiter ;
```
