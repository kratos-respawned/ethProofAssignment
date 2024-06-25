# MyToken Project

A simple Ethereum-based token contract.

## Description

MyToken is a basic implementation of an ERC-20-like token contract on the Ethereum blockchain. This contract allows the creation (minting) and destruction (burning) of tokens, managing the token supply and balances of addresses.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., myToken.sol). Copy and paste the following code into the file:

```javascript
pragma solidity ^0.8.18;

contract MyToken {

    // public variables here
    string public tokenName = "nevergonnagiveyouup";
    string public tokenAbbrv = "rickAstley";
    uint public totalSupply = 0;

    // mapping variable here
    mapping (address => uint) public balances; 

    // mint function
    function mint (address Address, uint value) public 
    {
        totalSupply += value;
        balances[Address] += value;
    }

    // burn function
    function burn (address Address, uint value) public
    {
        if (balances[Address]>= value)
        {
            totalSupply -= value;
            balances[Address] -= value;
        }
    }

}

```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile myToken.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the mint and burn functions. Click on the "MyToken" contract in the left-hand sidebar, and then click on the "mint" function. Finally, after adding the address and value, click on the "transact" button to execute the function and click on the "totalSupply" button to get the final value.

## Authors

Gaurav Bhandari                                          
[@sbhandari1907](mailto:sbhandari1907@gmail.com)
