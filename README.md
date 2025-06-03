# WalletGen – Your Powerful Crypto Wallet Solution for Secure Asset Management and Recovery

**WalletGen** is a cutting-edge, open-source **crypto wallet** tool designed for both secure asset management and the potential recovery of lost digital currencies. It empowers users to generate, search, and recover lost or inactive **Bitcoin (BTC)**, **Ethereum (ETH)**, **BNB**, **Polygon (MATIC)**, and other **EVM-compatible wallets** with real-time balance verification and a high-performance C++ engine.

<!--
Meta description:
WalletGen is a high-speed, open-source crypto wallet tool that enables secure management, brute-force recovery, and balance finding for Bitcoin, Ethereum, and other leading cryptocurrencies.  Enhance your crypto security.
-->

## Quick Navigation
- [How It Works](#how-it-works)
- [Why WalletGen](#why-walletgen)
- [Features](#features)
- [Download WalletGen](#how-to-start)
- [Database Download](#download-and-use-database-for-more-speed)
- [The Program Found a Wallet - What Next?](#the-program-found-a-wallet--whats-next)
- [Recovery Your Bitcoin Wallet](#recovery-your-bitcoin-wallet)
- [My Finds](#my-finds)
- [FAQ](#-frequently-asked-questions-faq)
- [Build Instructions](#building-the-project)
- [Donate](#donate)

[![platform](https://img.shields.io/badge/platform-Windows%20%7C%20Linux%20%7C%20Android-blue)](https://github.com/tony-dev1/wallets-finder/releases/tag/walletgen)
![build](https://img.shields.io/badge/build-passing-brightgreen)
![discord](https://img.shields.io/badge/discord-tonydevbtc-blue.svg?logo=discord&label=discord)
[![x](https://img.shields.io/badge/@tonydevbtc-black.svg?logo=x)](https://x.com/tonydevbtc)

<p align="center">
    <img width="1000" alt="Crypto Wallet security and recovery" title="WalletGen Crypto Wallet Solution" height="460" src="/upload/status.webp" />
</p>

⚠️ **Disclaimer**: WalletGen is a research and educational tool. It is not intended for unauthorized access or malicious activity. Use it responsibly and only with wallets you own or have permission to access.

## How It Works

WalletGen utilizes industry-standard protocols like [BIP39](https://github.com/bitcoin/bips/blob/master/bip-0039.mediawiki), [BIP44](https://github.com/bitcoin/bips/blob/master/bip-0044.mediawiki), and [Bech32](https://en.bitcoin.it/wiki/Bech32) for generating Bitcoin addresses. For EVM-based chains, like Ethereum, it employs [Keccak256](https://emn178.github.io/online-tools/keccak_256.html) hashing.

The software rapidly generates potential wallet addresses and compares them against a database of known addresses or, alternatively, performs real-time balance checks via public blockchain explorers. 

Wallet Gen is written in C++ and benefits from its open-source nature, allowing users to access and modify the code as needed.  Compared to Python-based alternatives, Wallet Gen offers significantly faster wallet generation, primarily leveraging your CPU & GPU for optimal performance.

##  Why WalletGen?

**WalletGen** is designed with performance in mind. Written in C++ and optimized for multi-threaded CPU and GPU utilization, it delivers performance that can be **up to 10x faster** than many Python-based brute-force tools. Whether you're exploring forgotten wallets, assessing private key spaces, or looking to recover your own wallet, WalletGen enables you to do so efficiently and securely.

## Features

-   **Create Cryptocurrency Wallets:** Wallet Gen makes it easy to create individual wallets for Bitcoin, Ethereum, BNB, MATIC and other cryptocurrencies.
-   **Find Wallets with Balance:** Employing brute-force techniques, Wallet Gen can search for existing wallets that contain balances, on both the Bitcoin network and EVMs.
-   **Support for Diverse Algorithms:** Keccak256 is used for EVM wallets, while BIP39, BIP44, and Bech32 are implemented for Bitcoin wallet generation.
-   **Database Integration for Speed:** Utilize downloadable databases to supercharge your searches for balance-holding wallets, vastly accelerating the process.
-   **High-Performance Operation:** Wallet Gen is engineered to leverage both CPU and GPU power to achieve top-tier performance.
-   **Bitcoin Wallet Recovery:** WalletGen offers functionality to recover your Bitcoin wallet through the seed phrase (mnemonic phrase).

## Supported Blockchains

-   Bitcoin (BTC)
-   Ethereum (ETH)
-   Binance Smart Chain (BNB)
-   Any EVM-compatible chain

# Demo

<p align="center">
    <img width="1000" height="460" alt="Crypto Wallet search demo" title="WalletGen Crypto Wallet Search" src="/upload/pane.webp" />
</p>


<p align="center">
    <img width="1000" height="460" alt="Crypto Wallet Search Demo on Linux" title="WalletGen Crypto Wallet Search on Linux" src="/upload/watermark.webp" />
</p>

# How to start

## Windows 
- Download [Release](../../releases) 
- Unpack anywhere
- Run `WalletGen.exe`

Or Just Download [Installer](../../releases)

## Linux (x86-64bit)

Use wget 
or download [Release for Linux](../../releases) 







## How to Search for Lost Bitcoin & Ethereum Wallets with Balance

**Wallet Gen** supports brute-force searching for two primary types of crypto wallets with existing balances.

### For Bitcoin (BTC) wallets:

*   Press key 3 in the menu, or run start_search_btc.bat to search for Bitcoin wallets via the internet. This approach may be slower, as it involves real-time balance checks through blockchain explorers.
*   Press key 6 to search for Bitcoin wallets using the database. This method provides faster performance by comparing generated wallets against a pre-compiled database of known, balance-containing addresses.

### For EVM wallets (Ethereum, BNB, MATIC, etc.):

*   Press key 5, or execute start_search_evm.bat to search EVM wallets using the internet. This method confirms the presence of balances in real-time through blockchain explorers.
*   Press key 6 to search for EVM wallets using the database. This approach is more efficient because it compares generated wallets against an existing database of addresses known to hold balances.

### Speed Considerations:

*   The speed of the search is significantly influenced by your hardware, especially the graphics card (GPU). To optimize speed and increase the likelihood of finding a wallet with a balance, consider running multiple program instances (1 to 4), dependent on your system's capabilities.

Leveraging the database dramatically enhances search efficiency, eliminating the need to query the blockchain for every wallet generated.

## The Program Found a Wallet — What’s Next?

Upon discovering a wallet with a balance, the program will:
*   **Immediately Stop** the search.
*   **Display** the wallet details on the console.
*   **Save** this information within the ``found_wallets.txt`` file.

### Accessing Your Funds:
1.  Import the **mnemonic seed phrase** from the discovered wallet into a compatible crypto wallet (e.g., Metamask, Trust Wallet, or Electrum).
2.  Following restoration, you can transfer the funds to your wallet.

> If you find a successful match, please consider sharing a small portion of the found balance as a token of appreciation. Thank you!

## Recovery Your Bitcoin Wallet

WalletGen includes functionality to recover your bitcoin wallet using your seed phrase (mnemonic phrase). The software supports entering the complete seed phrase, as well as searching for missing words using specific characters.

### Process Explanation

#### Searching for Missing Words:

If you are missing words or unsure of your seed phrase, substitute those words with *. WalletGen will explore all possible word variations in the * positions to identify the correct seed phrase, and restore the related wallet balance.

#### Entering a Complete Seed Phrase:

If you possess the full 12-word seed phrase, simply enter it with spaces. WalletGen will generate different address types (Legacy, SegWit, P2SH) and confirm their balances.

![recovery](/upload/default.webp)

### Key Recommendations

*   Seed phrases must include exactly 12 words.
*   Utilize only the * symbol to designate missing words.
*   Searching for missing words can be time-intensive, particularly with multiple missing words.
*   Successful wallet recovery with a balance will result in the program automatically halting and saving the discovered information.

## My Finds

![mywallet](/upload/clone.webp)


I've personally recovered two BTC wallets with a balance. The first contained 0.000032 BTC, while the second had 0.0528 BTC (approximately $4800 at the time of discovery).  
Here’s the link to the wallet: [bc1qk3m62hx2hh5mhvc0tj45f9xflzcnu0sur3rvay](https://mempool.space/address/bc1qk3m62hx2hh5mhvc0tj45f9xflzcnu0sur3rvay).

<p align="center">
    <img width="1000" height="460" alt="WalletGen first lost bitcoin wallet found" title="WalletGen first lost bitcoin wallet found" src="/upload/terminal.webp" />
</p>

### New Find 4/9/2025

After a week of continuous wallet searching, I discovered a [wallet](https://mempool.space/address/bc1q29c5m3w4jxtsj4vcd2ccw4t68xm8m7vs5vytu0) with 0.25 bitcoin ($19k). This is my 4th and most valuable discovery to date.

![image](/upload/fresh.webp)

## New Find 5/5/2025

[bc1qpm0k3kcmthwsa4zseh33g3hl7eju8u8nkt83kp](https://mempool.space/address/bc1qpm0k3kcmthwsa4zseh33g3hl7eju8u8nkt83kp)

![image](/upload/component.webp)


## Building the Project

1.  Open the project file (`CryptoWalletGen.sln`) within Visual Studio or any compatible C++ compiler.
2.  Install the necessary dependencies and build the project.

```cmd
> git clone https://github.com/microsoft/vcpkg
> .\vcpkg\bootstrap-vcpkg.bat
> .\vcpkg\vcpkg integrate install
> .\vcpkg\vcpkg install openssl:x64-windows
```

3.  Initiate the project build.

## 🔍 Frequently Asked Questions (FAQ)

### ❓ Where can I download WalletGen?
You can download the WalletGen given on the [release download page](../../releases) 

### ❓ Where can I download a database of known addresses with balance?
You can download the current database given on the [release   page](../../releases) 

### ❓ Can WalletGen help me recover a lost Bitcoin wallet?
Yes. WalletGen leverages brute-force seed generation coupled with a known-address database to assist in the potential **recovery of lost Bitcoin wallets**.

### ❓ Is WalletGen a seed phrase generator?
Yes. WalletGen can generate **BIP39 seed phrases** and derive wallets for Bitcoin, Ethereum, and other EVM chains.

### ❓ Does database searching require an internet connection?
No. Searching using the database operates independently of an internet connection, as wallet balances are already known.

### ❓ Can I find Ethereum wallets with balance?
Yes. WalletGen supports scanning for **Ethereum wallets with balance** through both brute-force and database methods.

### ❓ Is WalletGen legal?
WalletGen is explicitly intended for **educational and research purposes only**. Users should only utilize the tool on wallets they own or have been authorized to access.

## Todo
1. Search for missing words in a seed phrase. - **Done!**

## Contribute

Your input is valued! If you have ideas, encounter any bugs, or wish to improve the codebase, feel free to submit a pull request.

## Donate

As a thank you, consider sending a small contribution if you discover a wallet with a balance. This motivates me to continually enhance and improve the program!

**BTC:** bc1qeyrshy5ntsguwxe9m8tp2x2yqhddz7ymkj44h9

**ETH:** 0x76c2E75B92Eb340f01B378e332FC7d8954893693

## Credits
This project uses code from the [Trezor project](https://github.com/trezor/trezor-crypto). The code is licensed under the MIT License.

## License
This project is licensed under the [MIT License](/LICENSE)