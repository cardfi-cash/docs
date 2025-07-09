---
description: Add or update sub-user information
---

# \[POST] Add or update new sub-user information

## Path

```
/merchant/user/reg
```

## Method

```
POST
```

## Params

```
null
```

## Query

```
null
```

## Body

```
{
        mid, // Merchain define your own internal mid
        first_name, // first name
        last_name, // last name
        birth, // 1999-01-01 : YY:MM:DD
        email, // xxx@xxx.xx
        mobile: {
            nation_code, // eg: 852
            mobile , // 1920182121 your phone number
        },
        region, // ISO-3166 Region Code
        address , // Details address : privance | city | details
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
