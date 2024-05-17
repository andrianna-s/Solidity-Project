# Creating a Token in Solidity Project

This Solidity program allows creation, management and destruction of tokens.

## Description

This Solidity smart contract is a simple project for creating a token. It includes a mint function for creating new tokens, a burn function for destroying tokens.

## Getting Started

### Installing

* Download a Solidity compiler or use online compiler Remix Ethereum IDE: https://remix.ethereum.org/

### Executing program
* To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.
* Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension. Copy and paste the following code into the file:
```
// SPDX-License-Identifier: MIT
pragma solidity 0.8.25;

contract MyToken {

    // public variables here
     string public tokenName = "Token";
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
      if (balances[_address] >= _value) {
         totalSupply -= _value; 
         balances[_address] -= _value;
      }
    }  
   }  ```




## Authors

Andrianna R. Sabarillo  
422000869@ntc.edu.ph


