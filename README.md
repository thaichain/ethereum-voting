## Simple and secure voting system with Ethereum

This is an implementation of a simple and secure electronic voting system using Blockchain technology proposed [here](https://github.com/arikan/bitcoin-voting)

It is implemented as a Smart Contract on Ethereum. Although the proposal was originally designed to be implemented on the Bitcoin Blockchain.

The code follows the Condition-Orientated Programming (COP) methodology proposed by Gavin Wood. [More info](https://medium.com/@gavofyork/condition-orientated-programming-969f6ba0161a#.qoh9uadsb)


#### Requirements:

* All actors of the election should be able to have an Ethereum account.
* All actors of the election should be able to have a little amount of ether to pay for the gas needed to execute the Smart contract.
* All actors of the election should be able to secure their voting computer.

#### Actors:

* Election Authority
* Candidate
* Voter

#### Terminology:

* Blockchain: Distributed database that stores the code of the Smart contract and the interaction between the users and the application in the form of transactions.
* Smart contract: A piece of code that is excecuted on the Ethereum Blockchain.
* Ether (ETH): The cryptocurrency used in Ethereum.
* Gas: The amount of ether that you have to pay to have your transactions accepted in the Ethereum Blockchain.

#### Schema:

0. **Election Authority declaration:**
 - Election Authority publish the code of the Smart Contract on the Ethereum Blockchain and publicly announces its address.

1. **Voter registration:**
 - Voters show a valid ID and provide their Ethereum address to Election Authority.
 - All voter Ethereum addresses are publicly listed in the Blockchain by Election Authority using the function "register_voter".
 - To carry out citizens' right to vote anonymously, the Election Authority keeps the IDs to prevent double registration but does not keep a record of association between the IDs and the provided Ethereum addresses.

2. **Candidate registration:**
 - Candidates provide a valid ID to Election Authority.
 - All Candidate unique names are publicly listed in the Blockchain using the function "register_candidate".
 - As opposed to Voter registration, Election Authority stores and publicly announces a record of association between each candidate ID and their provided name.

3. **Starting the election:**
 - Election starts when Election Authority sets the duration of the election using the function "start_election".

4. **Voting:**
 - Voters vote for their preferred candidate's name publicly listed in the Blockchain using the function "vote".

5. **Election result:**
 - Any vote before the start datetime and after end datetime will not be accepted by the Smart Contract.
 - Any vote from an unauthorized Ethereum address will not be accepted by the Smart Contract.
 - Only one vote from each authorized Ethereum address will be accepted by the Smart Contract.
 - Election result can be audited in real time in the Blockchain.
 - Any vote to an unregistered candidate will not be valid.
 - The whole process from the registrations to the voting and counting the results is open to audition by anyone.

#### Contribution

This basic schema can be implemented today with the existing infrastructure. One can develop applications and interfaces for better user experience of this system. Please send your comments and questions on issues and feel free to fork the repository and send pull requests.

[Original proposal](https://github.com/arikan/bitcoin-voting) (with Bitcoin)

#### License

[The MIT License (MIT)](https://github.com/arikan/bitcoin-voting/blob/master/LICENSE)
