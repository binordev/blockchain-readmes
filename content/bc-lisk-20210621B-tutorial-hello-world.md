## Running Lisk hello-world tutorial in WSL2 on Windows

Lisk does not run on Windows, yet, so you can run it in WSL.  
I am running on Ubuntu 20.04.  

The [hello-world tutorial](https://github.com/LiskHQ/lisk-sdk-examples/tree/development/tutorials/hello-world) consist of a chain node and a react frontend.  
The link above tells you howto start them.  
With both running remote in WSL2 you [can't open the browser inside WSL - instead you manual open the browser from Windows](https://dev.lisk.com/t/running-lisk-projects-on-wsl2-on-windows/512).

## The code

The code covers [basic transactions in Lisk](https://lisk.com/documentation/lisk-sdk/guides/app-development/frontend.html#create-basic-components).  

## Output from running the hello-world frontend

You can see [screen-shots from the app here](https://lisk.com/documentation/lisk-sdk/tutorials/hello-world.html#the-hello-world-app).  

And here is some output I've gotten from the hello-world app running in WSL on http://localhost:8989

```text
---- New account A
{
  "address": "lskgfgn9t935y476bzmh84u66qqsyykg3wbee2rj3",
  "binaryAddress": "ffbe76cda85c52e51805ebd3052ab5dc634fa2e6",
  "passphrase": "question endorse jeans lonely best law fragile private million treat crew daring",
  "publicKey": "14fea0558aa1ee9ca8f8ee24ebad4e31a7a9b374235961a55f6a2b737d2ffc36",
  "privateKey": "54e44b391606ececf8c3c10551c64d74465b6985508705d159dd846303a066df14fea0558aa1ee9ca8f8ee24ebad4e31a7a9b374235961a55f6a2b737d2ffc36"
}
---- New account B
{
  "address": "lskhzrsfkaw5smg7wahjsco65dy4so3vsuz8dzrc7",
  "binaryAddress": "e825bf53375ecbf75f3de6c6c52f514ed8816e00",
  "passphrase": "symbol hybrid axis success lazy dismiss post exact stock similar town spot",
  "publicKey": "2e3511c103592fdf074967af1e96a9418943351d46b87567fa6ed2f99ca464f4",
  "privateKey": "327b02872163b912cb9081dd2739713740d1be96d9457b8019b2131d4bb6741d2e3511c103592fdf074967af1e96a9418943351d46b87567fa6ed2f99ca464f4"
}
---- fauset get 1
Transaction: {
  "moduleID": 2,
  "assetID": 0,
  "fee": "1000000",
  "nonce": "0",
  "senderPublicKey": "0fe9a3f1a21b5530f27f87a414b549e79a940bf24fdf2b2f05e7f22aeeecc86a",
  "signatures": [
    "06d9be7f2ce567fb3ec3bdf672faa18e5d4a3757bfe607e93ba5ee2444220c210b6afeafab40ad9c72fbc824c1fadcee37dcd6bffc792bebd4482b10855bb90a"
  ],
  "asset": {
    "amount": "100000000",
    "recipientAddress": "ffbe76cda85c52e51805ebd3052ab5dc634fa2e6",
    "data": ""
  },
  "id": "2b967f770289d772dc0fd1428090673e51e0c48895f911c3aedc72c4f0a53451"
}
Response: {
  "transactionId": "2b967f770289d772dc0fd1428090673e51e0c48895f911c3aedc72c4f0a53451"
}

---- send hello - fee = 0,01
Transaction: {
  "moduleID": 1000,
  "assetID": 0,
  "fee": "1000000",
  "nonce": "0",
  "senderPublicKey": "14fea0558aa1ee9ca8f8ee24ebad4e31a7a9b374235961a55f6a2b737d2ffc36",
  "signatures": [
    "76988171cf9a04ac27c1c1e2dbe90240909c820653d249a4e7e96675ebe69a861488d1da2aeb32836448e9d62af833315f1af730cb219c205cb5955ea331fb07"
  ],
  "asset": {
    "helloString": "binor says hello4"
  },
  "id": "36e16d3b5527d2ce5a41e8fa428ca49ad00b7b8b0d8d8f3bb7b9884d46d318d7"
}
Response: {
  "transactionId": "36e16d3b5527d2ce5a41e8fa428ca49ad00b7b8b0d8d8f3bb7b9884d46d318d7"
}

---- account A
Account: {
  "address": "ffbe76cda85c52e51805ebd3052ab5dc634fa2e6",
  "token": {
    "balance": "500099000000"
  },
  "sequence": {
    "nonce": "1"
  },
  "keys": {
    "numberOfSignatures": 0,
    "mandatoryKeys": [],
    "optionalKeys": []
  },
  "dpos": {
    "delegate": {
      "username": "",
      "pomHeights": [],
      "consecutiveMissedBlocks": 0,
      "lastForgedHeight": 0,
      "isBanned": false,
      "totalVotesReceived": "0"
    },
    "sentVotes": [],
    "unlocking": []
  },
  "hello": {
    "helloMessage": "binor says hello4"
  }
}
---- Send transfer to new account - To B, fee = 0,01, amount: 2, passphrase A
Transaction: {
  "moduleID": 2,
  "assetID": 0,
  "fee": "1000000",
  "nonce": "1",
  "senderPublicKey": "14fea0558aa1ee9ca8f8ee24ebad4e31a7a9b374235961a55f6a2b737d2ffc36",
  "signatures": [
    "1dbb1743066d7b579e9f2eaa4a79a0c672a63123b4a352c5674a8530852495b0d29171d4150d5085d1dff478c5e60ddc0aa2518e2475fe274699ee4132b8fb02"
  ],
  "asset": {
    "amount": "200000000",
    "recipientAddress": "e825bf53375ecbf75f3de6c6c52f514ed8816e00",
    "data": ""
  },
  "id": "36486c83140e6df693605b536f74313f6fe713f13536a4c30f2d935339268d9d"
}
Response: {
  "transactionId": "36486c83140e6df693605b536f74313f6fe713f13536a4c30f2d935339268d9d"
}
---- account A
Account: {
  "address": "ffbe76cda85c52e51805ebd3052ab5dc634fa2e6",
  "token": {
    "balance": "499898000000"
  },
  "sequence": {
    "nonce": "2"
  },
  "keys": {
    "numberOfSignatures": 0,
    "mandatoryKeys": [],
    "optionalKeys": []
  },
  "dpos": {
    "delegate": {
      "username": "",
      "pomHeights": [],
      "consecutiveMissedBlocks": 0,
      "lastForgedHeight": 0,
      "isBanned": false,
      "totalVotesReceived": "0"
    },
    "sentVotes": [],
    "unlocking": []
  },
  "hello": {
    "helloMessage": "binor says hello4"
  }
}
---- account B
Account: {
  "address": "e825bf53375ecbf75f3de6c6c52f514ed8816e00",
  "token": {
    "balance": "200000000"
  },
  "sequence": {
    "nonce": "0"
  },
  "keys": {
    "numberOfSignatures": 0,
    "mandatoryKeys": [],
    "optionalKeys": []
  },
  "dpos": {
    "delegate": {
      "username": "",
      "pomHeights": [],
      "consecutiveMissedBlocks": 0,
      "lastForgedHeight": 0,
      "isBanned": false,
      "totalVotesReceived": "0"
    },
    "sentVotes": [],
    "unlocking": []
  },
  "hello": {
    "helloMessage": ""
  }
}
---- home
Hello Lisk!
A simple frontend for blockchain applications built with the Lisk SDK.

Hello counter:

1
Latest Hello:

Message:

binor says hello4
Sender:

ffbe76cda85c52e51805ebd3052ab5dc634fa2e6
```

Done