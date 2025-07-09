---
description: Get the user's currently information
---

# \[GET] Get sub-user information

## Path

```
/merchant/user/info/:id
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

