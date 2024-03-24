# TradingView-Indicator-scripts

TradingView Indicators written in Pine Script. 

See my TradingView Profile to see some of these indicators in action: https://www.tradingview.com/u/EightBallDuVal/#published-scripts

## Price Outpaces Moving Average Buy/Sell Indicator:
![image](https://github.com/8BallDuVal/TradingView-Indicator-scripts/assets/39527881/dc29405b-980f-4deb-af4e-670d68e0c2fa)

### Details
- With inputs for the moving average, Bullish overshoot percentage, and bearish overshoot percentage, this indicator is attempting to show market tops based on the difference between the current price of an asset and how far away it is from its moving average.
- If you have the bullish overshoot percentage set to 1.5:
  - let's say price is currently at 20,000 and the moving average is around 6500.
  - The script calculates 20,000/6500 = 3.07
- Then, there is a boolean comparison asking if 3.07 > 1.5.
  - Since it is, the script will create a "SHORT" flag above that candlestick.
- A similar process happens for the "LONG" flags.


## Moving Average Buy/Sell Indicator
![image](https://github.com/8BallDuVal/TradingView-Indicator-scripts/assets/39527881/81a9e516-1496-4c93-a272-e5ca545877ef)

### Details
Using a selected Exponential Moving Average (EMA)/Simple Moving Average (SMA) range, this indicator inserts a Long/Short (buy/sell) indicator overlaid on chart depending on the following conditions:
- LONG/BUY SIGNAL = if SMA value is less than EMA, and both the SMA and EMA are less than the current average price.
- SHORT/SELL SIGNAL = if SMA value is greater than EMA, and both the SMA and EMA are greater than the current average price.

**NOTE: Intended for use with the 21 and 34 weekly moving average time range. Much more useful for long-term analysis rather than short-term analysis.**
