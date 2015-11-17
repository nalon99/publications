## Three bars reversal revised
A revised version of the three bars reversal pattern is depicted in this folder.
Before digging into it I strongly recommend to look at my previous study of the classic [three bars reversal pattern](http://nalon99.github.io/publications/three_bars/).

Let's assume to have three bars: Bar 1, Bar 2, Bar 3 and the last bar is Bar 3.
The classic three bars reversal batter suggest to enter a long position if:
1. Bar 1 closes down
2. Low of Bar 2 is below low of Bar 1 (and Bar 3)
3. High of Bar 2 is below high of Bar 1
4. Bar 3 closes above the high of both Bar 1 and Bar 2
5. Buy at close of Bar 3
 
I'm going to change the rules 4 and 5 with the followings:
4. Place a BUY STOP order at high of Bar 2 (before the Bar 3 closes)
5. A long position will be entered if and only if Bar 3 reaches the high of Bar 2
 
The main difference is that we don't need to wait for the close of the Bar 3, if the Bar 3 is going above the high of the Bar 2, a BUY STOP order is hit and the position is entered.

The underlying asset is the **S&P 500 index**. My focus is to simulate an algorithmic trading over a LONG only direction, so the pattern is used to buy a position and sell it at a higher price (hopefully). All simulations are tested with my software libraries written in R.

##### Daily bars
1. Simulations assuming Slippage = 0
  1. [Three bars revised](https://nalon99.github.io/publications/three_bars_revised/setup_3bars_revised_no_slippage.html)
  2. [Three bars revised with momentum](https://nalon99.github.io/publications/three_bars_revised/setup_3bars_revised_enhanced_no_slippage.html)
2. Simulations assuming Slippage = 1 basis point
  1. [Three bars revised](https://nalon99.github.io/publications/three_bars_revised/setup_3bars_revised_slippage.html)
  2. [Three bars revised with momentum](https://nalon99.github.io/publications/three_bars_revised/setup_3bars_revised_enhanced_slippage.html)

##### Intraday bars
1. Simulations assuming Slippage = 0
  1. [Three bars revised](https://nalon99.github.io/publications/three_bars_revised/setup_3bars_revised_5_no_slippage.html)
  2. [Three bars revised with momentum](https://nalon99.github.io/publications/three_bars_revised/setup_3bars_revised_5_enhanced_no_slippage.html)
2. Simulations assuming Slippage = 1 basis point
  1. [Three bars revised](https://nalon99.github.io/publications/three_bars_revised/setup_3bars_revised_5_slippage.html)
  2. [Three bars revised with momentum](https://nalon99.github.io/publications/three_bars_revised/setup_3bars_revised_5_enhanced_slippage.html)


The second case (ii) uses the same pattern, and in addition adds a filter signal looking for an underlying "momentum" of the trend, in order to avoid entering a long position when a downward price movement is occurring.
As many momentum indicators (RSI, MACD, etc.) this creates a lag of the responsiveness of the system, and during sideways period, may be ineffective.

#### Conclusions
Respect to my other simulation on the classic three bars reversal pattern, this modified version has an overall better performance. Looking at the intraday backtest with a 5 minutes timeframe, the equity curve is higher. There are many trades respect to the classic version of the pattern, and they help to get a better outcome.
The problem arises when slippage is accounted and it affects the goodness of the system, so adding a momentum filter lowers down the total number of trades (and costs) and the equity curve has less drawdown and a higher total return.  
Let's look at the daily bars backtest, in this case the revised pattern is outstanding, and slippage costs are very small respect to the average PnL (profit & loss) of each trade. A momentum filter is not recommended and a simple exit strategies with a trailing stop set to the low price of the previous bar is the best chance.  
From my perspective the revised pattern of the three bars reversal achieves better performances for a position trader and a day trader.  
