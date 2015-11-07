## Three bars reversal
Under this chapter I collect some results applying the well know three bars reversal pattern. The underlying asset is the SP&500 index, starting from the turmoil of global financial markets during August 2015. My focus is to simulate an intraday trading with a 5 minutes time frame, LONG only, so the pattern is used to buy a position and sell it at a higher price (hopefully). All simulations are tested with my software libraries written in R.

##### Bearish and sideways cycle
1. Simulations assuming Slippage = 0
  1. [Three bars reversal](https://nalon99.github.io/publications/three_bars/setup_3bars_no_slippage.html)
  2. [Three bars reversal with momentum](https://nalon99.github.io/publications/three_bars/setup_3bars_enhanced_no_slippage.html)
2. Simulations assuming Slippage = 1 basis point
  1. [Three bars reversal](https://nalon99.github.io/publications/three_bars/setup_3bars_slippage.html)
  2. [Three bars reversal with momentum](https://nalon99.github.io/publications/three_bars/setup_3bars_enhanced_slippage.html)

##### Bearish end - Bullish cycle
1. Simulations assuming Slippage = 0
  1. [Three bars reversal](https://nalon99.github.io/publications/three_bars/setup_3bars_bullish_no_slippage.html)
  2. [Three bars reversal with momentum](https://nalon99.github.io/publications/three_bars/setup_3bars_bullish_enhanced_no_slippage.html)
2. Simulations assuming Slippage = 1 basis point
  1. [Three bars reversal](https://nalon99.github.io/publications/three_bars/setup_3bars_bullish_slippage.html)
  2. [Three bars reversal with momentum](https://nalon99.github.io/publications/three_bars/setup_3bars_bullish_enhanced_slippage.html)


The second case (ii) uses the same pattern, and in addition adds a filter signal looking for an underlying "momemtum" of the trend, in order to avoid entering a long position when a downward price movement is occuring.
As many momentum indicators (RSI, MACD, etc.) this creates a lag of the responsiveness of the system, and during sideways period, may be uneffective.

#### Conclusions
My view about this pattern is negative at least for the *bearish - sideways* scenario of the SP&500 index. Used for an intraday trading system, in particular with a short period (5 minutes) implies negative returns on the long run. Using a momentum indicator to filter out bad downward movements can help the overall result, but in a real trading environment with a slippage and commissions it's not enough.
Where this pattern really shines is with an upward movement of the underlying trend, and in such a case it works. In particular adding a filter based on the momentum makes the difference. In addition, a trailing stop placed to the previous lows seems to be the best way to manage each trade.
