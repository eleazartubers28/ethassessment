# MY TOKEN ETH SOLIDITY

This Solidity program will show how mint, burn and totalSupply in the NFT Token. It can help the other people to have knowledge about it. 

## Description

Solidity an object-oriented programming language created specifically by the Ethereum Network team for constructing and designing smart contracts on Blockchain platforms.

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
