# Mastering Bitcoin Discussion Questions

This is the weekly discussion questions based on Mastering Bitcoin [2nd edition](https://github.com/bitcoinbook/bitcoinbook) by Bitshala Mastering Bitcoin Cohort, starting on 3rd Feb 2023. ([Apply](https://www.bitshala.org/mb-cohort-form))

## Week 1
----

### Chapter 1: Introduction

- What is the difference between the bitcoin network and bitcoin as a currency? How do they interrelate?

- Why doesn't bitcoin have a hierarchical network structure? What advantages or disadvantages does this bring?

- What is the double-spend problem, and how did bitcoin solve it? Discuss the technical mechanisms involved.

- What kind of privacy exists for transactions on a public ledger like bitcoin? What measures are taken to protect users' identities?

- What determines the rate of inflation in bitcoin? How is this mechanism different from traditional currencies?

- Do you think it would be better if bitcoin transactions were reversible? Discuss the potential benefits and drawbacks.

- Do you believe that bitcoin needs to be competitive with Visa/MasterCard to succeed? Why or why not?

### Chapter 2: How Bitcoin Works

#### Transactions

- What is the smallest unit of Bitcoin? How many of those units make 1 Bitcoin? Can we subdivide the smallest unit into even smaller chunks if the need arise?

- What information does the receiver need to provide to receive bitcoin from the sender?

- What basic information do you need to construct a bitcoin transaction?

- Why are transactions called a "chain of digital signatures"? Explain how spending a coin extends the "chain of digital signatures."

- What is the status of a transaction that has not yet been included in a block but has been propagated around the network?

#### Wallets

- What is a transaction fee, and why is it required? How is it calculated?

- What is change in a bitcoin transaction? When is change needed, and when should it be included or excluded?

#### Blockchain and Mining

- What is Proof of Work mining, and why is it compared to a "needle in a haystack" problem of random draws?

- What is a mining pool, and why would a miner choose to join one?

- What is a blockchain reorganization (reorg), and how does it occur?

- How does the network decide which of two blocks at the same height to add to the chain?

- What is difficulty adjustment in bitcoin mining, and why is it necessary?

- Why do some services require six confirmations before clearing funds?

## Week 2
----

### Chapter 3: Bitcoin Core

- Why is Bitcoin Core referred to as the reference implementation? Are there other widely used implementations?

- Run the unit test suite of Bitcoin Core and see if everything passes. What does this tell you about the software?

- What are Bitcoin Improvement Proposals (BIPs), and what role do they play in determining the Bitcoin protocol?

- Why should you run your own full node? Discuss the benefits and challenges.

- What is the difference between a pruned node and a full (archival) node?

#### bitcoind Configurations

- What are some major configuration options in Bitcoin Core? Provide examples and their significance.

#### bitcoin-cli RPC

- What is bitcoin-cli, and what purposes does it serve?

- List a few of the most important RPC commands you would use as a node operator. Explain their uses.

- What kind of network information can you fetch using RPC? Refer to Clark Moody's Dashboard as a resource.

#### Transactions

- Describe the structure of a bitcoin transaction. What are the fields, and what does each field imply?

#### Blocks

- Describe the structure of a Bitcoin block header. What are the fields, and what does each field imply?

### Chapter 4: Keys, Addresses

#### Elliptic Curves

- Provide a brief history of public key cryptography. Refer to the Diffie-Hellman paper as a resource.

- Describe the functions of private keys, public keys, Bitcoin addresses, and digital signatures. What is the mathematical relationship between them, and how are they used in Bitcoin?

- What is the discrete logarithm problem, and why is it considered hard to solve?

- What is asymmetry in cryptography, and why are one-way functions useful? Identify a one-way cryptographic function used in deriving public keys from private keys.

- Describe instances where private keys have been compromised due to lack of entropy. Why is it important to use a cryptographically secure pseudorandom number generator to produce a private key?

- What is secp256k1, and what are the curve constants used in Bitcoin?

#### Address

- What is a Bitcoin address, and why are addresses used instead of raw public keys?

- What hash functions are used in the generation of Bitcoin addresses?

- Why is Base58 used for Bitcoin addresses instead of Base64? Would you make any modifications beyond Base58?

- What are the different private key formats used by wallets?

- What are compressed public keys, and what are the benefits of compressing a public key?

- What are the different kinds of Bitcoin addresses? Explain the differences between P2PKH and P2SH.

- What is the difference between a hot wallet and cold storage?

## Week 3
---

### Chapter 5: Wallets

- Why does address reuse reduce privacy in Bitcoin? Can you think of other de-anonymizing missteps that might occur due to poor user experience design or lack of privacy education?

#### Wallet Types

- What is a Bitcoin wallet? What are the different types of wallets available?

- What is the difference between deterministic and non-deterministic wallets?

- Why does the author argue that BIP32 wallets are superior?

#### Seed and Mnemonic

- What is a "seed" in the context of Bitcoin wallets? How are mnemonic words generated from the seed?

- What is the optional passphrase for a mnemonic code? Discuss its potential advantages and disadvantages.

#### Extended Keys

- What are XPubs, XPrivs, and Chaincode?

- What are the components of an extended key? What is the fingerprint of a key?

- What are hardened and non-hardened derivations? Why is there a distinction, and what are the advantages of different kinds of derivations?

- Why is a brainwallet not secure, while mnemonic code words are?

### Chapter 6: Transactions

#### Transaction Structure

- What is a Bitcoin transaction, and how is it constructed?

- What are the different components of a Bitcoin transaction?

- What is a coinbase transaction, how are they created, and why are they important?

- What are UTXOs (Unspent Transaction Outputs), and how is the balance of a wallet calculated?

#### Digital Signatures

- What are digital signatures, where are they placed in a transaction, and what is their purpose?

- Describe some real-life exploits that occurred due to poor randomness in digital signatures.

- Besides signing transactions, what other uses could digital signatures have?

#### Transaction Validation

- What are transaction inputs, and how are they constructed? What are unlocking scripts?

- Is the Turing incompleteness of Bitcoin's scripting language (SCRIPT) a feature or a deficiency?

- What is the difference between a locking script (scriptPubKey) and an unlocking script (scriptSig)? What is the difference between a redeem script and a witness script?

- Why are the locking and unlocking scripts executed separately?

- What are sighashes, and what are their uses? How many types of sighashes are there?

## Week 4
---

### Chapter 7: Advanced Transactions and Scripting

- What are some advanced scripting methods possible using Bitcoin scripts? What is not possible?

- What are multisig scripts, and how can they be useful?

- What was the bug in multisig script execution, and why can't we just fix it?

- What is Pay-to-Script-Hash (P2SH), and why was it introduced? What problem does it solve?

- What is OP_RETURN, and do you think non-transactional OP_RETURN data should be allowed in the Bitcoin blockchain?

- What is a transaction lock time? What are the different kinds of time locks available in Bitcoin scripts?

- Time locks (nLockTime) are used to lock funds until a certain time or block height after which they are valid. Is it possible to invalidate transactions after a certain time or block height?

### Chapter 8: The Bitcoin Network

- Do SPV (Simplified Payment Verification) nodes help or hurt the network?

- How many nodes are on the Bitcoin network today? Why is this number significant?

- The Bitcoin Relay Network section describes multiple projects intended to reduce block propagation latency. Why is so much effort being put into this?

- How do new nodes discover peers on the network?

- What are the privacy concerns of using an SPV node?

- What is TOR, and how does it provide privacy for Bitcoin users?

- What happened to the original proposal to add peer-to-peer encryption (BIP150/151)?

## Week 5
---

### Chapter 9: The Bitcoin Blockchain

- The genesis block contains a hidden message within it. What opcode is used for this, and what are some other examples of this opcode being used? Do you think superfluous data should be allowed in the blockchain?

- How much data would be required to calculate a Merkle path for a tree with four transactions?

- What is Signet, and how is it different from Testnet and Regtest?

- Bloom filters have some problems. How are block filters better?

### Chapter 10: Mining and Consensus

- How does mining solve the Byzantine Generals Problem?

- What happens to a transaction that isn't validated by your node?

- What happens if a miner tries to pay itself a higher subsidy than allowed?

- In 2016, there was approximately 3 EH/sec of processing power. Today, there are 150 EH/sec. What is the right threshold for securing the network? Can you have too much security?

- Under what circumstances would a node receive an orphan block? Why wouldn't it be discarded if its parent