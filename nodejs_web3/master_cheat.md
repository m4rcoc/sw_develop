
# Installation of NodeJS and Web3 library

1. Go to nodejs.org and download the corresponding installer (follow its instructions)

2. Verify the installation:

```console
node -v
npm -v
```

3. Install web3 package:
```console
npm install --save web3
```


# Installation of Truffle and Ganache
1. Truffle Suite:
```console
npm install -g truffle
```

2. Ganache CLI:
```console
npm install -g ganache-cli
```
check if command "ganache-cli" exists

3. Ganache GUI:

[Official Web page to download](https://trufflesuite.com/ganache/)

NOTE: for Linux installation, download .AppImage file from the github repository, get permissions and execute the file

# Interact with Smart Contract on the lowest level:

```console
node
> let Web3 = require("web3");
> let web3 = new Web3(new Web3.providers.HttpProvider("http://localhost:7545"));
> web3.eth.getBalance("0x95a5A04A708b8Be3927d2160386e203C07EBA837").then(function(result) {console.log(web3.utils.fromWei(result,"ether"));});
> web3.eth.sendTransaction({from:"0x95a5A04A708b8Be3927d2160386e203C07EBA837" , to:"0x6b56adEA1c7fB0EA7b65f00177015E332F18750b" , value:web3.utils.toWei("1","ether")});
```