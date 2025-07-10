---
description: To get the transactions history for sub user card
---

# \[GET] Ger sub-user card transaction hisotry

## Path

```
/merchant/user/card/:id/:cardId/transactions
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
            "history": [
                {
                    "log_id": "",
                    "transaction_id": "",
                    "bill_date": "2025-07-09",
                    "transaction_time": "2025-07-09T10:23:16.148Z",
                    "mask_card_number": "******",
                    "card_id": "",
                    "amount": {
                        "amount": 9.44,
                        "currency": "USD"
                    },
                    "txn_type": "CARD_BALANCE_ADJUST",
                    "balance_after_transaction": {
                        "amount": 9.34,
                        "currency": "USD"
                    }
                },
                {
                    "log_id": "",
                    "transaction_id": "",
                    "bill_date": "2025-07-01",
                    "transaction_time": "2025-06-30T16:20:58.487Z",
                    "mask_card_number": "******",
                    "card_id": "",
                    "amount": {
                        "amount": -0.1,
                        "currency": "USD"
                    },
                    "txn_type": "CARD_SERVICE_FEE",
                    "balance_after_transaction": {
                        "amount": -0.1,
                        "currency": "USD"
                    }
                },
                {
                    "log_id": "",
                    "transaction_id": "",
                    "bill_date": "2025-06-08",
                    "transaction_time": "2025-06-07T18:49:56.596Z",
                    "mask_card_number": "536025******1814",
                    "card_id": "",
                    "amount": {
                        "amount": -46.07,
                        "currency": "USD"
                    },
                    "txn_type": "CARD_BALANCE_ADJUST",
                    "balance_after_transaction": {
                        "amount": 0,
                        "currency": "USD"
                    }
                },
                {
                    "log_id": "",
                    "transaction_id": "",
                    "bill_date": "2025-06-08",
                    "transaction_time": "2025-06-07T17:43:49.176Z",
                    "mask_card_number": "536025******1814",
                    "card_id": "",
                    "amount": {
                        "amount": 18,
                        "currency": "USD"
                    },
                    "txn_type": "CARD_BALANCE_ADJUST",
                    "balance_after_transaction": {
                        "amount": 46.07,
                        "currency": "USD"
                    }
                },
                {
                    "log_id": "",
                    "transaction_id": "",
                    "bill_date": "2025-06-08",
                    "transaction_time": "2025-06-07T17:07:17.657Z",
                    "mask_card_number": "536025******1814",
                    "card_id": "",
                    "amount": {
                        "amount": 18.07,
                        "currency": "USD"
                    },
                    "txn_type": "CARD_BALANCE_ADJUST",
                    "balance_after_transaction": {
                        "amount": 28.07,
                        "currency": "USD"
                    }
                },
                {
                    "log_id": "",
                    "transaction_id": "",
                    "bill_date": "2025-06-06",
                    "transaction_time": "2025-06-06T10:11:01.887Z",
                    "mask_card_number": "536025******1814",
                    "card_id": "",
                    "amount": {
                        "amount": 10,
                        "currency": "USD"
                    },
                    "txn_type": "CARD_BALANCE_ADJUST",
                    "balance_after_transaction": {
                        "amount": 10,
                        "currency": "USD"
                    }
                }
            ],
            "page": 1,
            "limit": 10,
            "total_count": 6,
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

