# ATM Web Application

A WebAssembly-based ATM application compiled from C++.

## Overview

This is an interactive ATM simulator written in C++ and compiled to WebAssembly (WASM) for running in web browsers. It includes features for managing savings and checking accounts with transactions like deposits, withdrawals, and transfers.

## Files

- **atm.html** - HTML interface for running the WASM application
- **atm.js** - JavaScript glue code that interfaces with the WASM module
- **atm.wasm** - Compiled WebAssembly binary containing the ATM logic

## How to Run

1. Open `atm.html` in a web browser
2. Interact with the ATM through the browser interface
3. Check the browser console for transaction logs and output

## Features

- Deposit to savings and checking accounts
- Withdraw from savings and checking accounts
- Transfer funds between accounts
- Fake bill detection
- Fee processing on transactions
- Card authentication (requires cards.json)

## Building from Source

To rebuild the WASM files from the C++ source:

```bash
source emsdk/emsdk_env.sh
em++ main.cpp -o atm.html -sALLOW_MEMORY_GROWTH
```

Requires [Emscripten SDK](https://emscripten.org/docs/getting_started/downloads.html) to be installed.
