## Three bars reversal revised
A revised version of the three bars reversal pattern is depicted in this folder.

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
