# TRON Contract Caller

[English](README.md) | [中文](README_zh.md)

---

### Introduction
A lightweight, single-file HTML tool for interacting with TRON smart contracts. It supports reading contract state via TronGrid HTTP API (no wallet required) and writing state via TronLink wallet.

### Features
*   **Single File**: No build process required, just open `tron-contract-caller.html` in your browser.
*   **Dual Mode**:
    *   **Read-Only**: Uses TronGrid HTTP API to query contract state without connecting a wallet.
    *   **Write**: Connects to TronLink wallet to sign and send transactions.
*   **Multi-Network Support**: Built-in support for Mainnet, Shasta Testnet, and Nile Testnet.
*   **Auto-Parsing**: Automatically parses ABI JSON and generates a user-friendly interface for all functions.
*   **Internationalization**: Supports English and Chinese languages.

### Usage
1.  **Start Local Server (Recommended)**:
    ```bash
    # Navigate to the project directory
    cd tron-contract-interaction
    # Start the server
    python3 -m http.server 8000
    ```
    Then open [http://localhost:8000/tron-contract-caller.html](http://localhost:8000/tron-contract-caller.html) in your browser.
    *(Alternatively, you can simply double-click `tron-contract-caller.html` to open it directly)*
2.  **Select Network**: Choose the network where your contract is deployed (Mainnet, Shasta, or Nile).
3.  **Load Contract**:
    *   Enter the Contract Address (starting with T).
    *   Paste the Contract ABI JSON.
    *   Click "Load Contract".
4.  **Interact**:
    *   **Read Functions**: Click "Query" to fetch data. No wallet connection needed.
    *   **Write Functions**: Click "Connect TronLink" first, then enter parameters and click "Send" to trigger a transaction.

### Requirements
*   A modern web browser (Chrome, Edge, Firefox, etc.).
*   [TronLink](https://www.tronlink.org/) browser extension (required for write operations).

### License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

