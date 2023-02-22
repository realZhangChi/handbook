---
title: "Event"
date: 2023-02-22T15:44:14+08:00
weight: 1
draft: true
---

### Creating Event

``` sql
CREATE
    [DEFINER = user]
    EVENT
    [IF NOT EXISTS]
    event_name
    ON SCHEDULE schedule
    [ON COMPLETION [NOT] PRESERVE]
    [ENABLE | DISABLE | DISABLE ON SLAVE]
    [COMMENT 'string']
    DO event_body;

schedule: {
    AT timestamp [+ INTERVAL interval] ...
  | EVERY interval
    [STARTS timestamp [+ INTERVAL interval] ...]
    [ENDS timestamp [+ INTERVAL interval] ...]
}

interval:
    quantity {YEAR | QUARTER | MONTH | DAY | HOUR | MINUTE |
              WEEK | SECOND | YEAR_MONTH | DAY_HOUR | DAY_MINUTE |
              DAY_SECOND | HOUR_MINUTE | HOUR_SECOND | MINUTE_SECOND}
```

### Show Event

``` bash
mysql> SHOW EVENTS;
```

### Dropping Event

``` bash
mysql> DROP EVENT IF EXISTS event_name;
```

### Temporarily Disable/Enable

``` sql
ALTER EVENT event_name [ENABLE | DISABLE]
```

### Reference

- [MySQL Reference Manual](https://dev.mysql.com/doc/refman/8.0/en/create-event.html)
