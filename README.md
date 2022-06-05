---
cover: .gitbook/assets/1541421557544.jpeg
coverY: 0
---

# Vendors integration

### Become partner with money on chain earning up to 1% commission on all your sales.

Vendors are third parties who want to integrate their platform with the MoC ecosystem. Vendors can charge a markup of up to 1% of the value to mint/redeem operations, and receive this value as MoC tokens. These tokens neither receive rewards nor vote nor can they participate as an oracle or as no other function that MoC stakeholders have in the Staking Machine.

## Step by step guide.

### **1 Step One: Choose your Markup**

Choose what percentage of commission you want to receive (maximum 1%) and prepare an address to receive the earnings. Once you are ready, contact the team so that we can register you as a vendor.

Fill this form to send formally your request. The Money on chain team will give you a response in less than 48hs

{% embed url="https://forms.gle/m22GMh9nQVNNrZPk6" %}

### **2 Step Two: Approve the allowance**

Before start please make sure that someone of the team has activated your address as a vendor For starting operations with MoCVendor we need to allow to MoCVendors.sol and MoC.sol using MoC Token.

With this same address that you chose for receiving vendor’s comission, you must go to the contract moc.sol (link) and mocVendor.sol (link) and execute an allowance function. The approval transaction is used to grant permission for the smart contract to transfer a certain amount of the token, called allowance.

There is many ways to do this step.

A. Runing a script.js that interacts with The MocToken.sol  ABI

B. Interacting with the Remix Interface&#x20;

C. With one click Dapp UI.

&#x20;



**B.**  Remix interface.

B.1 Connect your metamask to your RSK testnet with remix. In this case we are going to use testnet but it applies the same for mainnet

![](<.gitbook/assets/Screenshot from 2022-05-17 09-29-06.png>)

B.2 Create a file .sol and Copy the following [code](https://github.com/money-on-chain/main-RBTC-contract/blob/master-gitbook/contracts/MoCVendors.sol) paste it in remix

![](<.gitbook/assets/Screenshot from 2022-05-17 13-00-00 (1).png>)

**B.3** Copy this \[address]

&#x20;(0x45a97b54021a3F99827641AFe1BFAE574431e6ab)

&#x20;from MocToken.sol (testnet) and paste it where it says: at adress near the blue button.

![](<.gitbook/assets/Screenshot from 2022-05-17 13-03-03.png>)

**B.4** Press the blue button. Once you are Ready you can now interact with moctoken.sol in depth.

![](<.gitbook/assets/Screenshot from 2022-05-17 00-41-37.png>)

**B.5** So the next thing here is to Allow moc.sol and mocVendors.sol to be able to interact with each other. And for this, we will approach the approve function.

![](<.gitbook/assets/Screenshot from 2022-05-17 00-42-26.png>)

**B**.6 We need to approve these two addresses for some amount of Moc for spending.

MoC.sol (RSK Testnet) : 0x2820f6d4D199B8D8838A4B26F9917754B86a0c1F

MoCVendors.sol (RSK Testnet) : 0x84b895A1b7be8fAc64d43757479281Bf0b5E3719



![](<.gitbook/assets/Screenshot from 2022-05-17 15-11-52.png>)

Please Rember to do this twice; one for the moc.sol and the other one for MocVendors.sol

Here i leave a video for more Information.

{% embed url="https://streamable.com/hhe5gc" %}

{% embed url="https://docs.moneyonchain.com/main-rbtc-contract/integration-with-moc-platform/vendors" %}

### **3 Step Three: Stake some MOC**

If you reached at this point Congratulations! The most difficult part is done.

Now you have to go again to the RSK Faucet and get some tRBTC If you cant because of the dairy limit try with other address and a different explorer Here is the link: https://faucet.rsk.co/

Notice that MocVendors program have a limit in earning commissions , and thath limit is up to You. Let me explain : Let suppose that you staked 500 mocs on commissions , the maximum profit that you can reach is 500 mocs also, So the limit is up what you Stake

#### **3.1 Go to SOVRYN (Testnet) and exchange some MOC (testnet)**

![](<.gitbook/assets/Screenshot from 2022-05-17 18-48-42.png>)

3.2 Go to remix&#x20;

![](<.gitbook/assets/Screenshot from 2022-05-17 09-29-06.png>)

**3.3** copy this code (Address) MocVendors.sol (testnet)

0x84b895A1b7be8fAc64d43757479281Bf0b5E3719

Here is the docs off the abi

{% embed url="https://docs.moneyonchain.com/main-rbtc-contract/smart-contracts/abis-documentation/mocvendors" %}

This is the solidity smart contract that we must interact with.

{% embed url="https://github.com/money-on-chain/main-RBTC-contract/blob/master-gitbook/contracts/MoCVendors.sol" %}

&#x20;**3.4** push at address&#x20;

![](<.gitbook/assets/Screenshot from 2022-05-17 13-03-03.png>)

**3.5** go to the addStake function and stake some Mocs

You can unstake it when ever you want!

![](<.gitbook/assets/Screenshot from 2022-05-25 15-49-29.png>)

You are ready!!

### **4 Step : Test its !!!**

**4.0** Open this repo locally&#x20;

{% embed url="https://github.com/money-on-chain/moc-integration-js" %}

**4.1** Create a .env file and fill your private information&#x20;

```
USER_ADDRESS=
USER_PK=
HOST_URI=https://public-node.testnet.rsk.co
MOC_ENVIRONMENT=mocTestnet
MOC_PROJECT=MoC
VENDOR_ADDRESS=0xf69287F5Ca3cC3C6d3981f2412109110cB8af076
GAS_MULTIPLIER=2
OPERATION_AMOUNT_MINT_DOC=10
OPERATION_AMOUNT_REDEEM_DOC=10
OPERATION_AMOUNT_MINT_BPRO=0.0001
OPERATION_AMOUNT_REDEEM_BPRO=0.0001
```

**4.2** Run test mint docs

```
npm run mint-doc
```

&#x20;**4.3** Go to the contract again in the third step and interact&#x20;

![](<.gitbook/assets/Screenshot from 2022-05-17 13-03-03.png>)

**4.4** Go to the function getTotalPaidInMoc and see how much you earned Thats it!

![](<.gitbook/assets/Screenshot from 2022-05-25 16-13-12 (1).png>)

**Thats it , now you can see how much Moc tokens you earned.**
