# Token_META
This contract is a basic implementation of a token contract that allows minting and burning of tokens. It is written in Solidity and can be deployed on the Ethereum blockchain.
Contract Details
The contract has the following public variables:

tokenName: A string variable that stores the name of the token.
tokenAbbrv: A string variable that stores the abbreviation or symbol of the token.
totalSupply: An unsigned integer variable that represents the total supply of the token.
Additionally, the contract has a mapping of addresses to balances:

balances: A mapping that associates Ethereum addresses with their corresponding token balances.
Functions
Mint Function
The mint function allows the creation of new tokens. It takes two parameters:

address: The Ethereum address to which the newly created tokens will be assigned.
value: The number of tokens to be minted and assigned to the specified address.
The mint function increases the total supply by the given value and updates the balance of the address accordingly.

Burn Function
The burn function allows the destruction of tokens. It works in the opposite way to the mint function. It takes two parameters:

address: The Ethereum address from which tokens will be burned.
value: The number of tokens to be burned from the specified address.
The burn function deducts the specified value from the total supply and updates the balance of the address accordingly. It also includes conditionals to ensure that the balance of the address is greater than or equal to the amount that is supposed to be burned.
CoinContract contractInstance = CoinContract(address);

// Mint 100 tokens and assign them to the specified address
contractInstance.mint(addressToMint, 100);

CoinContract contractInstance = CoinContract(address);

// Burn 50 tokens from the specified address
contractInstance.burn(addressToBurn, 50);
