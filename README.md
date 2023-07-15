# BEGINNER PROJECT

This program is basically a program that i have done in my assesment of getting started with ssolidity. In this program we have created a contract in that we use different variables, if statement, etc.

## Description

This program is regarding creating contracts and use their different functianlity.In this program we have created two functions one is for mint that mints our tokens and another is for burn that burnsour tokens.We have also created a if statement that will judge whether we have enough tokens to burn or not.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., HelloWorld.sol). Copy and paste the following code into the file:

```javascript
pragma solidity 0.8.18;

/*
       REQUIREMENTS
    1. Your contract will have public variables that store the details about your coin (Token Name, Token Abbrv., Total Supply)
    2. Your contract will have a mapping of addresses to balances (address => uint)
    3. You will have a mint function that takes two parameters: an address and a value. 
       The function then increases the total supply by that number and increases the balance 
       of the “sender” address by that amount
    4. Your contract will have a burn function, which works the opposite of the mint function, as it will destroy tokens. 
       It will take an address and value just like the mint functions. It will then deduct the value from the total supply 
       and from the balance of the “sender”.
    5. Lastly, your burn function should have conditionals to make sure the balance of "sender" is greater than or equal 
       to the amount that is supposed to be burned.
*/

contract MyToken {

    // public variables here

  string public tokname = "SUDHANSHU";
  string public tabbv = "SDH";
  uint public tsupply = 0;

    // mapping variable here
  mapping(address => uint) public balances;
       
    // mint function
  function mint (address add, uint val) public {
      tsupply += val;
      balances[add] += val;
    }
    // burn function
  function burn (address add, uint val) public {
     if (balances[add]>= val) { 
      tsupply -= val;
      balances[add] -= val;
     }    
    }
}

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "Compile HelloWorld.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the mint function where we can provide address and mint some token also we can burn our tokens doing the same. Also we can view balance in this by clicking on viw balance button and providing the address.

## Authors

Sudhanshu Shekhar 
[@sudhanshu5788]

