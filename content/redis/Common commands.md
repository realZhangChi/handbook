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
Return the number of keys in the currently-selected database. see also [redis.io](https://redis.io/commands/dbsize/).

<---> 

#### FLUSHALL
```
FLUSHALL [ASYNC | SYNC]
```
Remove all keys from all database. see also [redis.io](https://redis.io/commands/flushall/).

<---> 

#### FLUSHDB
```
FLUSHDB [ASYNC | SYNC]
```
Remove all keys from the current database. see also [redis.io](https://redis.io/commands/flushdb/).

{{< /columns >}}

{{< columns >}}

#### SELECT
```
SELECT index
```
Change the selected database for the current connection. see also [redis.io](https://redis.io/commands/select/).

<--->

<--->

{{< /columns >}}

### Key

{{< columns >}}

#### KEYS
```
KEYS pattern
```
Returns all keys matching pattern. See also [redis.io](https://redis.io/commands/keys/).

<---> 

#### EXISTS
```
EXISTS key [key ...]
```
Determine if a key exists. See also [redis.io](https://redis.io/commands/exists/).

<--->

#### EXPIRE
```
EXPIRE key seconds [NX | XX | GT | LT]
```
Set a key's time to live in seconds. See also [redis.io](https://redis.io/commands/expire/).

{{< /columns >}}

{{< columns >}}

#### TTL
```
TTL key
```
Get the time to live for a key in seconds. See also [redis.io](https://redis.io/commands/ttl/).

<--->

#### TYPE
```
TYPE key
```
Determine the type stored at key. See also [redis.io](https://redis.io/commands/type/).

<--->

#### STRLEN
```
STRLEN key
```
Get the length of the value stored in a key. See also [redis.io](https://redis.io/commands/strlen/).

{{< /columns >}}

### Value

{{< columns >}}

#### GET
```
GET key
```
Get the value of a key. See also [redis.io](https://redis.io/commands/get/).

<--->

#### GETRANGE
```
GETRANGE key start end
```
Get a substring of the string stored at a key. See also [redis.io](https://redis.io/commands/getrange/).

<--->

#### APPEND
```
APPEND key value
```
Append a value to a key. See also [redis.io](https://redis.io/commands/append/).

{{< /columns >}}

{{< columns >}}

#### SET
```
SET key value [NX | XX] [GET] [EX seconds | PX milliseconds |
  EXAT unix-time-seconds | PXAT unix-time-milliseconds | KEEPTTL]
```
Set the string value of a key. See also [redis.io](https://redis.io/commands/set/).

<--->

#### SETRANGE
```
SETRANGE key offset value
```
Overwrite part of a string at key starting at the specified offset. See also [redis.io](https://redis.io/commands/setrange/).

<--->

#### MGET

```
MGET key [key ...]
```
Get the values of all given keys. See also [redis.io](https://redis.io/commands/mget/).

{{< /columns >}}

{{< columns >}}

#### MSET

```
MSET key value [key value ...]
```

Set multiple keys to multiple values. See also [redis.io](https://redis.io/commands/mset/).

<--->

#### MSETNX

```
MSETNX key value [key value ...]
```

Set multiple keys to multiple values, only if none of the key exist. See also [redis.io](https://redis.io/commands/msetnx/).

<--->

#### INCR
```
INCR key
```
Increment the integer value of a key by one. See also [redis.io](https://redis.io/commands/incr/).

{{< /columns >}}

{{< columns >}}

#### DECR
```
DECR key
```
Decrement the integer value of a key by one. See also [redis.io](https://redis.io/commands/decr/).

<--->

#### INCRBY
```
INCRBY key increment
```
Increment the integer value of a key by the given number. See also [redis.io](https://redis.io/commands/incrby/).

<--->

#### DECRBY
```
DECRBY key decrement
```
Decrement the integer value of a key by the given number. See also [redis.io](https://redis.io/commands/decrby/).

{{< /columns >}}

### List

{{< columns >}}

#### LPUSH

```
LPUSH key element [element ...]
```

Prepend one or multiple elements to a list. See also [redis.io](https://redis.io/commands/lpush/).

<--->

#### RPUSH

```
RPUSH key element [element ...]
```

Apend one or multiple elements to a list. See also [redis.io](https://redis.io/commands/rpush/).

<--->

#### LRANGE

```
LRANGE key start stop
```

Get a range of elements from a list. See also [redis.io](https://redis.io/commands/lrange/).

{{< /columns >}}

{{< columns >}}

#### LINDEX

```
LINDEX key index
```

Get an element from a list by its index. See also [redis.io](https://redis.io/commands/lindex/).

<--->

#### LPOP

```
LPOP key [count]
```

Remove and get the first elements in a list. See also [redis.io](https://redis.io/commands/lpop/).

<--->

#### RPOP

```
RPOP key [count]
```

Remove and get the last elements in a list. See also [redis.io](https://redis.io/commands/rpop/) .

{{< /columns >}}

{{< columns >}}

#### LLEN

```
LLEN key
```

Get the length of a list. See also [redis.io](https://redis.io/commands/llen/).

<--->

#### LREM

```
LREM key count element
```

Remove elements of a list. See also [redis.io](https://redis.io/commands/lrem/).

<--->

#### LTRIM

```
LTRIM key start stop
```

Trim the list **to** the specified range. See also [redis.io](https://redis.io/commands/ltrim/).

{{< /columns >}}

{{< columns >}}

#### LSET

```
LSET key index element
```

Set the value of an element in a list by its index. See also [redis.io](https://redis.io/commands/lset/).

<--->

#### LINSERT

```
LINSERT key <BEFORE | AFTER> pivot element
```

Insert an element before or after another element in list. See also [redis.io](https://redis.io/commands/linsert/).

<--->

{{< /columns >}}

### Set 

{{< columns >}}

#### SADD

```
SADD key member [member ...]
```

Add one or more members to a set. See also [redis.io](https://redis.io/commands/sadd/).

<--->

#### SMEMBERS

```
SMEMBERS key
```

Get all the members in a set. See also [redis.io](https://redis.io/commands/smembers/).

<--->

#### SISMEMBER

```
SISMEMBER key member
```

Determine if a given value is a member of a set. See also [redis.io](https://redis.io/commands/sismember/).

{{< /columns >}}

{{< columns >}}

#### SCARD

```
SCARD key
```

Get the number of members in a set. See also [redis.io](https://redis.io/commands/scard/).

<--->

#### SREM

```
SREM key member [member ...]
```

Remove one or more members from a set. See also [redis.io](https://redis.io/commands/srem/).

<--->

#### SRANDMEMBER

```
SRANDMEMBER key [count]
```

Get one or multiple random members from a set. See also [redis.io](https://redis.io/commands/srandmember/).

{{< /columns >}}

{{< columns >}}

#### SPOP

```
SPOP key [count]
```

Remove and return one or multiple random members from a set. See also [redis.io](https://redis.io/commands/spop/).

<--->

#### SMOVE

```
SMOVE source destination member
```

Move a member from one set to another. See also [redis.io](https://redis.io/commands/smove/).

<--->

#### SDIFF

```
SDIFF key [key ...]
```

Subtract multiple sets. See also [redis.io](https://redis.io/commands/sdiff/).

{{< /columns >}}

{{< columns >}}

#### SINTER

```
SINTER key [key ...]
```

Intersect multiple sets. See also [redis.io](https://redis.io/commands/sinter/).

<--->

#### SUNION

```
SUNION key [key ...]
```

Add multiple sets. See also [redis.io](https://redis.io/commands/sunion/).
<--->

{{< /columns >}}