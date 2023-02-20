---
title: "Common Functions"
date: 2023-02-20T14:24:02+08:00
weight: 2
draft: false
---

### COALESCE

``` sql
SELECT COALESCE(NULL, NULL, NULL, 'W3Schools.com', NULL, 'Example.com');
```

Return the first non-null value in a list. See also [w3schools](https://www.w3schools.com/sql/func_mysql_coalesce.asp).

### IFNULL

``` sql
SELECT IFNULL(NULL, "W3Schools.com");
```

Return the specified value IF the expression is NULL, otherwise return the expression. See also [w3schools](https://www.w3schools.com/sql/func_mysql_ifnull.asp).

### IF

``` sql
SELECT IF(500<1000, "YES", "NO");
```

The IF() function returns a value if a condition is TRUE, or another value if a condition is FALSE. See also [w3schools](https://www.w3schools.com/sql/func_mysql_if.asp).
