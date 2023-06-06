---
title: "Oracle"
date: 2023-06-06T15:16:42+08:00
draft: false
---

## Find duplicates

``` sql
SELECT column_name, COUNT(column_name)
FROM table_name
GROUP BY column_name
HAVING COUNT(column_name) > 1;
```

See also [How do I find duplicate values in a table in Oracle?](https://stackoverflow.com/questions/59232/how-do-i-find-duplicate-values-in-a-table-in-oracle).

## Removing duplicates

``` sql
DELETE FROM your_table
WHERE rowid not in
(SELECT MIN(rowid)
FROM your_table
GROUP BY column1, column2, column3);
```

See also [Removing duplicate rows from table in Oracle](https://stackoverflow.com/questions/529098/removing-duplicate-rows-from-table-in-oracle).
