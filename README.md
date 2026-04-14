# ROES : Advanced Luau Script Protection & Execution Layer 

ROES  is a high-security, client-server execution framework for Roblox designed to mitigate script theft and "dumping." By utilizing a custom Lua-in-Lua Virtual Machine (VM), ROES ensures that your source code never touches the client’s disk or standard memory space in a readable format.

# 🛡️ Purpose
Standard LocalScripts are easily decompiled by exploiters. ROES changes the game by:

Eliminating Source Visibility: Your code is compiled into bytecode and encrypted server-side.

Memory Obfuscation: The client receives an encrypted payload that is only decrypted and executed within a sandboxed VM environment.

Dynamic Handshaking: Utilizes a secure server-client handshake to prevent unauthorized "fetching" of game logic.

# 🚀 How It Works
Compilation: Source Lua is pre-compiled into Luau bytecode.

Encryption: The bytecode is encrypted using a rotating XOR or AES-256 scheme.

Transmission: A secure RemoteFunction sends the payload to the client upon a successful integrity check.

Execution: A modified Fiu VM instance decrypts and interprets the bytecode in real-time without using loadstring().

# 📂 Project Structure
Server: The "Vault" logic, handling encryption and key rotation.

Client: The "Bootstrapper" and the Fiu VM implementation.

Shared: Common encryption utilities and networking protocols.

Tools: Scripts for local bytecode compilation and mutation.

# 📜 License & Usage
This project is open-source under the MIT License.

Contribution Rules:
Modify: Feel free to modify, optimize, or harden the VM.

Forking: You are free to fork this repository. However, you must include an attribution to "Emmanuel ( Mane ) " in the README or the "About" section of your fork.

Commercial Use: You may use this for your own games or products, provided the original license. YOU CAN NOT SELL or DISTRIBUTE THIS PROJECT for profit. It is open source!

# ⚠️ Disclaimer
While ROES significantly increases the "cost of attack," no client-side security is 100% unhackable. This tool is designed to stop the majority of script dumpers and decompiler tools, but it should be used as one layer of a multi-depth security strategy.

## Yes, this was AI-generated. It can explain things better than I can sometimes.
