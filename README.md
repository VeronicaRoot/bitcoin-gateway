# ₿ Bitcoin Core & Telegram Payment Gateway

A completely self-hosted, third-party-free Bitcoin payment gateway that connects directly to your own **Bitcoin Core** node. 

This system generates unique SegWit addresses for your customers, tracks incoming payments using an embedded SQLite database, and sends real-time notifications to your **Telegram** account when a payment is detected in the Mempool (0-conf) and when it is fully confirmed.

## 🌟 Features

* **No Middlemen & Zero Fees:** Connects directly to your own Bitcoin Core node via JSON-RPC.
* **Object-Oriented Architecture:** Modular, clean, and highly extensible Python structure.
* **Lightweight Database:** Uses embedded `SQLite3` for persistent invoice tracking (no separate DB server needed).
* **Real-time Telegram Alerts:** 
  * ⏳ Alerts you instantly when a transaction hits the Mempool (0-confirmations).
  * ✅ Alerts you when the payment is included in a block (1+ confirmations).
* **Extensive Logging:** Full terminal logging for monitoring RPC and API traffic.

## ⚠️ Important Security Notice
Before deploying this on **Mainnet**, please test it thoroughly on **Testnet** or **Regtest**. Ensure that your `bitcoin.conf` binds the RPC server strictly to `127.0.0.1` (localhost) so it is not exposed to the public internet.

## 🛠️ Requirements

* A fully synced Bitcoin Core Node (Mainnet or Testnet)
* Python 3.7+
* Telegram Bot API Token (Obtained via BotFather)

## 📦 Installation

1. Clone the repository to your local machine or server:
   ```bash
   git clone https://github.com/YOUR_USERNAME/bitcoin-telegram-gateway.git
   cd bitcoin-telegram-gateway
