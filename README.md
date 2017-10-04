# PlusCoin - cryptocurrency for the people

[![PlusCoin](https://pluscoin.io/images/dsp/pluscoin_alpha_cut.png)](https://pluscoin.io/images/dsp/pluscoin_alpha_cut.png)

**PlusCoin** is a cryptocurrency, which provides the basis for a cashback platform of the DSPlus company. It is a marketing instrument for offline and online enterprises to attract new gamers and consumers based on the Blockchain technology. 

# Smart-contracts

PlusCoin smart-contract contains:

  - The SafeMath library for protection against overflow during arithmetic operations. 

  - Standard ERC20 functions and events (only the owner of the smart contract can use these functions during the Presale and ICO 1-3 stages):
    - `function balanceOf(address _owner) constant returns (uint256 balance) {}`
    Returns the balance in coins held at a given address;
    - `function transfer(address _to, uint256 _value) returns (bool success) {}`   
    Sends coins (from the sender’s balance) to a given address;
    - `function transferFrom(address _from, address _to, uint256 _value) returns (bool success) {}`
    Sends coins from a given address to a given address, if the owner of the address to be deducted from has permitted this operation;
    - `function approve(address _spender, uint256 _value) returns (bool success) {}`
    Permits the deduction of a given quantity of coins from a given address from the message sender’s account;
    - `function allowance(address _owner, address _spender) constant returns (uint256 remaining) {}` 
    Returns the total quantity of coins that can be deducted from a given address by another address.

  - Public variables and constants:
    - `name` – token name;
    - `symbol` – token symbol;
    - `decimals` – number of digits the cryptocurrency has after the decimal point;
    - `totalSupply` – total supply of coins;
    - `PRESALE_PRICE` – price fort 1 ether;
    - `current_state` – current state of the contract;
    - `OWNER_MIN_LIMIT` – minimum quantity of coins;
    - `TOKEN_PRESALE_LIMIT` – – limit on coin sales during the Presale stage;
    - `TOKEN_ICO1_LIMIT` – –limit on coin sales during the ICO 1 stage;
    - `TOKEN_ICO2_LIMIT` - –limit on coin sales during the ICO 2 stage;
    - `TOKEN_ICO3_LIMIT` - –limit on coin sales during the ICO 3 stage.

  - Functions for the Presale and ICO stages, etc.:
    - `function transferOwnership(address newOwner) onlyOwner {}`
    Allows the contract owner transfering ownership to another party;
    - `function buy() public payable {}`
    Function for coin purchase from the contract owner at a fixed price; active only during the Presale and ICO 1-3 stages;
    - `function buyTokens(address _buyer) public payable {}
    Function for purchasing coins and credit them to a given address;
    - `function get_token_state() public constant returns (State) {}`
    Get the current state of the contract;
    - `function setTokenState(State _nextState) public onlyOwner`
    Change the contract status;
    - `function remaining_for_sale() public constant returns (uint remaining_coins)`
    Returns the remaining quantity of coins for sale during the current stage, in accordance with the set limit.
    
Possible statuses: Created, Presale. ICO1, ICO2, ICO3, Free trading, Pause. Statuses can only be changed in one direction (from ‘Created’ to ‘Free trading’). However, the smart contract owner can halt sales at the Presale stage by putting the contract into the ‘Pause’ state. This is necessary to protect against unforeseen circumstances. Transition to the Pause state and back is only possible during the Presale and ICO stages.

The main smart contract, according to the ERC20 standard, provides basic functions for PlusCoin tokenholders:
  - an opportunity to check PLC balance on a wallet address;
  - an opportunity for a wallet owner to send PLC to any other wallet;
  - an opportunity for a wallet owner to allow a certain amount being deducted in a benefit of another address (allowance);
  - an opportunity to deduct coins from a given wallet address with permission of the owner.

Support of these functions allows using PlusCoin as a common cryptocurrency based on the Ethereum Blockchain (including placement on the exchange services).

# Additional contracts

We are not going to be limited by standard ERC20 functionality; therefore we are actively developing additional smart contracts which will interact with the basic one. These contracts will provide operation of the DS Plus service in the blockchain-network. The publication of additional smart contracts won't affect the work of the basic one and WONT'T be followed by release of new "coins" instead of PlusCoin. Additional smart contracts will provide correct interaction of the DS Plus service functionality and the basic PlusCoin contract.

DS Plus team sees a great prospects and opportunities, which are showed because of using blockchain-technologies in real world. Using of smart-contracts in business processes of companies, public and social spheres is irreversible. It’s about time. That’s why we constantly monitor for new developments in smart-contract sphere, learning the possibilities of applying it. Also we prepare our own contracts, which will provide:
 -making safe and clear deals in DS Plus partner-companies and also in our online Market place
-making safe and clear deals on P2P-platform in DS Plus app(deals with or without the mediator)
-introduction of definition of digital property, which changes the holder because of making a deal
-introduction of “cryptoscoring”(rating) for PlusCoin holders, base for making the decision, for example, of crediting one or another PlusCoin holder
-providing secure credit deals(including p2p crediting)
At the moment we are testing contract for deals, containing cryptoscoring functions. Code of this contract will be published in current repository as soon as possible, after we finish the testing and external audit.
Besides, we go beyond above-mentioned functions and constantly discuss and work on new ideas for implementation blockchain-technologies into real life. 

### Additional materials
For additional information on this project please follow the links to our official channels:
* [Facebook] - official group on Facebook
* [Telegram] - official Telegram-channel
* [Pluscoin.io] - official PlusCoin web-site
* [Youtube] - official Youtube channel

If you have any questions you can write us to our e-mail address mail@dsplus.pro
Thank you for your attention to our project!


[//]: #

   [Facebook]: <https://www.facebook.com/dsplus.fork?fref=ts>
   [Telegram]: <https://t.me/joinchat/C9pDig06uYbTgoEq6N4ShQ>
   [Pluscoin.io]: <http://pluscoin.io>
   [Youtube]: <https://www.youtube.com/channel/UCeniN6CmMqp_ujbkWtSmaEA>
