# ATS Advisor MT5

This is the code for the ATS Advisor MT5, a fully automatic forex software with a loss recovery system. The development team behind this software is Forex Robot Easy Team. For detailed reviews and trading results of this product, you can visit the [Forex Robot Easy](https://forexroboteasy.com/forex-robot-review/review-ats-advisor-mt5-fully-automatic-forex-software-with-loss-recovery-system/) website.

## Input Parameters

- LotSize: Initial lot size for opening trades (default: 0.01)
- MaxLotSize: Maximum lot size allowed (default: 10.0)
- RecoveryFactor: Lot size multiplier for loss recovery (default: 1.5)
- StopLoss: Stop loss level in points (default: 100.0)
- TakeProfit: Take profit level in points (default: 200.0)

## Global Variables

- previousProfit: Stores the previous profit value
- currentLotSize: Stores the current lot size for opening trades

## Initialization Function (OnInit)

The OnInit function is called during the initialization of the expert advisor. In this function, the initial lot size is set to the value specified in the input parameters.

## Start Function (OnTick)

The OnTick function is called on each tick of the market. Here is how the code works:

1. Check for previous profit:
   - If the previous profit is greater than 0, adjust the current lot size based on the previous profit multiplied by the recovery factor. Limit the lot size to the maximum allowed.
   - If the previous profit is less than 0, increase the lot size for loss recovery by multiplying it with the recovery factor.

2. Open a new trade:
   - Use the OrderSend function to open a buy trade with the current lot size, stop loss, and take profit levels.
   - If there is an error opening the buy trade, print the error message.

3. Save the current profit as the previous profit for the next tick.

## Product Description

ATS Advisor MT5 is a fully automatic forex software developed by Forex Robot Easy Team. It is designed to trade on the MetaTrader 5 platform and incorporates a loss recovery system. The expert advisor uses a set of input parameters to determine the lot size, stop loss, and take profit levels for each trade.

The software aims to optimize trading performance by adjusting the lot size based on previous profit and implementing a recovery strategy for losses. It allows traders to set their initial lot size, maximum lot size, and recovery factor according to their risk tolerance and trading preferences.

With the ATS Advisor MT5, traders can automate their trading strategy and take advantage of market opportunities without constantly monitoring the market. The expert advisor is suitable for both beginner and experienced traders who are looking for a reliable and efficient trading solution.

Please note that ForexRobotEasy is not the official developer of this product. We are only showcasing the sample code that can work as described in this product. To find the official developer of ATS Advisor MT5, please refer to MQL5.
