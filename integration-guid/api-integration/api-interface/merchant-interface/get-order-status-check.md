---
description: Check the deposite or apply status
---

# \[GET] Order status check

## Path

```
/merchant/order/check/id/oid
```

## Method

```
GET
```

## Params

```
id : The merchant set
oid : Order Id from apply or deposite interface
```

## Query

```
null
```

## Success Response

```
{
    "code": 200,
    "data": []
}
```

## Failed Response

```
{
    "code": 200,
    "data": false
}
```

