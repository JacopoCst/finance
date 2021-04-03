# finance
Finance analysis python 
The non interactive version requires, to fully work, 2 datasets (the paths need to be inserted in the first chunk of code, for ease it’s set up as my downloads folder):
-	portfolio_path: csv with the actual portfolio, formatted as a standard download of the cvs from yahoo finance
-	new_stock_path: csv with the new stocks to analyze in relation with  the actual portfolio; it only requires the “Symbol” column

and it does the following:
1)	ANALYSIS PER STOCK: for every stock in the portfolio last price, gain according to the weighted purchase price across all the purchases, last 2 years price trend, last 20 days price trend with moving averages, beta and alpha according to single factor using SPY, volumes, last 2 years price trend, mean daily return (2 years and last 20 days), annualized return (2 years and last 20 days), distribution of returns
2)	ANALYSIS PORTFOLIO: same as analysis per stock but for the overall portfolio
3)	CORRELATION BETWEEN STOCKS: a simple correlation matrix between all the stocks in the portfolio
4)	COMPARISON PER INDUSTRY: using various industry indexes ("XLC", "XLY", "XLP", "XLE", "XLF","XLV", "XLI", "XLB", "XLRE", "XLK", "XLU", "SPDV", "DMDV", "EEMD") calculates correlation and beta for last 400 days and last 100 days, shows graphically portfolio vs index, summary table at the end
5)	SHARPE RATIO OPTIMIZATION: with 2 years data performs a sharpe optimization; it uses the logarithmic returns and a RFR = 0 (graphically I think that the max sharpe line becomes a curve in the log space, that’s why the tangency portfolio seems to be in a weird place, am I correct? It still looks weird and I can’t understand why)
6)	SHARPE RATIO OPTIMIZATION (custom) [1],[2]: through widget allows the user to select the preferred parameters for the optimization
7)	ANALYSIS OF NEW STOCK: similar to analysis per stock + correlation and beta with portfolio last 400 days and last 100 days, summary table at the end
8)	SHARPE RATIO OPTIMIZATION with new stocks (custom) [1],[2]: using all the new stocks in the portfolio, performs a similar optimization as sharpe optimization (custom)


The interactive version is simplified: it's only an exercise to show how easily these code can be translated in a Voilà application and it only has steps 1,2,3,4,5,6. 
The usage is immediate and only requires the packages listed in the code.
