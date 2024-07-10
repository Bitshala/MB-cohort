# Week 1

## Chapter 1: Introduction

- What were the major problems of Digital Currencies before Bitcoin? How did Bitcoin solve them?
- What are the major components of the Bitcoin System? What does it mean by "consensus rules"?
- What are the different types of Bitcoin Wallets? Which one among them is most and least secured?
- What are the different types of Bitcoin Nodes? What are the tradeoffs between them? When is it applicable to use a "light node"?
- Do you think it would be better if bitcoin transactions were reversible? What are the potential benefits and drawbacks?
- Do you believe Bitcoin needs to compete with Visa/MasterCard to succeed? Why or why not?
- What is the Bitcoin Issuance Rate? How do we know the supply cap of Bitcoin is 21 million?
- Is Bitcoin private? Does Bitcoin need to be private? Why isn't Bitcoin fungible?


## Chapter 2: How Bitcoin Works

- What is transaction fee? How is it calculated? Whats the effect of transaction fee on transaction confirmation?
- What are the two main components of a Transaction? What does each component include?
- What are change addresses? When are change addresses required? What happens if the user (or wallet sofwtware) forgets to include the change address in a transaction? When will we not require a change address?
- What does coinselection mean? Can you name few popular coinselection algorithms? Is it better to manually select coins or let the wallet software automatically handle it?
- How is Proof of Work mining similar to "needle in haystack" problem? What happens when two blocks are mined by different miners at the same height, how does the network decide which is the "right" block?
- What does it mean by a transaction to be "confirmed"? How many confirmation is usually acceptable? Is it okay to accept unconfirmed transactions? Why or why not?
- What is the lowest denomination of Bitcoin? Can we run out of decimals to denominate the smallest unit, as Bitcoin adoption increases?
- Why did Satoshi said transactions are "chain of digital signatures"? What is a UTXO? Whats the difference between UTXO and Account based model? Why did Bitcoin choose to stick with UTXO model?



--------------


# Week 2

## Chapter 3: Bitcoin Core

- Why is Bitcoin Core called a "Reference Implementation"? What other implementations of Bitcoin are out there? Is it preferable to have many implementations of Bitcoin?
- What are BIPs (Bitcoin Improvement Proposals)? What are their role in the Bitcoin development process?
- What are the few major configuration options in Bitcoin Core? As a home node operator, which one do you think is most useful?
- What is `txindex`? When would a node operator use this configuration flag? What are the overheads of turning this configuration on?
- What is `bitcoin-cli`? What is it used for? Have you explored any `bitcoin-cli` commands? Which commands do you find most useful as a home node operator?
- What is the approximate disk space requirement for running Bitcoin Core? What are the approximate network bandwidth and memory requirements? Do you think it's "cheap" to run a node?
- What are commands you would use sequentially to get the fully deserialized coinbase transaction of the Block 100, using `bitcoin-cli`?
- How can you verify the signatures of download binaries of Bitcoin Core? What are the potential damages of running a malicious version of the software?


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

### Transaction Structure

- What are the different components of a Bitcoin transaction?

- What parts of the transaction structure got affected with the segwit upgrade? Were there any new fields added to the transaction structure?

- What is a coinbase transaction, how are they created, and why are they important?

- Compare a coinbase transaction to a normal bitcoin transaction and highlight the differences between the two.

- What are UTXOs (Unspent Transaction Outputs), and how is the balance of a wallet calculated?

- Explain transaction weight and virtual bytes? How are they calculated?

- What is witness marker and witness flag? How is it necessary?

- What is nSequence? What was it intented use when Satoshi created Bitcoin? How is it used today?

- What are various sources of transaction malleability? How does segwit fix transaction malleability?

- Can two transactions have the same transaction id? What happens to the UTXOs in those two transactions in that case?

- How is legacy serialization different from serialization after segwit upgrade? Highlight key differences.

- What are transaction inputs, and how are they constructed? What are unlocking scripts?

--------------
fil
# Week 4

## Chapter 7: Authorization and Authentication

- Is the Turing incompleteness of Bitcoin's scripting language (SCRIPT) a feature or a deficiency?

- What is the difference between a locking script (scriptPubKey) and an unlocking script (scriptSig)? What is the difference between a redeem script and a witness script?

- Why are the locking and unlocking scripts executed separately?

- Explain different types of timelocks which you can have and list the components of the transactions that can be used to set timelocks.

- What are the different ways to create contracts in the script? Briefly highlight pros and cons of each.

- Why is the public key directly included in a P2TR output whereas in other script types we always include a hash?

- Why is the Merkle path length limited to 128?

- How does Taproot upgrade increase security and privacy in Bitcoin?

- Highlight the differences between Tapscript and native Bitcoin script?


## Chapter 8: Digital Signature

- What are sighashes, and what are their uses? How many types of sighashes are there?

- What are digital signatures, where are they placed in a transaction, and what is their purpose?

- Describe some real-life exploits that occurred due to poor randomness in digital signatures.

- Besides signing transactions, what other uses could digital signatures have?

- How does batch verification works in Schnorr signatures?

- What are the difference in serialisation of Schnorr signatures and ECDSA signatures?

- What is the quadratic sighash problem? How does segwit's new signing algorithm addresses it?

- What is the Discrete Log Problem, and why is it important in Cryptography? What does it mean when we say "DLP is hard"? What would have happened if DLP wasn't a "hard" problem?

- Why is it important to use a random number (k) as the basis for a private/public nonce pair? What vulnerabilities can be exploited if k is known to be reused? Can you provide a real-life example of when such an exploit occurred?

- How are ECDSA signature malleable? Does this malleability also occur in Schnorr signatures? Is there a way to fix this malleability?

- Explain the key difference between scriptless multisignature and scriptless threshhold signatures. Are they both possible in Bitcoin? If yes, then briefly discuss the different protocols for the same.

--------------

# Week 5

## Chapter 9: Transaction Fess

- Why do we need to pay transaction fees when we have block reward as an incentive? Is there a minimum fee that every transaction needs to pay? Is it a consensus rule or policy rule?

- What are the different fee estimation algorithms? Briefly discuss the internal workings of each.

- What are the RBF rules for fee-bumping a transaction? Which rules are important to protect against DoS attacks?

- What is transaction pinning? How is it a vulnerability for multiparty time-sensitive protocols such as LN?

- What is fee sniping and how does it work? How can it be prevented?

- Explain CPFP carve out and anchor outputs.

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
- What is a Merkle Tree and what significance does it have in the Blockchain?
- What is a design flaw in the Merkle Tree used in Bitcoin?
- What is a Light Client in context to Bitcoin? How do Light Clients verify transactions associated to their addresses?
- Explain mainnet and testnet in brief. Can testned coins have value?
- Explain signet and regtest in brief. When would you use regtest for testing, and when Signet?


## Chapter 12: Mining and Consensus

- What are the goals of Bitcoin mining and what are the incentives for the miners?
- Explain in brief how does the Bitcoin network attain emergent decentralised consensus.
- What is a coin-base transaction? What prevents the miners from inflating the coin-base reward?
- What is Mining Difficulty? Why and how is it adjusted?
- Explain the 51% attack. Can it compromise the security of private keys and signing algorithms?
- What factors could cause a change in Bitcoin’s consensus rules? How is a change in consensus rules achieved in a decentralised network like Bitcoin?
- Define a Hard fork and explain whether a new software implementation of the consensus rules is a pre-requisite for it.
- Explain a soft fork. What are some common criticisms of a soft fork?

--------------

# Week 7

## Chapter 13: Bitcoin Security

- Why does the author say securing bitcoins is like securing cash or a chunk of precious metal? 
- What could be the consequences of applying centralised security models to a decentralised network like Bitcoin?
- Explain the concept of root of trust in security models. What should be the root of trust for Bitcoin            applications?
- How is physical storage of Bitcoin keys one of the most effective methods of securing bitcoins?
- How do hardware signing devices secure bitcoins?
- What could be the consequences of using unnecessarily complex techniques to secure bitcoins?
- What is the importance of using diverse storing mechanisms for bitcoin?
- What is a multi-sig address? In what situation is it advisable to share confidential information about your      bitcoin keys with a trusted person?

## Chapter 14: Second-Layer Applications


--------------

- Mention and explain three primitives that Bitcoin guarantees for applications built on top of it.
- Explain at least two use-cases of applications build on top of Bitcoin.
- What are payment channels in context to Bitcoin? How do they facilitate extremely high transaction throughput?
- Explain what are funding and commitment transactions in context of payment channels.
- What is a uni-directional payment channel? Give an example.
- What is a bi-directional payment channel? Give an example.
- Can a Bitcoin transaction be cancelled? Explain asymmetric revocable transactions.
- What is a HTLC? Which OP-code is used to achieve it in context to payment channels?
