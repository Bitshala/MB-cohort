# Mastering Bitcoin Discussion Questions

This is the weekly discussiion questions based on Mastering Bitcoin [2nd edition](https://github.com/bitcoinbook/bitcoinbook)  by Bitshala Mastering Bitcoin Cohort, starting on 3rd Feb 2023. ([Apply](https://www.bitshala.org/mb-cohort-form))

## Week 1
----

### Chapter 1:

 - What is the difference between the bitcoin network and bitcoin as a currency?

- Why doesn't bitcoin have a hierarchical network?

- What is the double-spend problem and how did bitcoin solve it?

- What kind of privacy is there for transactions on a public ledger?

- What determines the rate of inflation in bitcoin?

- Do you think it would be better if bitcoin transactions were reversible?

- Do you believe that bitcoin needs to be competitive with visa/mastercard to succeed?

### Chapter 2:

#### **Transactions**

- Whats the smallest unit of Bitcoin?

- What does the receiver need to send to receive bitcoin from the sender?

- What basic information do you need to construct a transaction?

- Why are transactions called "chain of Digital Signatures"? Explain spending of a Coin as extending the "chain of digital signatures" one step further.

- What is the status of a transaction that has not yet been included in a block, but has been propagated around the network?


#### **Wallets**

- What is a transaction fee? Why is it required? How is it calculated?

- What is change? When is change needed?  When to include change when not to change?


#### **Blockchain and Mining**

- What is Proof of Work mining, and how is it like a needle in a haystack problem of random draws.

- What is a mining pool and why would someone belong to one?

- What is a Reorg?

- How does the network decide on which of the two blocks to add to the chain at the same height?

- What is difficulty adjustment?

- Why do some services require 6 confirmations to clear funds?


## Week 2
----

### Chapter 3:
#### **Bitcoin Core**

- Why is Bitcoin Core referred to as the reference implementation? Are there other widely used implementations?

- Run the unit test suite and see if everything passes.

- What are Bitcoin Improvement Proposals (BIPs) and what role do they play in determining the Bitcoin protocol?

- Why should you run your own full node?

- What is the difference between a pruned node and a full (AKA archival) node?


#### **bitcoind configurations**

-  What are some major configuration options in bitcoin core (according to you). [Add example config gen instruction]

#### **bitcoin-cli RPC**

- What is bitcoin-cli, for what purposes it can be used?

- List a few of the most important RPC commands you would use as a node operator?

- What kind of network information can you fetch from rpc (resource: [Clark Moddy's Dashboard](https://bitcoin.clarkmoody.com/dashboard/)).


#### **Transactions**

-  Describe the bitcoin transaction structure. What are the fields? What does each field imply?

#### **Blocks**

-  Describe the Bitcoin Block Header structure. What are the fields? What does each field imply?

### Chapter 4:

#### **Elliptic Curves**

- History on Public Key cryptography (resource : the Diffy helman paper)


- Describe the functions of ‘private keys’, ‘public keys’, ‘Bitcoin addresses’, ‘digital signatures’. What is the mathematical relationship between them and how are they used in Bitcoin?

- What is the ‘discrete logarithm problem’? How do we know that the discrete log problem is hard to break?

- What is asymmetry? Why one-way functions are useful? What is a one-way cryptographic function used in deriving publick keys from private keys?

- What are some ways that private keys have been broken because of lack of entropy? Why is it important to use a cryptographically secure pseudorandom number generator to produce a private key?

- What is secp256k1? What are the curve constants used in Bitcoin?


#### **Address**

- What is an address. Why do we need addresses and just not send bitcoin to raw public keys?

- What hash functions are used in address generation?

- Why do we use Base58 for addresses rather than Base64? Would you make any modifications beyond Base58?

- What are different Private key formats used by wallets?

- What are compressed public keys? What are the benefits of compressing a public key?

- What are the different kinds of addresses? What is the difference between P2PKH and P2SH?

- What is the difference between a hot wallet and cold storage?


## Week 3
---

### Chapter 5

- Why does address re-use reduces privacy? Can you think of other de-anonymizing missteps that might happen due to bad user-experience design or lack of privacy education?


#### **Wallet Types**

- What is a Bitcoin Wallet? What are the different types of wallets out there?

- Whats the diff between deterministic and non-deterministic wallets??

- Why does the author argue that BIP32 wallets are a superior wallet?

#### **Seed and Mnemonic**

- What is a "Seed"? How are the mnemonic words generated from the Seed?

- What is the optional passphrase to a mnemonic code? What are its possible advantages/disadvantages?

#### **Extended Keys**

- What are XPubs, XPrivs and Chaincode?

- What are the components of an Extended Key? What is the Fingerprint of a key?

- What are hardened and non hardened derivations? Why the distinction? What are the advantages of having different kind of derivations?

- Why is a brainwallet not secure, but mnemonic code words are?

### Chapter 6

#### **Transaction**

- What is a Bitcoin Transaction? How is a Transaction constructed in Bitcoin?

- Different components of transactions

- What is a Coinbase Transaction? How are they created and why?

- What are UTXOs? How is the balance of a wallet calculated?

#### **Digital Signatures**

- What are digital signatures? Where are they placed in a transaction? What is their purpose?

- What were some real life exploits that happened due to poor randomness in digital signature?

- Besides signing transactions, what could be other uses of digital signatures?


#### **Transaction validation**

- What are Transaction inputs and how are they constructed? What are unlocking scripts?

- Is SCRIPT's Turing incompleteness a feature or a deficiency?

- What is the difference between locking script and Script Pubkey? What is the difference between redeem script and witness script?

-  Why are the locking and unlocking scripts executed separately?

- What are `sighashes`? What are their use? How many types of `sighashes` are there?


## Week 4
---

### Chapter 7

- What are some advanced scripting methods possible using Bitcoin Scripts? What's not possible?

- What are multisig scripts? How they can be useful?

- What was the bug in multisig script execution? Why can't we just fix it?

- What is Pay-to-Script-Hash (P2SH)? Why were they introduced and what problem does it solve?

- Whats an `OP_RETURN`? Do you think non transactional `OP_RETURN` data should be allowed in the Bitcoin blockchain?

- What is a Transaction Lock Time? What are different kinds of time locks available with Bitcoin scripts?

- Timelocks (`nlocktime`) are used to lock funds until a certain time or   `blockheight` after which they are valid. Is it possible to invalidate transactions after a certain time or `blockheight`?


### Chapter 8

- Do SPV nodes help or hurt the network?

- How many nodes are on the Bitcoin network today?

- The Bitcoin Relay Network section describes multiple projects intended to reduce block propagation latency. Why is so much effort being put into this?

- How do new nodes discover peers on the network?

- What are the privacy concerns of using an SPV node?

- What is TOR and how does it provide privacy?

- What happened to the original proposal to add p2p encryption (BIP150/151)?


## Week 5
---

### Chapter 9

- The genesis block contains a hidden message within it. What `OP_CODE` is used for this and what are some other examples of this `OP_CODE` being used? Do you think superfluous data should be allowed in the blockchain?

- How much data would be required to calculate a Merkle path for a tree with 4 transactions?

- What is `signet` and how is it different than `testnet` and `regtest`?

- Bloom filters have some problems, how are block filters better?

### Chapter 10

- How does mining solve the Byzantine Generals Problem?

- What happens to a transaction that isn't validated by your node?

- What happens if a miner tries to pay itself a higher subsidy than allowed?

- In 2016, there was ~3 EH/sec of processing power. Today there are 150 EH/sec. What is the right threshold for securing the network? Can you have too much security?

- Under what circumstances would a node receive an orphan block? Why would it not be discarded if its parent hasn't been received? How long should a node wait? Do you see any problems with keeping it for a long time?

- A 10-minute block interval was set by Satoshi. Is that too slow? How might we speed it up? What problems might be caused by a shorter interval?

- How is work by a miner monitored by pools? Can this be gamed?

- How do p2p pools work? Why is this not the main method for pooling used?

- What are the largest pools today and what risk do they pose?

- What prevents miners from signaling that they will support an upgrade but later not enforce it?

- Upgrades have become increasingly more difficult to get merged and accepted by the community. Should we make it easier? If so, how?

## Week 6
---
### Chapter 11

- Bitcoin's security relies on decentralized control over keys and on independent transaction validation by miners. Are there instances when centralization might be appropriate or even encouraged?

- How do developers of the protocol fit into the trust model? What safeguards are in place to ensure there are no single points of failure?

- How can we protect ourselves from the thousands of software components that run on our personal computers?

### Chapter 12

- What do you see as the biggest weakness of the Lightning Network?

- Do you think the punishment mechanism in the Lightning Network incentivized the right kind of behavior?

- People say that the Lightning Network is better for privacy, but each node has a persistent identity, so how is that possible?

- Lightning sounds complicated. Can't we just use unidirectional payment channels? It's not like my coffee shop will ever be paying me, right?
