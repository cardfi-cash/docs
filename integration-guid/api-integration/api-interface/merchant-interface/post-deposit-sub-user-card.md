---
description: Restful API deposit interface
---

# \[POST] Deposit sub-user card

## Path

```
/merchant/user/card/deposite/:id
```

## Method

```
POST
```

## Params

```
id //Your internal ID for user
```

## Query

```
null
```

## Body

```
{
    "cardId":0, // Card Type . currently support 0 only
    "amount":0.1, //Amount in token . eg : 0.1 {SOL}
    "token":"ETHARBITRUM" // Payment method . currently support : TON | SOL | ETHARBITRUM | XMR | TRX | USDTTRX
}
```

## Success Response

```
{
    "code": 200,
    "data": {
        "to": "0xcbc830685cbe5dd72aa7d277b9976f0615f6c83f", //Reciver address
        "amount": "0.00500000", //Amount to send
        "orderId": 1751714477698 //Order ID
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

```
{
    "code": 500,
    "error": "Filed reason."
}
```
