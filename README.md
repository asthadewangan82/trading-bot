# Binance Futures Testnet Trading Bot

## 📌 Overview

This project is a Python-based CLI trading bot that interacts with Binance Futures Testnet (USDT-M) to place orders. It is designed with a clean structure, input validation, logging, and error handling.

---

## 🚀 Features

* Place Market Orders
* Place Limit Orders
* Supports BUY and SELL operations
* Command-line interface using argparse
* Input validation for order parameters
* Structured logging of API activity
* Exception handling for robustness

---

## 📁 Project Structure

```
trading_bot/
│
├── cli.py
├── requirements.txt
├── README.md
│
├── bot/
│   ├── client.py
│   ├── orders.py
│   ├── validators.py
│   ├── logging_config.py
│   └── __init__.py
│
└── logs/
    └── bot.log
```

---

## ⚙️ Setup Instructions

### 1. Clone the repository

```
git clone <repository_url>
cd trading_bot
```

---

### 2. Create and activate virtual environment

```
python -m venv venv
venv\Scripts\activate
```

---

### 3. Install dependencies

```
pip install -r requirements.txt
```

---

### 4. Configure environment variables

Create a `.env` file in the root directory and add your API credentials:

```
BINANCE_API_KEY=your_api_key
BINANCE_API_SECRET=your_api_secret
BASE_URL=https://testnet.binancefuture.com
```

---

## ▶️ Usage

### Market Order

```
python cli.py --symbol BTCUSDT --side BUY --type MARKET --quantity 0.001
```

---

### Limit Order

```
python cli.py --symbol BTCUSDT --side SELL --type LIMIT --quantity 0.001 --price 75000
```

---

## 🧾 Sample Output

```
=== ORDER REQUEST ===
{'symbol': 'BTCUSDT', 'side': 'BUY', 'type': 'MARKET', 'quantity': 0.001}

=== ORDER RESPONSE ===
{'orderId': 12345678, 'status': 'NEW', 'executedQty': '0.0000', 'avgPrice': '0.00'}
```

---

## 📊 Logging

Application logs are stored in:

```
logs/bot.log
```

---

## ⚠️ Assumptions

* Uses Binance Futures Testnet (USDT-M)
* Supports basic order types (Market and Limit)
* CLI-based execution

