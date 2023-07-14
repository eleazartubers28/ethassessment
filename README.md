# MY TOKEN ETH

This Solidity program is user input program where the user will add tokens and subtract tokens in which user can also monitor the balances.

## Description

Written in Solidity, a programming language for creating smart contracts for the Ethereum blockchain, this application is a straightforward contract. This program can help the future IT Students to develop even more complex code that can function very well.

## Getting Started

### Executing program

Remix is an online Solidity IDE that you may use to run this application. To get started, go to https://remix.ethereum.org/.

When you are on the Remix website, click the "+" icon in the left sidebar to start a new file. Put a.sol extension to the file, such as HelloWorld.sol. The code below should be copied and pasted into the file:

### Installing
1. Your contract will have public variables that store the details about your coin (Token Name, Token Abbrv., Total Supply)
2. Your contract will have a mapping of addresses to balances (address => uint)
3. You will have a mint function that takes two parameters: an address and a value. The function then increases the total supply by that number and increases the balance of the “sender” address by that amount
4. Your contract will have a burn function, which works the opposite of the mint function, as it will destroy tokens. It will take an address and value just like the mint functions. It will then deduct the value from the total supply and from the balance of the “sender”.
5. Lastly, your burn function should have conditionals to make sure the balance of "sender" is greater than or equal to the amount that is supposed to be burned.

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

## Authors

Jhon Eleazar P. Tuburan
422003221@ntc.edu.ph
