---
description: To get the balance history for sub user card
---

# \[GET] Ger sub-user card balance hisotry

## Path

```
/merchant/user/card/:id/:cardId/history
```

## Method

```
GET
```

## Params

```
id : The merchant set's user id
cardId : card type id , default 0 
```

## Query

```
page:1  // Page number for seach
limit:10 // page size
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

