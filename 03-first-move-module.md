# 03 – Your First Move Module

In this chapter, you will write and deploy your first Move smart contract on the Aptos Testnet.

## 1. Create a New Project
Open a terminal and run:
mkdir my_first_move
cd my_first_move
aptos move init --name MyFirstMove
This creates a new Move package named MyFirstMove.

## 2. Write Your First Module
Open sources/MyFirstMove.move in a text editor and paste:
module MyFirstMove::Hello {
    public fun say_hello() {
        debug::print("Hello, Aptos Move!");
    }
}
This module defines a simple function say_hello that prints a message.

## 3. Compile the Module
Run:
aptos move compile
This checks your code for errors and builds the module.

## 4. Deploy to Testnet
Make sure you have testnet tokens from the Aptos Faucet (https://aptos.dev/en/network/faucet).
Deploy your module:
aptos move publish --package-dir . --profile default

## 5. Run the Function
Execute:
aptos move run --function-id MyFirstMove::Hello::say_hello --profile default
You should see: Hello, Aptos Move! in the transaction logs.

## Next Steps
- Experiment with struct and resource in Move
- Try creating simple token modules
- Explore more examples: https://github.com/aptos-labs/aptos-examples
