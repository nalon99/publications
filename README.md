# publications
A repository for my ongoing research...

This repository hosts some results of my research about trading strategies and patterns in general.
With GitHub Pages I will add more content to the repository for different backtests and parameters used. Each html page with its results, will contain the parameters and in general all the conditions set to run the entire simulation.

## Three bars reversal
Under this chapter I collect some results applying the well know three bars reversal pattern. The underlying asset is the SP&500 index, starting from the turmoil of global financial markets during August 2015. My focus is to simulate an intraday trading with a 5 minutes time frame, LONG only, so the pattern is used to buy a position and sell it at a higher price (hopefully). All simulations are tested with my software libraries written in R.

1. Simulations assuming Slippage = 0
  1. [Three bars reversal](https://nalon99.github.io/publications/setup_3bars_no_slippage.html)
  2. [Three bars reversal with momentum](https://nalon99.github.io/publications/setup_3bars_enhanced_no_slippage.html)

The second case (ii) uses the same pattern, and in addition adds another filter looking for an underlying "momemtum" of the trend, in order to not enter a long position when a downward price movement is occuring.
As many momentum indicators (RSI, MACD, etc.) this creates a lag of the responsiveness of the system, and during sideways period, may be uneffective.
