# Week 1

## Chapter 1: Introduction

- What were the major problems of Digital Currencies before Bitcoin? How did Bitcoin solve them?
- What are the major components of the Bitcoin System? What does it mean by "consensus rules"?
- What are the different types of Bitcoin Wallets? Which one among them is most and least secured?
- What are the different types of Bitcoin Nodes? What are the tradeoffs between them? When is it applicable to use a "light node"?
- Do you think it would be better if bitcoin transactions were reversible? What are the potential benefits and drawbacks?
- Do you believe Bitcoin needs to compete with Visa/MasterCard to succeed? Why or why not?


## Chapter 2: How Bitcoin Works

- What is transaction fee? How is it calculated? Whats the effect of transaction fee on transaction confirmation?
- What are the two main components of a Transaction? What does each component include?
- What are change addresses? When are change addresses required? What happens if the user (or wallet sofwtware) forgets to include the change address in a transaction? When will we not require a change address?
- What does coinselection mean? Can you name few popular coinselection algorithms? Is it better to manually select coins or let the wallet software automatically handle it?
- How is Proof of Work mining similar to "needle in haystack" problem? What happens when two blocks are mined by different miners at the same height, how does the network decide which is the "right" block?
- What does it mean by a transaction to be "confirmed"? How many confirmations is usually acceptable? Is it okay to accept unconfirmed transactions? Why or why not?


--------------


# Week 2

## Chapter 3: Bitcoin Core

- Why is Bitcoin Core called a "reference implementation"? What other implementation of Bitcoin are out there? Is it preferable to have many implementation of Bitcoin?

- What are BIPs? What are their role in the Bitcoin development process?


## Chapter 4: Keys and Addresses

### Elliptic Curves

- Describe the functions of ‘private keys’, ‘public keys’, ‘Bitcoin addresses’, and ‘digital signatures’. What is the mathematical relationship between them and how are they used in Bitcoin?

- What is the discrete logarithm problem, and why is it considered hard to solve?

- What is asymmetry in cryptography, and why are one-way functions useful? Identify a one-way cryptographic function used in deriving public keys from private keys.

- Describe instances where private keys have been compromised due to lack of entropy. Why is it important to use a cryptographically secure pseudorandom number generator to produce a private key? What are some techniques of generating pseudo random numbers?

- What is secp256k1, and what are the curve constants used in Bitcoin? How is ECDSA malleable?

+### Address

- What is a Bitcoin address, and why are addresses used instead of raw public keys?

- What hash functions are used in the generation of Bitcoin addresses?

- Why is Base58 used for Bitcoin addresses instead of Base64? Would you make any modifications beyond Base58?

- What are the different private key formats used by wallets?

- What are compressed public keys, and what are the benefits of compressing a public key?

- What are the different kinds of Bitcoin addresses? Explain the differences between P2PKH and P2SH.

- What is the difference between a hot wallet and cold storage?

- What is bech32? How is it better than base58? Are there any problems in bech32? How are they solved?

--------------

# Week 3

## Chapter 5: Wallet Recovery

- Why does address reuse reduce privacy in Bitcoin? Can you think of other de-anonymizing missteps that might occur due to poor user experience design or lack of privacy education? What institutes perform the most address reuse?

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


## Chapter 6: Transactions


--------------

# Week 4

## Chapter 7: Authorization and Authentication


## Chapter 8: Digital SIgnature


--------------

# Week 5

## Chapter 9: Transaction Fess


## Chapter 10: The Bitcoin Network

- What is a peer-to-peer network? Give two examples of successful peer-to-peer networks that preceded Bitcoin.
- What is a block finding race? How does compact block relay prevent it?
- How does a new node discover other Bitcoin nodes on the network in order to participate?
- How do light weight clients validate that a transaction exists? How is this different from the mechanism full archival nodes use to validate a transaction?
- What are bloom filters? How do they work?
- What are compact block filters? What data should be included in a block filter?
- What are the privacy trade-offs in using a light weight client?
- Explain in brief what is a Mempool and what is an Orphan Pool.
--------------

# Week 6

## Chapter 11: The Blockchain

- How is the Bitcoin blockchain analogous to layers in a geological formation?
- Describe the structure of a block and what data does a block header contain?
- What are the two identifiers of a Block? Discuss each in brief.
- What is a Merkle Tree and what significance does it have in Bitcoin?
- What is a design flaw in the Merkle Tree used in Bitcoin?
- What is a Light Weight Client in context to Bitcoin? How do Light Weight Clients verify transactions associated to their addresses?
- Explain mainnet and testnet in brief.
- Explain signet and regtest in brief.

  
## Chapter 12: Mining and Consensus


--------------

# Week 7

## Chapter 13: Bitcoin Security


## Chapter 14: Second-Layer Applications


--------------

