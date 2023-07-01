# Creating a Token

This is a Solidity smart contract that implements a basic token contract called MyToken. The contract allows for the creation and destruction of tokens, as well as tracking the balances of different addresses.

## Description

This is a Solidity smart contract that implements a basic token contract called MyToken. The contract allows for the creation and destruction of tokens, as well as tracking the balances of different addresses.

Features:

Token Details: The contract includes public variables to store the details about the token, such as the token name, token abbreviation, and the total token supply.

Balances Mapping: The contract maintains a mapping of addresses to their token balances. Each address can have a specific amount of tokens associated with it.

Mint Function: The contract includes a mint function that increases the total token supply and the balance of a specific address. This function takes two parameters: an address and a value, and adds the specified value to the total supply and the balance of the address.

Burn Function: The contract includes a burn function that decreases the total token supply and the balance of a specific address. This function works in the opposite way to the mint function and also takes an address and a value. It deducts the specified value from the total supply and the balance of the address.

Burn Function Validation: The burn function includes conditionals to ensure that the balance of the address is greater than or equal to the amount to be burned.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., mytokens.sol). Copy and paste the following code into the file:

```
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;


contract MyToken {

    // public variables here
string public tokenname = "ADROCX";
string public tokenAbbriv = "ADRX";
uint public totalSupply = 0;

    // mapping variable here
mapping(address => uint) public balances;

    // mint function
function mint (address add, uint val) public {
    totalSupply += val;
    balances[add] += val;
}
    // burn function
function burn (address add, uint val) public {
    if(balances[add] >= val){
        totalSupply -= val;
        balances[add] -= val;
    }
    
}
}
```
To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "mytokens.sol" button.

Click on the "Compile" button to compile the smart contract code. Verify that the compilation is successful without any errors.

In the "Deploy & Run Transactions" panel on the right-hand side of the Remix IDE, select the desired network environment (e.g., JavaScript VM or Injected Web3).

Click on the "Deploy" button to deploy the smart contract.
Once the contract is deployed, you will see the contract's details, including the contract address, in the "Deployed Contracts" section.

Interact with the contract by invoking its functions:

a. Set the token name and abbreviation by accessing the public variables tokenname and tokenAbbriv.

b. Check the initial total token supply by accessing the public variable totalSupply.

c. Mint new tokens by calling the mint function and providing an address and a value as parameters. This function increases the total supply by the specified value and increases the balance of the given address by that amount.

d. Burn tokens by calling the burn function and providing an address and a value as parameters. This function decreases the total supply by the specified value and deducts that value from the balance of the given address. Note that the burn operation will only be executed if the balance of the address is greater than or equal to the amount to be burned.

e. View token balances by accessing the balances mapping and providing an address as the key.

Use the Remix IDE's transaction panel to interact with the contract and observe the changes in state variables and balances.
Monitor the output in the Remix IDE's console to check for any transaction events, errors, or log messages generated during the execution of the contract functions.

## Authors

Aditya Raju

@[ADROCX6105](https://twitter.com/ADROCX6105)

## License

This project is licensed under the MIT License - see the LICENSE.md file for details
