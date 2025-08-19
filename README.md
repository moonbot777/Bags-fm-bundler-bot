# Bags.fm Bundler Bot

A high-performance Solana trading bot designed for bags.fm that bundles multiple transactions for efficient execution using Jito MEV protection.

## 🚀 Features

- **Transaction Bundling**: Bundle multiple buy/sell transactions for optimal execution
- **Jito MEV Protection**: Uses Jito block engine for MEV protection and faster execution
- **Address Lookup Tables**: Optimizes transaction size and gas costs
- **Multi-wallet Support**: Distribute funds across multiple wallets for trading
- **Automated Trading**: Execute trades with configurable parameters
- **Raydium Integration**: Built on Raydium SDK for DEX trading

## 📋 Prerequisites

- Node.js 18+ 
- Solana CLI tools
- A Solana wallet with SOL for transactions
- RPC endpoint (Helius, QuickNode, etc.)

## 🛠️ Installation

1. Clone the repository:
```bash
git clone https://github.com/moonbot777/Bags-fm-bundler-bot.git
cd Bags-fm-bundler-bot
```

2. Install dependencies:
```bash
yarn install
# or
npm install
```

3. Create a `.env` file with your configuration:
```env
PRIVATE_KEY=your_wallet_private_key
RPC_ENDPOINT=your_rpc_endpoint
RPC_WEBSOCKET_ENDPOINT=your_websocket_endpoint
DISTRIBUTE_WALLET_NUM=4
BACKEND_URL=your_backend_url
SLIPPAGE=0.01
```

## 🚀 Usage

### Basic Usage

Start the main bot:
```bash
yarn start
```

### Other Commands

- **Gather**: `yarn gather`
- **Close LUT**: `yarn closeLut`
- **Close WSOL**: `yarn closeWsol`

## 🔧 Configuration

The bot can be configured through environment variables:

- `PRIVATE_KEY`: Your wallet's private key
- `RPC_ENDPOINT`: Solana RPC endpoint
- `RPC_WEBSOCKET_ENDPOINT`: WebSocket endpoint for real-time updates
- `DISTRIBUTE_WALLET_NUM`: Number of wallets to distribute funds to
- `SLIPPAGE`: Trading slippage tolerance (default: 1%)

## 📁 Project Structure

```
├── src/                    # Core trading logic
│   ├── buy.ts             # Buy transaction creation
│   ├── createAta.ts       # Associated token account creation
│   ├── distribute.ts      # SOL distribution logic
│   ├── LUT.ts            # Address lookup table management
│   └── token.ts          # Token creation and management
├── executor/              # Transaction execution
│   ├── jitoWithAxios.ts  # Jito MEV protection
│   └── legacy.ts         # Legacy execution method
├── constants/             # Configuration constants
├── utils/                 # Utility functions
└── index.ts              # Main entry point
```

## 🔒 Security

- Never share your private keys
- Use environment variables for sensitive data
- Test on devnet before mainnet
- Monitor transaction logs carefully

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📞 Support

- **GitHub**: [@moonbot777](https://github.com/moonbot777)
- **Twitter**: [@greenfoxworld](https://twitter.com/greenfoxworld)
- **Telegram**: [@greenfoxfun](https://t.me/greenfoxfun)

## ⚠️ Disclaimer

This software is for educational purposes only. Use at your own risk. The authors are not responsible for any financial losses incurred from using this bot.

## 📄 License

This project is licensed under the MIT License.