# Decentralised-App
Decentralised App 

# Demo 
 > We will build a decentralised voting app . No need to trust anyone  , Tallied votes will not be going to be modified 
 
# But first , what happened to web 
The web started off as 'decentralised' . Everyone who wanted a website bought their own server and hosted the website on it 
But after the DOT-COM Bubble , data started to become centralised 

# This is bad , Real Bad :
It's shrinking the economy
Too much concentrated power
We have no say in how our data is used
We should get paid for our data

> Decentralised systems are those where no node is telling any other node what to do .Bitcoin is both distributed because it's timestamped public ledger , the blockchain ,resides on multiple computer and decentralised because if one node goes down the network is still able to operate <br />
⋅⋅⋅ Multiple servers <br />
⋅⋅⋅ Demand and failure better handled<br />
Examples : `Bitcoin & Ethereum` <br />


So , does a profitable decentralised app look like ? <br />

|                           | `WEB 2.0`     | `WEB 3.0`          |
| ------------------------- |:-------------:| ------------------:|
| Scalable computation      | Amazon EC2    | Ethereum , Truebit |
| File Storage              | Amazon EC3    |  IPFS/Filecoin , storj |
| External Data             | 3rd Party API |   Oracle (Augur)   |
| Monetization              | Ads , selling goods    | Token Model |
| Payments                  | Credit Card, Paypal    |  Ethereum,Bitcoin,state channels   |

# How to run it ?
## Setup an Environment :
> Install `npm install ethereumjs-testrpc web3` <br />
> Install `npm install solc` (for solidity compiler) <br />

## Usage :
vidit:~/hello_world_voting$ node <br />
> Web3 = require('web3') <br />
> web3 = new Web3(new Web3.providers.HttpProvider("http://localhost:8545")); <br />
> code = fs.readFileSync('Voting.sol').toString() <br />
> solc = require('solc') <br />
> compiledCode = solc.compile(code)  <br />
> abiDefinition = JSON.parse(compiledCode.contracts[':Voting'].interface) <br />
> VotingContract = web3.eth.contract(abiDefinition) <br />
> byteCode = compiledCode.contracts[':Voting'].bytecode <br />
> deployedContract = VotingContract.new(['Rama','Nick','Jose'],{data: byteCode, from: web3.eth.accounts[0], gas: 4700000})  <br />
> deployedContract.address  <br />
> contractInstance = VotingContract.at(deployedContract.address)  <br />
