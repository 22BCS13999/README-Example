# A Customizable ERC20-like Token Implementation in JavaScript
## Description
This project focuses on the development of a customizable token system inspired by the ERC20 standard, implemented in JavaScript. The aim is to provide a foundational understanding of how digital tokens can be created, managed, and manipulated using simple JavaScript classes and methods. This implementation includes basic functionalities such as minting new tokens, burning existing tokens, and checking token balances for specific addresses.

## Features:

Token Creation: Initialize a new token with a specified name and symbol.
Minting Tokens: Add new tokens to the total supply and update the balance of a specified address.
Burning Tokens: Reduce the total supply of tokens by removing tokens from a specified address.
Balance Inquiry: Check the balance of tokens held by any address.
Error Handling: Ensure proper management of token balances with error handling for insufficient balances during burn operations.


## Key Components:

Token Class: The MyToken class encapsulates the core functionalities of the token system, including methods for minting, burning, and checking balances.
Public Variables: Store the token's name, symbol, and total supply.
Balance Mapping: Utilize a JavaScript Map to keep track of the balances associated with different addresses.
Example Usage: Demonstrate the use of the token system through minting and burning operations, and handle errors gracefully.

## Getting Started
To run and interact with this program, you can use Remix, an online Solidity Integrated Development Environment (IDE). Here are the steps to get started:

## Execution Instructions
Follow these steps to execute and interact with the "A Customizable ERC20-like Token Implementation in JavaScript" project:

Prerequisites
Ensure you have Node.js installed on your machine. You can download it from Node.js official website.
A code editor like Visual Studio Code or any text editor of your choice.

# Step-by-Step Instructions

1.Set Up:

Create a new directory for your project.
Open your terminal or command prompt.
Navigate to your project directory.
Initialize a new Node.js project by running:  npm init -y

2.Create the JavaScript File:

In your project directory, create a new file named MyToken.js.

3.Add the Code:

Copy and paste the provided MyToken class code into the MyToken.js file.

4.Run the Script:

Open your terminal or command prompt.
Navigate to your project directory.
Run the script using Node.js by executing : node MyToken.js

5.Interact with the Contract:

 1. //Method to mint new tokens
    mint(address, value) {
        this.totalSupply += value;
        if (this.balances.has(address)) {
            this.balances.set(address, this.balances.get(address) + value);
        } else {
            this.balances.set(address, value);
        }
    }
2.// Method to burn tokens
    burn(address, value) {
        if (!this.balances.has(address) || this.balances.get(address) < value) {
            throw new Error("Insufficient balance to burn");
        }

        this.totalSupply -= value;
        this.balances.set(address, this.balances.get(address) - value);
    }

6.Check Balances:

=> Enter an address into the balances function and click on the call button to see the balance.

7.View Token Details:

=> Click on the tokenName, tokenAbbrv, and totalSupply buttons to display their values.
    

By following these steps, you'll be able to execute and interact with your token implementation in JavaScript.
   
## Authors

=> Md Bellal Hosssain
Github :https://github.com/22BCS13999
## License

This project is licensed under the MIT License - see the LICENSE.md file for details
