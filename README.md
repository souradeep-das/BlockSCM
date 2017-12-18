
1. [Link to demo-video](https://youtube.com)<br>
2. [Link to contract deployed & tested on the Ropsten network](https://ropsten.etherscan.io/tx/0x04410d805f46d05dccd69c5e2a6a7c26d76cbf9403c4792658720df9eb93c1d3) <br>

## BlockSCM - Supply Chain Management 3.0
The Automobile industry's supply chain is massive logistical arrangment that is an integral part of any automobile manufacturing company. It mediates between multiple parties, and optimizes the creation of distribution of resources, but the presence of numerous interacting parties, differential pricing, and quality & complicance issues create a logistical nightmare which wastes both time and resources. The [failure of Boeing's supply chain for 787](http://www.maxqtech.com/3-true-stories-of-supply-chain-management-disasters-and-how-to-avoid-them/) led to a disastrous 3 year delay of their product. Using that as a case-study, we show blockchains are currently the best-suited solution to the problems in current supply chain infrastructure.

### The Problem
1. **Differential Pricing**: Companies prefer keeping their pricings a secret, since this allows them to pay lower prices when outsourcing to developing countries.
2. **Numerous Parties Invovled**: Mediating between so many parties can be a big problem for logistics-providers, slowing down the delivery of services and creating a large overhead for logistics. Furthermore, a centralized mediator of these parties can misuse power to perfer some parties over others.
3. **Quality & Compliance issues**: Procuring a replacement for defective parts is a long-drawn and uncomfortable process.
4. **Inevitable disruptions**: LEAN "on-demand" manufacturing falls flat in a situations where natural disasters and socio-economic problems are common. For example, Japan (frequently affected by earthquakes) has outsourced most of it's supply chain logistics to other countries.
7. **Centralization**: A central mediator for parties is required, which centralizes power in the hands of a few and is a gateway to misuse of resources.
8. **Fraud by Middlemen**: As number of interacting parties increase, there is a proportional increase in middlemen. They lead to fraud and slow down the supply without adding anything to the network.
9. **Tracking history of any product**: Validating identity vendor and checking for tampering by middlemen is not possible.

### How can blockchains help?

| Problems | How our solution solves them |
| --- | --- |
| Differential Pricing | Permissioned ledger for confidential transactions between parties |
| Numerous parties invovled | Consensus between multiple parties is maintained through Smart Contracts |
|  Quality & Compliance issues | Smart contract stores money while all solutions are checked and tested |
| Inevitable disruptions | Digital ledger is free of geographical constraints like natural disasters, socio-economic issues |           
| Procuring replacements for defective pieces | Smart contract only lets out payments once both parties satisified |
| Centralization | Risk of fraud is mitigated by using decentralized nodes for checking delivery status |
| Fraud by Middlemen | Because of using doubly-signed smart contracts, no financial fraud by middlemen can occur in the system |
| Tracking supply-chain history of each part | Using our network's merkle trees we can verify vendor identity and validity of product |


<img src="https://raw.githubusercontent.com/SatoshiNextTechLab/TheSpareRoute/master/GUI%20SCM.png">

<solution>
As we observe, the problems are both financial (interests, maintenance of accounts) and organisations (central authority => corruption). Blockchains are a unique solution which addresses both these issues. ***Blockchains are a fundamentally new way of not just organising financial capital but also social capital.*** A new way of organising finances and power in rural microfinancial groups.

__**To solve these problems, we've created an Aadhar-linked digital pan-Indian capital-pooling network. Through this network, MAXIMUM POSSIBLE microloan requests are fully funded with 0% interest (least request satisfied first) and the reserve wealth is re-distributed into the system.**__ People can exit the network by requesting their deposited money, which they’ll receive once the loans given are repayed back. This systems allows workers to not only fund each other, but also get microloans for seed-funding their own businesses.

This allows villagers all across India to pool their resources and receive **interest-free microloans** from the network. Blockchain tech enables micro-transactions (which allows for a greater inclusion for poverty-stricken individuals), automatic bookkeeping (no delay or pathy maintenance of ledgers on-chain) in a transparent (all chain transactions are open) manner. We remove the need for a group managing authority (decentralized smart contract). By needing consent from previous members to enter the network and making them accountable for him, **we introduce peer pressure into the network**. This [lowers chances of non-repayment of loans](https://www.microfinancegateway.org/library/microfinance-and-mechanics-solidarity-lending-improving-access-credit-through-innovations).

### Protocol
1. Manufacture requests parts from OEM.
2. 
3. 
4. 

This protocol has been coded into a smart contract from scratch, specifically for the use-case of automobile supply chains. This protocol has been deployed and tested on the Ropsten network. The link to that deployed contract can be [found here](https://ropsten.etherscan.io/tx/0x04410d805f46d05dccd69c5e2a6a7c26d76cbf9403c4792658720df9eb93c1d3).



## Architecture and Tech-stack

![System Architecture](https://raw.githubusercontent.com/SatoshiNextTechLab/TheSpareRoute/master/UML%20SCM.jpg)


### Architecture Modules
##### 1. Add parts
Initial members of the network call add_member to add a new person to the network, once they've validated his identity using Aadhar.
##### 2. Buy parts show price
The newly added member must deposit money to the pool to be able to request a loan.
##### 3. Use OEM parts
A person can request a loan if 
  1. He has been validated by 4 existing members
  2. He has deposited some amount of money
##### 4. Pay to OEM
All loan request are sorted in increasing order of loan-request amount. Every three months, the money in pool is used to fullfill the maximum number of loan-requests. Any reserve wealth in the pool is re-distributed back to the network. The is the function of pay_loan.
##### 5. Part to vehicle

##### 6. Check part location

##### 7. Vehicle assembled

##### 8. Showroom





### Tech Stack
1. Ethereum smart constracts (in solidity)
2. Ropsten testnet  
3. Truffle framework
4. MetaMask
5. Remix IDE
6. Web3.js
7. Aadhar_validator.js


##### Steps to compile in Truffle
1. git clone https://github.com/jangidkrishna/0xSHG.git
2. truffle compile
3. truffle migrate
4. truffle console
5. Interact using Web3.js


##### Steps to compile GUI
1. clone repo https://github.com/jangidkrishna/0xSHG.git
2. cd into 0xSHG-master/GUI
2. npm install .
3. gulp serve


## Possible problems
1. Adoption : Initial adoption of the system might be slow due to technical illiteracy, but [NABARD's E-Shakti initiative](https://eshakti.nabard.org/Aboutus.aspx) has shown us that once a few villages are tested, [adoption is exponential](https://eshakti.nabard.org/Downloads/EShakti%20Brochure%202017A.pdf).

2. Difference in unit of currency: The solution model requires ether/wei as the basic unit of currency. However, a similar system can be put in place for the government's cryptocurrency LakshmiCoin.

3. Possibility of leftover reserves in pool: After the distribution of loans every 3 months, there is a possibility that some amount of pool money is left unused (all loan requests satisfied). This reserve can be utilised by redistributing it equally into the network.

4. If everyone exits the network at the same time: Though this is extremely improbable, if this happens everyone in the system will have to wait 3 months to receive their money back, with possibility of losses to initial deposit (in case someone defaults and all consentees have exited network).


## Built by undergraduates at [Next Tech Lab, SRM University](http://nextech.io/index2.html)
