---
title: "Common Expressions"
date: 2023-02-20T14:40:19+08:00
weight: 1
draft: false
---

### CASE

``` sql
CASE
    WHEN condition1 THEN result1
    WHEN condition2 THEN result2
    WHEN conditionN THEN resultN
    ELSE result
END;
```

The CASE expression goes through conditions and returns a value when the first condition is met (like an if-then-else statement). So, once a condition is true, it will stop reading and return the result. If no conditions are true, it returns the value in the ELSE clause.If there is no ELSE part and no conditions are true, it returns NULL. See also [w3schools](https://www.w3schools.com/sql/sql_case.asp).
