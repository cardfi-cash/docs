---
description: EVM contract call and contract interface
---

# Arbitrum | Polygon | BSC

## Contract address

| Chain | Contract Address                           |
| ----- | ------------------------------------------ |
| Arb   | 0x65571cb75214915A2cD43d9F883C96eDc4D5AB1a |
| Pol   |                                            |
| BSC   |                                            |

## Deposit Interface

```javascript
sendTx({
        address: "0x65571cb75214915A2cD43d9F883C96eDc4D5AB1a",
        abi: abi,
        functionName: 'deposit',
        args: [
            token, 
            amount,
            bytesToHex(Buffer.from(id)) // Deposit To Id. Card's owner ID
        ],
    })
```
