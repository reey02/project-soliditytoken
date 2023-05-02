# Project Solidity Token

Tokens are used for a variety of purposes such as fundraising, creating loyalty programs, or even as a form of currency.The purpose of this program is to help you learn how to create a digital asset called a token on the Ethereum blockchain using a programming language called Solidity. 

## Description

The project will cover the basics of writing a Solidity contract, including how to define variables and functions, how to use mappings to keep track of data, and how to implement a minting and burning function for the token. We'll also discuss some best practices for writing secure and efficient smart contracts.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., myToken.sol). Copy and paste the following code into the file:

```
pragma solidity 0.8.18;

contract MyToken {

    // public variables here
    string public tokenName = "TOKEN";
    string public tokenAbbrv = "TKN";
    uint public totalSupply = 0;

    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint (address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }
    // burn function
     function burn (address _address, uint _value) public {
        if (balances[_address] >= _value){
        totalSupply -= _value;
        balances[_address] -= _value;
        }
    }

}

```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile myToken.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, You can explore it like a wallet , you can mint or burn and thats it!


By the end of this project, you'll have a good understanding of how to write a basic token contract in Solidity and how to deploy it to the Ethereum blockchain. You'll also be familiar with some of the tools and resources available to help you develop and test your contracts. Whether you're interested in creating tokens for your own projects or exploring the world of smart contracts, this project is a great place to start.

## Authors

reey02 >>
https://github.com/reey02


## License

This project is licensed under the MIT License - see the LICENSE.md file for details
