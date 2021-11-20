# PancakeSwap Snipe Front Running Bot
Scan the blockchain and find transactions based on certain criteria (pending on the block aka mempool).
Front-run (specific trade volumes, slippage and gas price) transactions by placing a buy order on the same block at the same time by setting a higher gas price.

Sell immediately in the next block right after at the buy transaction on the front-ran block is completed.
It detects when new liquidity is added to an AMM (automated market maker) pool on PancakeSwap (runs on Binance Smart Chain).

## Prerequisities
- Node and NPM https://nodejs.org/en/download/
- Wallet with BNB for gas and token swap

## Running BOT
- Update env.js and provide private key of your wallet and token address you want to target
- Update bot.js and provide your BSC wallet address
- Bot is preconfigured for Pancakeswap on BSC. Review configuration in constants.js. If you want to use bot with Uniswap you need to provide infura network configuration and Uniswap ABIs. Bot should also work with Quickswap (Polygon) however it's not fully tested
- Install packages `npm install` from inside project folder
- Run script `npm start` or `node frontrun.js`
