---
title: "Common commands"
date: 2023-02-15T09:20:58+08:00
draft: false
---

## Redis common commands

### Database

{{< columns >}} 
#### DBSIZE
```
DBSIZE
```
Return the number of keys in the currently-selected database. see also [https://redis.io/commands/dbsize/](https://redis.io/commands/dbsize/)

<---> 

#### FLUSHALL
```
FLUSHALL [ASYNC | SYNC]
```
Remove all keys from all database. see also [https://redis.io/commands/flushall/](https://redis.io/commands/flushall/)

<---> 

#### FLUSHDB
```
FLUSHDB [ASYNC | SYNC]
```
Remove all keys from the current database. see also [https://redis.io/commands/flushdb/](https://redis.io/commands/flushdb/)

{{< /columns >}}

{{< columns >}}

#### SELECT
```
SELECT index
```
Change the selected database for the current connection. see also [https://redis.io/commands/select/](https://redis.io/commands/select/)

{{< /columns >}}

### KEY

{{< columns >}}

#### KEYS
```
KEYS pattern
```
Returns all keys matching pattern. See also [https://redis.io/commands/keys/](https://redis.io/commands/keys/)

<---> 

#### EXISTS
```
EXISTS key [key ...]
```
Determine if a key exists. See also [https://redis.io/commands/exists/](https://redis.io/commands/exists/)

<--->

#### EXPIRE
```
EXPIRE key seconds [NX | XX | GT | LT]
```
Set a key's time to live in seconds. See also [https://redis.io/commands/expire/](https://redis.io/commands/expire/)

{{< /columns >}}

{{< columns >}}

#### TTL
```
TTL key
```
Get the time to live for a key in seconds. See also [https://redis.io/commands/ttl/](https://redis.io/commands/ttl/)

<--->

#### TYPE
```
TYPE key
```
Determine the type stored at key. See also [https://redis.io/commands/type/](https://redis.io/commands/type/)

<--->

#### STRLEN
```
STRLEN key
```
Get the length of the value stored in a key. See also [https://redis.io/commands/strlen/](https://redis.io/commands/strlen/)

{{< /columns >}}

### VALUE

{{< columns >}}

#### GET
```
GET key
```
Get the value of a key. See also [https://redis.io/commands/get/](https://redis.io/commands/get/)

<--->

#### APPEND
```
APPEND key value
```
Append a value to a key. See also [https://redis.io/commands/append/](https://redis.io/commands/append/)

<--->

#### INCR
```
INCR key
```
Increment the integer value of a key by one. See also [https://redis.io/commands/incr/](https://redis.io/commands/incr/)

{{< /columns >}}

#### SET
```
SET key value [NX | XX] [GET] [EX seconds | PX milliseconds |
  EXAT unix-time-seconds | PXAT unix-time-milliseconds | KEEPTTL]
```
Set the string value of a key. See also [https://redis.io/commands/set/](https://redis.io/commands/set/)
