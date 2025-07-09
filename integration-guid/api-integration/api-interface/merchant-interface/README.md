---
description: API interface for merchant using cardFi service
icon: shop
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
| USDCBSC      | 10    |
| USDTBSC      | 10    |
| BSC          | 0.01  |

### Card Apply Fee

| Chain       | Fee   |
| ----------- | ----- |
| APTOS       | 3.99  |
| TON         | 3     |
| SOL         | 0.05  |
| ETHARBITRUM | 0.005 |
| XMR         | 0.02  |
| TRX         | 50    |
| USDCBSC     | 10    |
| USDTBSC     | 10    |
| BSC         | 0.01  |

### API Index

1. You should apply for your merchant API-KEY on [CardFi\_Bot](http://t.me/cardfi_bot)
2. Try Ping with auth

{% content-ref url="get-ping.md" %}
[get-ping.md](get-ping.md)
{% endcontent-ref %}

3. New an user profile and infromation&#x20;

{% content-ref url="post-add-or-update-new-sub-user-information.md" %}
[post-add-or-update-new-sub-user-information.md](post-add-or-update-new-sub-user-information.md)
{% endcontent-ref %}

4. Apply a new card for user .

{% content-ref url="post-apply-new-sub-user-card.md" %}
[post-apply-new-sub-user-card.md](post-apply-new-sub-user-card.md)
{% endcontent-ref %}

5. Pay the new card invoice .&#x20;
6. Wait for 60s , try fetch the card infromation .&#x20;

{% content-ref url="get-get-sub-user-information.md" %}
[get-get-sub-user-information.md](get-get-sub-user-information.md)
{% endcontent-ref %}

7. If the card exsit already . Now you can deposite assert into it !

{% content-ref url="post-deposit-sub-user-card.md" %}
[post-deposit-sub-user-card.md](post-deposit-sub-user-card.md)
{% endcontent-ref %}

8. Here we go !  Now run !&#x20;
