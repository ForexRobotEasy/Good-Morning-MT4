# Good Morning MT4

## Description
Good Morning MT4 is a forex trading expert advisor that uses a combination of candle size, RSI indicator, and price range to determine trade entry points. It is designed to open trades based on specific conditions and manage them accordingly.

This code is provided as a sample and is not the official code developed by Forex Robot Easy Team. It is intended to demonstrate how the Good Morning MT4 expert advisor works and can be used as a reference for understanding the logic behind it.

For detailed reviews and trading results of the official Good Morning MT4 product, please visit [Forex Robot Easy - Good Morning MT4 Review](https://forexroboteasy.com/forex-robot-review/review-good-morning-mt4-a-professional-forex-traders-perspective/). 

To find the official developer of this product and obtain the official code, please refer to the MQL5 platform.

## Input Parameters
- CandleSize: Minimum size of a candle.
- RsiPeriod: Period of the RSI indicator.
- UpperRangePercent: Percentage to determine the upper part of the range.
- LowerRangePercent: Percentage to determine the lower part of the range.

## Global Variables
- ticket: Ticket number of the last opened trade.

## Initialization Function
The OnInit function is called when the expert advisor is initialized. It can be used for any necessary setup or initialization code. In this code, no additional initialization is done.

## Deinitialization Function
The OnDeinit function is called when the expert advisor is being deinitialized. It can be used for any cleanup or deinitialization code. In this code, no additional deinitialization is done.

## Start Function
The OnTick function is the main function of the expert advisor that is called on each tick. It calculates the size of the current candle, the RSI value, and the price range. Based on these values, it determines whether to open a trade.

If the candle size is greater than or equal to the specified CandleSize and the RSI value is greater than or equal to the UpperRangePercent, a buy trade is opened. If the candle size is greater than or equal to the specified CandleSize and the RSI value is less than or equal to the LowerRangePercent, a sell trade is opened.

After opening a trade, it checks if the trade was opened successfully and if the spread is too high. If the spread is high, the trade is closed. 

It also includes a loop to close trades in the order they were opened using the FIFO (First In First Out) principle. It checks if the trade belongs to the same symbol and magic number and closes it accordingly.

## Disclaimer
ForexRobotEasy is not the official developer of Good Morning MT4. The provided code is a sample that demonstrates the functionality of the expert advisor. To obtain the official code and for more information, please refer to the MQL5 platform and the official developer of Good Morning MT4.
