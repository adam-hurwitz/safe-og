---
title: 🔰 Perform Safe transactions
tags: Safe
description: Perform Safe transactions
image: https://pbs.twimg.com/profile_banners/8467082/1674046807/1500x500
---

Perform transactions
===

## About

#### On-chain

- The last cosigner confirms the transaction (txn) that executes on-chain.
- The on-chain txn pays the network fee and is recorded in the cosigner's address history.
- If the cosigner does not have enough funds for the txn fee the txn can fail with txn fees lost.

#### Limits and queue

- There are no time limits to sign txns.
- [Transaction queue](https://help.safe.global/en/articles/4987205-transaction-queue)
    - No other txn can be executed until the current txn is executed, canceled, or replaced.
    - First in first out (FIFO)

## Steps

1. Create the txn: Safe > Submit *New Transaction*
    a. If verifying a txn: Follow the [off and on-chain steps]() to check that the data matches.
    b. Sign the txn on the wallet.
    c. Partially signed txns show in *Transactions* > *Queue*
2. Complete the transaction with the required threshold of cosigners: Safe > *Transactions*
    a. *Confirm*
    b. *Cancel*
    - [Why do I need to pay for canceling a transaction?](https://help.safe.global/en/articles/4738501-why-do-i-need-to-pay-for-cancelling-a-transaction)

    c. [Speed up an approved and pending transaction.](https://hackmd.io/@safe/og/https%3A%2F%2Fhackmd.io%2F%40safe%2Fopportunities#Transaction-management-P2)
3. Check the wallet's [token approval amounts](https://docs.google.com/document/u/0/d/1uPMUppk7BZ5ZLmLx0ht0RPrneDTyiXKAfr2kV9YK_C4/edit).

## Features

#### Advanced options

- Go to Safe > *Transactions > Queue > Confirm> Advanced options > Edit*
- *Owner Transaction (Execution) > Nonce*: Use the same nonce on the signer's address as originally used if overwriting or canceling a pending transaction.
- *Gas limit*: Auto-generated, do not adjust.
- *Gas price (GWEI)*: Auto-generated, can use [Ethereum Gas Tracker](https://etherscan.io/gastracker#historicaldata) to verify.

#### Bundle multiple transactions

- *See [Transaction Builder](https://help.safe.global/en/articles/4680071-transaction-builder)*
- Approve multiple transactions with one set of signatures.
- Convert to [Uint256 format](https://docs.google.com/document/d/1pfGXa-DCOBQ6Ed7w1Q_XNaTtiUwuWRQSLgJ6vZ4v85I/edit#heading=h.ohamhurjxbk)

#### Spending approvals and limits

- *See [Set up and use Spending Limits](https://help.safe.global/en/articles/4667979-set-up-and-use-spending-limits)*
- Recurring or one-time
- Only beneficiaries who are also owners can actually withdraw funds.

## Troubleshoot

- If using a Ledger: [Enable smart contract data](https://hackmd.io/fNvoR6H4RjCygPVIn7-Fzw#2-Add-ETH-addresses-as-signers)
- Ensure the cosigner has enough funds to execute the on-chain txn.
- Txn not showing in Safe
    - Check Etherscan in a few minutes.
    - If showing in Etherscan and not in Safe
        - Restart Safe and cosigner wallet.
        - Check the Safe UI in a few minutes.

<p style="text-align: center; font-style: italic">This content is not financial, technical, or legal advice. Always consult a financial professional and do your own research.</p>

<style>
    .markdown-body h1 {
        font-weight: 700;
        font-size: 3.4rem;
    }
    .markdown-body {
        font-size: 1.8rem;
    }
    .markdown-body a:link {
        color: #3C8974
    }
    .markdown-body a:hover {
        color: #225347 
    }
    .markdown-body a:active {
        color: #225347
    }
</style>