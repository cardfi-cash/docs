---
description: To transfer the card balance to other cards .Support base on same merchant
---

# \[POST] Card transfer to card

## Path

```
/merchain/user/card/transfer/:from/:to
```

## Method

```
POST
```

## Params

```
from : From user's merchant internal user ID
to : To user's merchant internal user ID
```

## Query

```
null
```

## Body

```
{
    "amount":5, // Amount to transfer . Mini 5 $
}
```

## Success Response

```
{
    "code": 200,
    "data": "success"
}
```

## Failed Response

```
{
    "code": 401,
    "error": "Permission deny . Please check if API-KEY correct ."
}
```

```
{
    "code": 500,
    "error": "Filed reason."
}
```
