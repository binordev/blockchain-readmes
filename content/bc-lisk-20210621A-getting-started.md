## Getting started with Lisk

I am testing out Lisk on WSL2 on Windows. The chain nodes does not currently run on Windows, which is why I use WSL2.  

First I got [the quick start running](https://github.com/binordev/lsk-qstart1). It only runs a chain node.  
The link shows you to use `lisk init`.  

Next I ran [Lisk Tutorial hello-world](bc-lisk-20210621B-tutorial-hello-world.md). It runs a node and a React frontend. It tells you how to run the frontend from WSL2 and open it in a browser from Windows.  

Next I wan't to connect the [hello-world node](https://github.com/LiskHQ/lisk-sdk-examples/tree/development/tutorials/hello-world/blockchain_app) with the [Lisk Wallet](https://lisk.com/wallet).  
This is [not possible directly](https://discord.com/channels/405002561775599619/606112254789681163/856487834483294229) without [Lisk Service](https://discord.com/channels/405002561775599619/606112254789681163/856488548731846677).  
Here is [howto setup a Lisk Service](https://lisk.com/documentation/lisk-service/) in front of your node.

The link also gives you the links to the urls to the existing nets services:

* [Mainnet](https://service.lisk.io/api/)
* [Testnet](https://testnet-service.lisk.io/api/)
* [Betanet](https://betanet-service.lisk.io/api/)

and their [swagger pages](https://lisk.com/documentation/lisk-service/references/api.html), that enables you to test.

Done