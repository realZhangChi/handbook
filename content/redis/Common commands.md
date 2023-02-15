---
title: "Common commands"
date: 2023-02-15T09:20:58+08:00
draft: false
---

## Redis common commands

### Database

{{< columns >}} 
#### DBSIZE

``` bash
DBSIZE
```

Return the number of keys in the currently-selected database. see also [redis.io](https://redis.io/commands/dbsize/).

<--->

#### FLUSHALL

``` bash

FLUSHALL [ASYNC | SYNC]

```
Remove all keys from all database. see also [redis.io](https://redis.io/commands/flushall/).

<--->

#### FLUSHDB

``` bash
FLUSHDB [ASYNC | SYNC]
```

Remove all keys from the current database. see also [redis.io](https://redis.io/commands/flushdb/).

{{< /columns >}}

{{< columns >}}

#### SELECT

``` bash
SELECT index
```

Change the selected database for the current connection. see also [redis.io](https://redis.io/commands/select/).

<--->

<--->

{{< /columns >}}

### Key

{{< columns >}}

#### KEYS

``` bash
KEYS pattern
```

Returns all keys matching pattern. See also [redis.io](https://redis.io/commands/keys/).

<--->

#### EXISTS

``` bash
EXISTS key [key ...]
```

Determine if a key exists. See also [redis.io](https://redis.io/commands/exists/).

<--->

#### EXPIRE

``` bash
EXPIRE key seconds [NX | XX | GT | LT]
```

Set a key's time to live in seconds. See also [redis.io](https://redis.io/commands/expire/).

{{< /columns >}}

{{< columns >}}

#### TTL

``` bash
TTL key
```

Get the time to live for a key in seconds. See also [redis.io](https://redis.io/commands/ttl/).

<--->

#### TYPE

``` bash
TYPE key
```

Determine the type stored at key. See also [redis.io](https://redis.io/commands/type/).

<--->

#### STRLEN

``` bash
STRLEN key
```

Get the length of the value stored in a key. See also [redis.io](https://redis.io/commands/strlen/).

{{< /columns >}}

### Value

{{< columns >}}

#### GET

``` bash
GET key
```

Get the value of a key. See also [redis.io](https://redis.io/commands/get/).

<--->

#### GETRANGE

``` bash
GETRANGE key start end
```

Get a substring of the string stored at a key. See also [redis.io](https://redis.io/commands/getrange/).

<--->

#### APPEND

``` bash
APPEND key value
```

Append a value to a key. See also [redis.io](https://redis.io/commands/append/).

{{< /columns >}}

{{< columns >}}

#### SET

``` bash
SET key value [NX | XX] [GET] [EX seconds | PX milliseconds |
  EXAT unix-time-seconds | PXAT unix-time-milliseconds | KEEPTTL]
```

Set the string value of a key. See also [redis.io](https://redis.io/commands/set/).

<--->

#### SETRANGE

``` bash
SETRANGE key offset value
```

Overwrite part of a string at key starting at the specified offset. See also [redis.io](https://redis.io/commands/setrange/).

<--->

#### MGET

``` bash
MGET key [key ...]
```

Get the values of all given keys. See also [redis.io](https://redis.io/commands/mget/).

{{< /columns >}}

{{< columns >}}

#### MSET

``` bash
MSET key value [key value ...]
```

Set multiple keys to multiple values. See also [redis.io](https://redis.io/commands/mset/).

<--->

#### MSETNX

``` bash
MSETNX key value [key value ...]
```

Set multiple keys to multiple values, only if none of the key exist. See also [redis.io](https://redis.io/commands/msetnx/).

<--->

#### INCR

``` bash
INCR key
```

Increment the integer value of a key by one. See also [redis.io](https://redis.io/commands/incr/).

{{< /columns >}}

{{< columns >}}

#### DECR

``` bash
DECR key
```

Decrement the integer value of a key by one. See also [redis.io](https://redis.io/commands/decr/).

<--->

#### INCRBY

``` bash
INCRBY key increment
```

Increment the integer value of a key by the given number. See also [redis.io](https://redis.io/commands/incrby/).

<--->

#### DECRBY

``` bash
DECRBY key decrement
```

Decrement the integer value of a key by the given number. See also [redis.io](https://redis.io/commands/decrby/).

{{< /columns >}}

### List

{{< columns >}}

#### LPUSH

``` bash
LPUSH key element [element ...]
```

Prepend one or multiple elements to a list. See also [redis.io](https://redis.io/commands/lpush/).

<--->

#### RPUSH

``` bash
RPUSH key element [element ...]
```

Apend one or multiple elements to a list. See also [redis.io](https://redis.io/commands/rpush/).

<--->

#### LRANGE

``` bash
LRANGE key start stop
```

Get a range of elements from a list. See also [redis.io](https://redis.io/commands/lrange/).

{{< /columns >}}

{{< columns >}}

#### LINDEX

``` bash
LINDEX key index
```

Get an element from a list by its index. See also [redis.io](https://redis.io/commands/lindex/).

<--->

#### LPOP

``` bash
LPOP key [count]
```

Remove and get the first elements in a list. See also [redis.io](https://redis.io/commands/lpop/).

<--->

#### RPOP

``` bash
RPOP key [count]
```

Remove and get the last elements in a list. See also [redis.io](https://redis.io/commands/rpop/) .

{{< /columns >}}

{{< columns >}}

#### LLEN

``` bash
LLEN key
```

Get the length of a list. See also [redis.io](https://redis.io/commands/llen/).

<--->

#### LREM

``` bash
LREM key count element
```

Remove elements of a list. See also [redis.io](https://redis.io/commands/lrem/).

<--->

#### LTRIM

``` bash
LTRIM key start stop
```

Trim the list **to** the specified range. See also [redis.io](https://redis.io/commands/ltrim/).

{{< /columns >}}

{{< columns >}}

#### LSET

``` bash
LSET key index element
```

Set the value of an element in a list by its index. See also [redis.io](https://redis.io/commands/lset/).

<--->

#### LINSERT

``` bash
LINSERT key <BEFORE | AFTER> pivot element
```

Insert an element before or after another element in list. See also [redis.io](https://redis.io/commands/linsert/).

<--->

{{< /columns >}}

### Set

{{< columns >}}

#### SADD

``` bash
SADD key member [member ...]
```

Add one or more members to a set. See also [redis.io](https://redis.io/commands/sadd/).

<--->

#### SMEMBERS

``` bash
SMEMBERS key
```

Get all the members in a set. See also [redis.io](https://redis.io/commands/smembers/).

<--->

#### SISMEMBER

``` bash
SISMEMBER key member
```

Determine if a given value is a member of a set. See also [redis.io](https://redis.io/commands/sismember/).

{{< /columns >}}

{{< columns >}}

#### SCARD

``` bash
SCARD key
```

Get the number of members in a set. See also [redis.io](https://redis.io/commands/scard/).

<--->

#### SREM

``` bash
SREM key member [member ...]
```

Remove one or more members from a set. See also [redis.io](https://redis.io/commands/srem/).

<--->

#### SRANDMEMBER

``` bash
SRANDMEMBER key [count]
```

Get one or multiple random members from a set. See also [redis.io](https://redis.io/commands/srandmember/).

{{< /columns >}}

{{< columns >}}

#### SPOP

``` bash
SPOP key [count]
```

Remove and return one or multiple random members from a set. See also [redis.io](https://redis.io/commands/spop/).

<--->

#### SMOVE

``` bash
SMOVE source destination member
```

Move a member from one set to another. See also [redis.io](https://redis.io/commands/smove/).

<--->

#### SDIFF

``` bash
SDIFF key [key ...]
```

Subtract multiple sets. See also [redis.io](https://redis.io/commands/sdiff/).

{{< /columns >}}

{{< columns >}}

#### SINTER

``` bash
SINTER key [key ...]
```

Intersect multiple sets. See also [redis.io](https://redis.io/commands/sinter/).

<--->

#### SUNION

``` bash
SUNION key [key ...]
```

Add multiple sets. See also [redis.io](https://redis.io/commands/sunion/).
<--->

{{< /columns >}}

### Hash

{{< columns >}}

#### HGET

``` bash
HGET key field
```

Get the value of a hash field. See also [redis.io](https://redis.io/commands/hget/).

<--->

#### HSET

``` bash
HSET key field value [field value ...]
```

Set the string value of a hash field. See also [redis.io](https://redis.io/commands/hset/).

<--->

#### HMGET

```bash
HMGET key field [field ...]
```

Get the values of all given hash fields. See also [redis.io](https://redis.io/commands/hmget/).

{{< /columns >}}

{{< columns >}}

#### HGETALL

``` bash
HGETALL key
```

Get all the fields and values in a hash. See also [redis.io](https://redis.io/commands/hgetall/).

<--->

#### HDEL

``` bash
HDEL key field [field ...]
```

Delete one or more hash fields. See also [redis.io]().
<--->

#### HLEN

``` bash
HLEN key
```

Get the number of fields in a hash. See also [redis.io](https://redis.io/commands/hlen/).

{{< /columns >}}

{{< columns >}}

#### HEXISTS

``` bash
HEXISTS key field
```

Determine if a hash field exists. See also [redis.io](https://redis.io/commands/hexists/).

<--->

#### HKEYS

``` bash
HEXISTS key field
```

Get all the fields in a hash. See also [redis.io](https://redis.io/commands/hkeys/).

<--->

#### HVALS

``` bash
HVALS key
```

Get all the values in a hash. See also [redis.io](https://redis.io/commands/hvals/).

{{< /columns >}}

{{< columns >}}

#### HINCRBY

``` bash
HINCRBY key field increment
```

Increment the integer value of a hash field by the given number. [redis.io](https://redis.io/commands/hincrby/).

<--->

#### HSETNX

``` bash
HSETNX key field value
```

Set the value of a hash field, only if the field does not exist. See also [redis.io](https://redis.io/commands/hsetnx/).

<--->

{{< /columns >}}
