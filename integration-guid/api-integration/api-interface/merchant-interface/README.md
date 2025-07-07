---
description: API interface for merchant using cardFi service
---

# Merchant Interface

## Base Path

```
/merchant
```

#### Eg :&#x20;

Ping : `https://api.cardfi.cash/merchant/ping`

### Auth Rules

Add header to all your request about `merchain` role

| Header | Value   |
| ------ | ------- |
| token  | API-KEY |

You can apply your API-KEY on CardFi Bot : [http://t.me/cardfi\_bot](http://t.me/cardfi_bot)

### Minimum Card Deposit Fee

| Chain        | Fee   |
| ------------ | ----- |
| APTOS        | 3.99  |
| TON          | 3     |
| SOL          | 0.05  |
| ETHARBITRUM  | 0.005 |
| XMR          | 0.02  |
| TRX          | 50    |
| USDTSOL      | 10    |
| USDCSOL      | 10    |
| USDTARBITRUM | 10    |
| USDCARBITRUM | 10    |

### Card Apply Fee

| Chain       | Fee   |
| ----------- | ----- |
| APTOS       | 3.99  |
| TON         | 3     |
| SOL         | 0.05  |
| ETHARBITRUM | 0.005 |
| XMR         | 0.02  |
| TRX         | 50    |

### API Index

