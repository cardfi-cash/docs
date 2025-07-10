---
description: Get sub-user's card information
---

# \[GET] Get card information

## Path

```
/merchant/user/card/:id
```

## Method

```
GET
```

## Params

```
id : The merchant set
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
    "code": 401,
    "error": "Permission deny . Please check if API-KEY correct ."
}
```

