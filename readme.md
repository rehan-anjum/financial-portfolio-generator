# Automated Financial Portfolio Generator #
Python program that consumes a list of tickers (minimum 25), and does data filtering and financial analysis to produce a risky financial portfolio.

## Achievements: ##
* Increased performance times by **3x** by utilizing multithreading and parallelism
* Developed efficient solution via use of maximum spanning tree algorithm to efficiently select stocks with high correlation and volatility
* Optimized NP hard solutoin in polynomial computational complexity
* Created data cleaning pipeline that sanitizes input data
* Accurately completed data analysis on portfolio and stock volatility

## Problems we ran into: ##
* The K-MST algorithm solution we came up with was already extremely difficult to implement, hence, we optimized the dataset for the graph and directly ran the **Maximum Spanning Tree** algorithm on multiple combinations of stock tickers.
* The graph was being initialized very slowly due to multiple dataframes being created. To solve this issue, we implemented multithreading and utilized hashtables instead of dataframes to achieve faster read and write times.
* There wasn't enough options data available for some stocks, so we implemented a data filtering solution for stocks that lacked sufficient options data.

## Set-up ##
### Dependencies: ###
* pandas
* numpy
* numpy_financial
* networkx
* matplotlib
* itertools
* datetime
* threading
* yfinance
* warnings

Authors: *Rehan Anjum, Rui Li, Anton Smetanov*