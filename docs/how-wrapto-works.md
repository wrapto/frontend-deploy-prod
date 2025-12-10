# How Wrapto Works

## Introduction

Wrapto is a cross-chain bridge system that enables the native coin **PAC** to
be used on other chains through a wrapped token called **WPAC**.
The system supports two primary operations:

1. **Wrapping (PAC → WPAC)**
2. **Unwrapping (WPAC → PAC)**

WPAC is always backed 1:1 by the native coins held in custody.

## Wrapping PAC

Wrapping converts the native coin PAC into a WPAC token on a compatible chain.
Users must send PAC coins to the Deposit Wallet with the following memo:

**<destination-address>**@**<chain-id>**

**destination-address**  is the address on the target chain that will receive WPAC, and **chain-id** is identifies the target blockchain. such as `BSC`, `POLYGON`, or `BASE`.

This instructs Wrapto to mint WPAC on the target chain and send the tokens to that address.

## Unwrapping WPAC

Unwrapping converts WPAC tokens back to native PAC coins.

This is performed on-chain using the WPAC contract’s `bridge()` function.
The user calls the bridge function by providing their Pactus address and the amount they want to bridge:

```solidity
bridge("<pactus-address>", amount)
```

The function burns the user’s WPAC and emits a Bridge event.
Wrapto then detects the event and releases the corresponding amount of PAC to the user’s address.

## Security Model

Deposit and withdrawal wallets are separate to:

* Reduce risk exposure
* Simplify accounting

### Controlled Minting

Only the specific **MINTER** address can mint WPAC.
This process is secure and transparent through the smart contract logic.

## WPAC Contract

The WPAC token contract is fully open-source and can be reviewed here:
[wpac-erc20](https://github.com/wrapto/wpac-erc-20)
