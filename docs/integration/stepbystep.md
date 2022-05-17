# Step by step guide.

If you have reached this point, please make sure you have read what [Vendors](integration/vendors.md) are and how they work in money on chain. In this section we are going to make a guide to follow step by step and at the same time we are going to leave an address enabled as vendor with a private key so that you can test it in RSK testnet from your console. simple and easy . Please pay attention to the following steps.


## 1 Step One:

Choose what percentage of commission you want to receive (maximum 1%) and prepare an address to receive the earnings.
Once you are ready, contact the team so that we can register you as a vendor.

Contact the [Money on Chain team](https://moneyonchain.com/)
* Send DM via [Twitter](https://twitter.com/moneyonchainok)
* Send DM via [Telegram](https://t.me/MoneyOnChainCommunity)


## 2 Step Two:

Before start operations with MoCVendor we need to allow to MoCVendors.sol and MoC.sol using MoC Token. 
With this same address that you chose, you must go to the contract moc.sol (link) and mocVendor.sol (link) and execute an allowance from the explorer .
The approval transaction is used to grant permission for the smart contract to transfer a certain amount of the token, called allowance. 
Here I leave you a simple video how to do it.

#### Moc Vendors

Contract that manage vendors functions.

[MoCVendors contract ABI interface](../abis/MoCVendors.md). 

| Environment | Contract | Contract address |
| --- | --- | --- |
| Testnet | MoCVendors | 0x84b895A1b7be8fAc64d43757479281Bf0b5E3719 |
| Mainnet | MoCVendors | 0x2d442aA5D391475b6Af3ad361eA3b9818fb35BcA |
 

**Moc Token**

| Environment | Contract | Contract address |
| --- | --- | --- |
| Testnet | MoCToken | 0x45A97b54021A3F99827641AFE1bFae574431E6ab |
| Mainnet | MoCToken | 0x9aC7Fe28967b30e3a4E6E03286D715B42B453d10 |



