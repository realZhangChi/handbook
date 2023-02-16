---
title: "Transations"
date: 2023-02-16T14:12:36+08:00
weight: 2
draft: false
---

## Usage

``` bash
> MULTI
OK
> INCR foo
QUEUED
> INCR bar
QUEUED
> EXEC
1) (integer) 1
2) (integer) 1
```

## DISCARD

``` bash
> SET foo 1
OK
> MULTI
OK
> INCR foo
QUEUED
> DISCARD
OK
> GET foo
"1"
```

## Optimistic locking using check-and-set

``` bash
WATCH mykey
val = GET mykey
val = val + 1
MULTI
SET mykey $val
EXEC
```

## See also

[Transaction | Redis](https://redis.io/docs/manual/transactions/).