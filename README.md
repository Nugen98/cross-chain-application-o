Cross-Chain Token Swap Mechanism
The architecture follows a two-step process:

Ethereum Side: A smart contract deployed on Ethereum locks the user’s tokens when a swap is initiated. Once the tokens are locked, the contract emits an event that is picked up by an oracle/bridge service, notifying Cosmos about the locked tokens.

Cosmos Side: The bridge communicates with the Cosmos blockchain via the IBC protocol to transfer or mint the equivalent tokens on Cosmos. If the process on Cosmos is successful, the Ethereum contract unlocks the tokens for the recipient.
