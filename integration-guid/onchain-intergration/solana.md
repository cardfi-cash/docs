---
description: Onchain deposite & apply on solana
---

# Solana

## Token Support

Currently cardFi support follow tokens on solana chains

| Name | Mint                                         | Vault                                        | Vault Token Account                          |
| ---- | -------------------------------------------- | -------------------------------------------- | -------------------------------------------- |
| USDT | Es9vMFrzaCERmJfrF4H2FYD4KCoNkY11McCe8BenwNYB | EKpdNp4X8uw3267qZCCBs3WuBYPW3vBnbC1x5gnGSv2K | 34uXzajC7JSwNc1ogiPqQPQ9FCw3FJVNSoSneUwhY4xc |

## Deposit Rules

You can deposit asserts to any card on CardFi system with follow rules :

1. Create a new transaction
2. Add a USDT SPL-transfer transaction
3. Add a MEMO-transaction using `splMemo` . Input the `user_card_id` you wants to deposit with `base64` string .
4. Send out the transaction and wait for callback .

### Deposit Example \[Node.js]

```javascript
const web3 = require('@solana/web3.js');
const splToken = require('@solana/spl-token');
const splMemo = require('@solana/spl-memo');
const b58 = require("b58")
const secretKey = b58.decode("");
const payer = web3.Keypair.fromSecretKey(secretKey);
const connection = new web3.Connection(web3.clusterApiUrl('mainnet-beta'), 'confirmed');
const recipientAddress = new web3.PublicKey('EKpdNp4X8uw3267qZCCBs3WuBYPW3vBnbC1x5gnGSv2K');
const USDT_MINT = new web3.PublicKey('Es9vMFrzaCERmJfrF4H2FYD4KCoNkY11McCe8BenwNYB');

async function main() {
  const fromTokenAccount = await splToken.getAssociatedTokenAddress(
    USDT_MINT,
    payer.publicKey
  );
  const toTokenAccount = await splToken.getAssociatedTokenAddress(
    USDT_MINT,
    recipientAddress
  );
  const transferIx = splToken.createTransferInstruction(
    fromTokenAccount,
    toTokenAccount,
    payer.publicKey,
    0.3 * 10 ** 6 
  );

  const memoIx = splMemo.createMemoInstruction(Buffer.from("15_1_0").toString("base64"), [payer.publicKey]); //user_card_id Here .
  const tx = new web3.Transaction().add(transferIx, memoIx);
  const sig = await web3.sendAndConfirmTransaction(connection, tx, [payer]);

  console.log('✅ Transaction sent:', sig);
}

main().catch(console.error);

```

## Apply Rules

Same as deposit . mast > $3&#x20;
