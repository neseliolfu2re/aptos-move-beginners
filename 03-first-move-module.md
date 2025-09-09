# 03 – Your First Move Module

In this chapter, you will write and deploy your **first Move smart contract** on the Aptos Testnet.

---

## 1️⃣ Create a New Module
1. Open a terminal and create a folder for your project:
```bash
mkdir my_first_move
cd my_first_move


Initialize a new Move package:

aptos move init --name MyFirstMove

2️⃣ Write Your First Module

Open sources/MyFirstMove.move in a text editor.

Paste the following simple module:

module MyFirstMove::Hello {
    public fun say_hello() {
        // Print a message
        debug::print("Hello, Aptos Move!");
    }
}

3️⃣ Compile Your Module
aptos move compile


This will check for errors and build your module.

4️⃣ Deploy to Testnet

Make sure you have a funded testnet account from Aptos Faucet
.

Deploy your module:

aptos move publish --package-dir . --profile default

5️⃣ Call Your Function
aptos move run --function-id MyFirstMove::Hello::say_hello --profile default


You should see Hello, Aptos Move! in the transaction logs.

✅ Next Steps

Experiment with struct and resource in Move

Try creating simple token modules

Explore more examples: Aptos Examples
