---
title: "Trigger"
date: 2023-02-22T15:03:28+08:00
weight: 4
draft: False
---

### Creating Trigger

``` bash
mysql> CREATE TRIGGER ins_sum 
       BEFORE INSERT
       ON account
       FOR EACH ROW
       SET @sum = @sum + NEW.amount;
```

### Show Trigger

``` bash
mysql> SHOW TRIGGERS;
```

### Dropping Trigger

``` bash
mysql> DROP TRIGGER IF EXISTS test.ins_sum;
```

### OLD and NEW Extensions

Within the trigger body, the `OLD` and `NEW` keywords enable you to access columns in the rows affected by a trigger. `OLD` and `NEW` are MySQL extensions to triggers; they are not case-sensitive.

{{< hint warning >}}
In a `BEFORE` trigger, the `NEW` value for an `AUTO_INCREMENT` column is `0`, not the sequence number that is generated automatically when the new row **actually** is inserted.
{{< /hint >}}

```bash
mysql> delimiter //
mysql> CREATE TRIGGER upd_check BEFORE UPDATE ON account
       FOR EACH ROW
       BEGIN
           IF NEW.amount < 0 THEN
               SET NEW.amount = 0;
           ELSEIF NEW.amount > 100 THEN
               SET NEW.amount = 100;
           END IF;
       END;//
mysql> delimiter ;
```

### Attention

{{< hint danger >}}
In the trigger, we can modify the data in any tables except the table that this trigger is for. Otherwise it will end in an infinite loop, because this trigger will fire itself.
{{< /hint >}}

### Reference

- [MySQL Reference Manual](https://dev.mysql.com/doc/refman/8.0/en/trigger-syntax.html).
