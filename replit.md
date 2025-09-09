# Pi Auto Forwarder

## Overview
This is a Python console application that automatically forwards Pi Network cryptocurrency from user wallets to a designated safe wallet. It monitors both available and locked balances, automatically forwarding available Pi while waiting for locked balances to unlock.

**Current Status**: Successfully imported from GitHub and running in Replit environment

## Recent Changes
- **Sept 9, 2025**: GitHub import setup completed
  - Installed Python dependencies via UV package manager (stellar-sdk, bip-utils, requests, mnemonic, PyNaCl)
  - Configured console workflow "Pi Auto Forwarder" for continuous monitoring
  - Set up deployment configuration for VM hosting
  - Application successfully running and awaiting user input

## Project Architecture

### Core Components
- **main.py**: Single-file application containing all functionality
- **Dependencies**: Uses Pi Network's Stellar-based blockchain via stellar-sdk
- **BIP44 Wallet**: Converts mnemonic phrases to Ed25519 keypairs
- **Auto-installer**: Automatically installs required packages on first run

### Key Features
- **Automatic forwarding**: Sends available Pi to safe wallet
- **Locked balance monitoring**: Tracks and waits for locked Pi to unlock
- **Dry run mode**: Safe testing mode (DRY_RUN = True by default)
- **Error handling**: Robust error recovery and retry logic

### Configuration
- **HORIZON_URL**: Pi Network mainnet API endpoint
- **SAFE_WALLET**: Destination wallet address for forwarded Pi
- **DRY_RUN**: Safety flag for testing (set to True by default)

## Deployment Settings
- **Target**: VM (continuous running required for monitoring)
- **Command**: `python main.py`
- **Output**: Console (interactive input required for mnemonic)

## Usage Notes
- Application requires 24-word Pi Network passphrase at startup
- Runs continuously monitoring for available and unlocking Pi balances
- Safe mode enabled by default - change DRY_RUN to False for live transfers
- Designed for long-running background operation