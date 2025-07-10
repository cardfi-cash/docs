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
    "data": {
        "result": {
            "result": "S",
            "code": "SUCCESS",
            "message": "Success"
        },
        "data": {
            "query": {
                "page": 1,
                "limit": 10,
                "card_id": ""
            },
            "transactions": [
                {
                    "transaction_id": "",
                    "card_id": "",
                    "mask_card_number": "******",
                    "transaction_time": "2025-06-30T16:20:58.467Z",
                    "confirm_time": "2025-06-30T16:20:58.467Z",
                    "transaction_amount": {
                        "amount": -0.1,
                        "currency": "USD"
                    },
                    "accounting_amount": {
                        "amount": 0,
                        "currency": "USD"
                    },
                    "surcharge": {
                        "amount": 0.1,
                        "currency": "USD"
                    },
                    "biz_type": "SERVICE_FEE",
                    "status": "SUCCEED"
                }
            ],
            "page": 1,
            "limit": 10,
            "total_count": 1,
            "total_page": 1
        }
    }
}
```

## Failed Response

```
{
    "code": 401,
    "error": "Permission deny . Please check if API-KEY correct ."
}
```

