# Sleep Walker EA MT4

This code represents the Sleep Walker EA MT4, developed by the Forex Robot Easy Team. This EA is a powerful forex software designed for a scalping strategy. For detailed reviews and trading results of this product, you can visit [forexroboteasy.com](https://forexroboteasy.com/forex-robot-review/sleep-walker-ea-mt4-review-powerful-forex-software-for-scalping-strategy/). Please note that ForexRobotEasy is not the official developer of this product. We are only providing a sample code that can work as described in this product. To find the official developer of this product, please refer to MQL5.

## Code Explanation
### Input Parameters
- `LotSize`: Determines the lot size for trading.
- `StopLoss`: Sets the stop loss in pips.
- `TakeProfit`: Sets the take profit in pips.

### Global Variables
- `startTime`: Stores the start time for trading.
- `endTime`: Stores the end time for trading.

### Trade Management Parameters
- `magicNumber`: Identifies trades using a magic number.
- `slippage`: Specifies the maximum allowed slippage in pips.

## Expert Functions
### OnInit()
The initialization function sets the trading hours by assigning values to `startTime` and `endTime`.

### OnDeinit(const int reason)
The deinitialization function is used for any necessary cleanup after the expert advisor is removed or stopped.

### OnTick()
This function is called on every tick and checks if the current time is within the specified trading hours. If it is, the function checks if the current symbol is either GBPUSD or EURUSD. If the conditions are met, it generates an entry point using the `GenerateEntryPoint()` function, calculates the stop loss and take profit levels, and places a pending order using `OrderSend()`. The function also checks if the order was successfully placed and prints relevant information or error messages accordingly.

### GenerateEntryPoint()
This function generates entry points based on linked numbers and settings. In the provided code, a placeholder logic is used to calculate the entry point, subtracting 0.001 from the current Ask price. This logic can be replaced with the actual strategy for generating entry points.

### NormalizeDouble(double price, int digits)
This function normalizes a price level to the required number of digits. It rounds the price to the specified number of digits using `MathRound` and `MathPow` functions.

Please note that this code is a sample and may need modifications to fit specific trading strategies or requirements. The actual Sleep Walker EA MT4 may have additional functionalities and features not described in this code sample.
