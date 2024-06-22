CustomToken Smart Contract

The CustomToken smart contract is a simple token implementation on the Ethereum blockchain using Solidity. It includes basic functionalities for minting and burning tokens. The token is named "Sumanbhardwaj" with the symbol "SB".

Token Details

Name: Sumanbhardwaj
Symbol: SB
Total Supply: Dynamic (initially 0)
Public Variables

string public coinName: Stores the name of the token.
string public coinSymbol: Stores the symbol of the token.
uint public supplyTotal: Stores the total supply of tokens.
Mappings

mapping(address => uint) public walletBalances: Maps each address to its token balance.
Functions

function createTokens(address recipient, uint amount) public
This function mints new tokens and assigns them to the specified recipient.

Parameters:

address recipient: The address that will receive the newly created tokens.
uint amount: The number of tokens to create.
Behavior:

Increases supplyTotal by amount.
Increases walletBalances[recipient] by amount.
destroyTokens

function destroyTokens(address account, uint amount) public
This function burns a specified amount of tokens from the specified account.

Parameters:

address account: The address from which the tokens will be burned.
uint amount: The number of tokens to burn.
Behavior:

Checks that the account has at least amount tokens.
Decreases supplyTotal by amount.
Decreases walletBalances[account] by amount.
Reverts if:

walletBalances[account] is less than amount.
License

This project is licensed under the MIT License.

Usage Example
Deploying the Contract
Deploy the CustomToken contract to the Ethereum network using a tool like Remix or Truffle.
After deployment, the token name will be "Sumanbhardwaj" and the symbol will be "SB".
Minting Tokens
To mint new tokens, call the createTokens function with the recipient's address and the amount of tokens to create.


customToken.createTokens(0xRecipientAddress, 1000);
This will create 1000 new tokens and assign them to 0xRecipientAddress.

Burning Tokens

To burn tokens, call the destroyTokens function with the account address and the amount of tokens to burn.


customToken.destroyTokens(0xAccountAddress, 500);
This will burn 500 tokens from 0xAccountAddress, reducing the total supply.

Contributing

Feel free to fork this repository and submit pull requests. For major changes, please open an issue first to discuss what you would like to change.

Acknowledgments

This contract is a basic implementation for educational purposes and should not be used in production without proper security audits and enhancements.

This README provides a concise overview of the CustomToken smart contract, its functionalities, and usage.
