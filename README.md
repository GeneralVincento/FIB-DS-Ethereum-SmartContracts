# FIB-DS-Ethereum-SmartContracts

## Description
Lab solution in course Decentralized Systems, FIB UPC - Leonard Halling and Aksel Vincent Berg.

As the scope of the lab description states, we will implement and evaluate a Decentralized Application [*dApp*]. The dApp that is going to be made is a **Lottery System** built upon **Smart Contracts**, deployed on the **Ethereum Platform**.

### Deadlines
* **Tuesday 08.05.2018**: Intermediate results presentation.
* **Tuesday 31.05.2018**: Final presentation.

### Links/resources
* [Ethereum](https://www.ethereum.org)
* [Ethereum White Paper](https://github.com/ethereum/wiki/wiki/White-Paper)
* [Cyberdice P2P gambling](http://www.cl.cam.ac.uk/%7Efms27/papers/2008-StajanoCla-cyberdice.pdf)
* [Remix](https://remix.ethereum.org/)
* [Truffle](https://github.com/trufflesuite/truffle)
* [Intro to Ethereum smart contract w/ Solidity, Part I](https://www.youtube.com/watch?v=8jI1TuEaTro)
* [Intro to Ethereum smart contract w/ Solidity, Part II](https://www.youtube.com/watch?v=3-XPBtAfcqo)
* [Intro to Smart Contracts](https://solidity.readthedocs.io/en/develop/introduction-to-smart-contracts.html)
* [Solidity tutorial](https://ethereumbuilders.gitbooks.io/guide/content/en/solidity_tutorials.html)
* [Solidity tutorial 2](http://truffleframework.com/tutorials/pet-shop)
* [Ganache](http://truffleframework.com/ganache/)
* [MetaMask](https://metamask.io/)
* [Predicting random numbers in Ethereum Smart Contracts](https://blog.positive.com/predicting-random-numbers-in-ethereum-smart-contracts-e5358c6b8620)


## Keywords - Intermediate presentation
- A quick summary of smart contracts.
- A quick summary of the lottery rules.
- Fully implemented the functionality of the Lottery.
- Explain the function of each file, and maybe keywords as well.
- Which technologies are used? Why? A short description of each.
- Teaser of what the final presentation is going to regard.

## Keywords - Final presentation
- Why is it better to implement this on a blockchain, in a decentralized way, compared to using a centralized server.
- Show how it is implemented in a test environment, and what to change in order to deploy it on the actual Ethereum blockchain.
- Different rules for lottery. Different methods we could have used in order to determine the winner.
- How to generate random number? The code should be deterministic since it runs on multiple (16k) nodes. I think this might be one of the main issues and subjects of our presentation. 
- Clock time is not available on Ethereum. How to decide when to pick a winner.
- What is gas? How to implement the code in order to minimize gas cost.



## How to deploy a Smart Contract implementation on Ethereum test blockchain
1. run *truffle init*
2. Copy-paste the following to *truffle.js*
```javascript
module.exports = {
  networks: {
    development: {
      host: "127.0.0.1",
      port: 8545, // your rpc port (like geth rpc port or testrpc port )
      network_id: "*"
    }
  }
};
```
3. run *testrpc*
4. run *truffle compile*
5. run *truffle migrate --reset*
6. run *truffle console*
7. NameOfFile.deployed().then(function(instance){objectName=instance})
  - objectName.getValue()
  - objectName.setValue("Values", "to", "insert")

## Smart Contract Lottery

### Rules
A generic description of the smart contract lottery system.

* Each player inputs certain amount of Ether in the lottery.
* When the lottery cap has been reached, the lottery will start.
* There’s a limit of how much Ether one participant can insert.
* The chances of winning is based on the amount of Ether inserted by each participant.
* When the winner has been decided, the winnings will be rewarded to the winner, and the other participants will be notified that the game has ended.


