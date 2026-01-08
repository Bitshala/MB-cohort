# Week 1
## GD Questions
1. What were the major problems of Digital Currencies before Bitcoin? How did Bitcoin
solve them?
2. Do you think it would be better if bitcoin transactions were reversible? What are the
potential benefits and drawbacks?
3. What is the Bitcoin Issuance Rate? How do we know the supply cap of Bitcoin is 21 million?
4. Is Bitcoin private? Does Bitcoin need to be private? Why isn't Bitcoin fungible?
5. What is a transaction fee? How is it calculated? What's the effect of transaction fee on transaction confirmation?
6. What are change addresses? When are change addresses required? What happens if the user (or wallet software) forgets to include the change address in a transaction? When will we not require a change address?
7. What does it mean by a transaction to be "confirmed"? How many confirmation is usually acceptable? Is it okay to accept unconfirmed transactions? Why or why not?
8. Why did Satoshi said transactions are "chain of digital signatures"? What is a UTXO? Whats the difference between UTXO and Account based model? Why did Bitcoin choose to stick with UTXO model?

## Bonus Questions
1. Do you believe Bitcoin needs to compete with Visa/MasterCard to succeed? Why or why
not?
2. What are the two main components of a Transaction? What does each component
include?
3. What is the lowest denomination of Bitcoin? Can we run out of decimals to denominate
the smallest unit, as Bitcoin adoption increases?

--------------
# Week 2
## GD Questions

1. Why is Bitcoin Core called a "Reference Implementation"? What other implementations of Bitcoin are out there? Is it preferable to have many implementations of Bitcoin?
2. What are BIPs (Bitcoin Improvement Proposals)? What are their role in the Bitcoin development process?
3. What is bitcoin-cli? What is it used for? Have you explored any bitcoin-cli commands? Which commands do you find most useful as a home node operator?
4. Describe the functions of ‘private keys’, ‘public keys’, ‘Bitcoin addresses’, and ‘digital signatures’. What is the mathematical relationship between them and how are they used in Bitcoin?
5. What is the discrete logarithm problem, and why is it considered hard to solve?
6. What is asymmetry in cryptography, and why are one-way functions useful? Identify a one-way cryptographic function used in deriving public keys from private keys.
7. Describe instances where private keys have been compromised due to lack of entropy. Why is it important to use a cryptographically secure pseudorandom number generator to produce a private key? What are some techniques of generating pseudo random numbers?
8. What are the different kinds of Bitcoin addresses? Explain the differences between P2PKH and P2SH.
9. What is the difference between a hot wallet and cold storage?
10. What is bech32? How is it better than base58? Are there any problems in bech32? How are they solved?

## Bonus Questions
1. What is the approximate disk space requirement for running Bitcoin Core? What are the approximate network bandwidth and memory requirements? Do you think it's "cheap" to run a node?
2. How can you verify the signatures of download binaries of Bitcoin Core? What are the potential damages of running a malicious version of the software?
3. What hash functions are used in the generation of Bitcoin addresses?

--------------

# Week 3
## GD Questions
1. What is a Bitcoin wallet? What are the different types of wallets available?
2. What is the difference between deterministic and non-deterministic wallets?
3. What is a "seed" in the context of Bitcoin wallets? How are mnemonic words generated from the seed?
4. What is the optional passphrase for a mnemonic? In which situations passphrase can be useful?
5. What are the components of an extended key (XPub)? What is the fingerprint of a key?
6. What are hardened and non-hardened derivations? What are the advantages of having different types of derivations?
7. What are the different components of a Bitcoin transaction? What are transaction inputs and outputs, and how are they constructed? What are locking and unlocking scripts?
8. What are various sources of transaction malleability? How does segwit fix transaction malleability? What parts of the transaction structure got affected with the segwit upgrade?

## Bonus Questions
1. What is nSequence? What was it intended use when Satoshi created Bitcoin? How is it used today?
2. What are various sources of transaction malleability? How does segwit fix transaction malleability?
3. Can two transactions have the same transaction id? When can this happen? Is that a consensus violation?
--------------

# Week 4
## GD Questions
1. Is the Turing incompleteness of Bitcoin's scripting language (SCRIPT) a feature or a deficiency?
2. Explain different types of timelocks available in a Bitcoin transaction and list the components of the transactions that can be used to set these timelocks.
3. How does Taproot upgrade increase security and privacy in Bitcoin?
4. Highlight the differences between Tapscript and native Bitcoin script?
5. What are digital signatures, where are they placed in a transaction, and what is their purpose?
6. What are sighashes, and what are their uses? How many types of sighashes are there?
7. What is the Discrete Log Problem, and why is it important in Cryptography? What does it mean when we say "DLP is hard"? What would have happened if DLP wasn't a "hard" problem?
8. Why is it important to use a random number (k) as the basis for a private/public nonce pair? What vulnerabilities can be exploited if k is known to be reused? Can you provide a real-life example of when such an exploit occurred?

## Bonus Questions
1. Why is the public key directly included in a P2TR output whereas in other script types we always include a hash?
2. Why are the locking and unlocking scripts executed separately?
3. Besides signing transactions, what other uses could digital signatures have?


--------------

# Week 5
## GD Questions
1. Why do we need to pay transaction fees when we have block reward as an incentive? Is there a minimum fee that every transaction needs to pay? Is it a consensus rule or policy rule?
2. What is RBF. When is it useful? List all the conditions required to do a valid RBF.
3. What is CPFP (Child Pays For Parents)? When is it useful? In which situation RBF cannot be used, but CPFP can be used?
4. What is transaction pinning? How is it a vulnerability for multiparty time-sensitive protocols such as LN?
5. What is a peer-to-peer network? Give two examples of successful peer-to-peer networks that preceded Bitcoin.
6. Explain in brief what is a Mempool and what is an Orphan Pool.
7. How do light clients validate that a transaction exists? How is this different from the mechanism full archival nodes use to validate a transaction?
8. What are compact block filters? What data should be included in a block filter?

## Bonus Questions
1. What are the privacy trade-offs in using a light client?
2. What is fee sniping and how does it work? How can it be prevented?
3. What is CPFP carve out and anchor outputs?

--------------

# Week 6
## GD Questions
1. Describe the structure of a block and what data does a block header contain?
2. What is a Merkle Tree? How is it used in the blockchain? What data does the Merkle Root verifies?
3. What is the difference between mainnet and testnet? Can testnet coins have value?
4. What is the difference between signet and testnet? What is regtest? When is it useful?
5. What is a coinbase transaction? What prevents the miners from inflating the coinbase reward?
6. Explain the 51% attack. Can it compromise the security of private keys and signing algorithms?
7. What is Mining Difficulty? How is it adjusted? What would happen if it wasn't adjusted?
8. What is the difference between Hard Fork and Soft Fork? Is it possible to do hard fork of Bitcoin, without creating a new coin/network, at current stage of the market? 

## Bonus Questions
 1. How are soft forks are activated in Bitcoin? What was the last soft fork that happened?
 2. What is "Rough Consensus"? How does it affect Bitcoin's development?
 3. When was the last Bitcoin hardfork? What caused it?  

--------------

# Week 7
## GD Questions
1. Why does the author say securing bitcoins is like securing cash or a chunk of precious metal? 
2. What could be the consequences of applying centralised security models to a decentralised network like Bitcoin?
3. Explain the concept of root of trust in security models. What should be the root of trust for Bitcoin applications?
4. Why are hardware siging devices the most recommended way of storing Bitcoin?
5. What are payment channels in context to Bitcoin? How do they facilitate extremely high transaction throughput?
6. Can a Bitcoin transaction be cancelled? Explain asymmetric revocable transactions.
7. What is a HTLC? Which OP-code is used to achieve it in context to payment channels?
8. Explain what are funding and commitment transactions in context of payment channels.

## Bonus Questions
1. What could be the consequences of using unnecessarily complex techniques to secure bitcoins?
2. Explain at least two use-cases of applications build on top of Bitcoin.
3. Can a Bitcoin transaction be cancelled? Explain asymmetric revocable transactions.


