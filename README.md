# MY TOKEN ETH

This Solidity program is user input program where the user will add tokens and subtract tokens in which user can also monitor the balances.

## Description

Written in Solidity, a programming language for creating smart contracts for the Ethereum blockchain, this application is a straightforward contract. This program can help the future IT Students to develop even more complex code that can function very well.

## Getting Started

### Executing program

Remix is an online Solidity IDE that you may use to run this application. To get started, go to https://remix.ethereum.org/.

When you are on the Remix website, click the "+" icon in the left sidebar to start a new file. Put a.sol extension to the file, such as HelloWorld.sol. The code below should be copied and pasted into the file:

### Installing

``` ethsolidity
contract MyToken {

    // public variables here
   string public tokenName = "Eleazar";
   string public tokenAbbrv = "Lzr";
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

}

```

## Authors

Jhon Eleazar P. Tuburan
422003221@ntc.edu.ph
