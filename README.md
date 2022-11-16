# Solana Token Creator

## Creating a Solana Token

[Demo](https://token-creator-lac.vercel.app/)

You can use the token creator application to create a token and
sent it to your wallet. This application is purely for demonstration
purposes.

## Full Breakdown

Creating a Solana token requires the following steps:

1. Creating a new Mint account
2. Creating an associated token account
3. Minting an amount of the token to the associated token account
4. Adding the token metadata to the mint account

### Creating a new mint account

Mint accounts hold information about the token such as how 
many decimals the token has and who can mint new tokens.

You can create a custom keypair for the mint account by
[grinding a keypair](https://solanacookbook.com/references/keypairs-and-wallets.html#how-to-generate-a-vanity-address). 
This keypair's public key will be used to have a vanity address 
for the token. Create a new mint account with that key
by first initializing the account and space for the mint 
account, then calling `createInitializeMintInstruction`. 
These instructions can be added and executed in the same 
transaction.
