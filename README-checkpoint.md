# Week8_Project1

Using Market Sector Behaviors to Hedge Portfolios in a Downturn

Path to File in GitHub - Week8_Project1 -> Resources -> Project_1_Final_jsjp_revised.ipynb
To view the slide presentation in pdf format: Week8_Project1 -> Resources -> Navigating Market Sectors in a Downturn.pdf

Note: we need to acknowledge 2 errors:
1 - When calculating cumulative returns, we used ##cumulative_returns = (1 + x).cumprod().dropna().reset_index()## instead of cumulative_returns = ((1 + x).cumprod() - 1).dropna().reset_index().
The result is that a cumulative return of 1.0 in our charts would be the break-even point, and anything under 1.0 would be a loss. But the presentation has been given and the project has been completed, so we just want to acknowledge the error. 
2 - We used two ETFs - VDC and XLP - which unfortunately represent the same sector. This was discovered too late. If we had more time, we would find the missing sector and recalculate everything with an appropriate ETF. 

Jesus Saenz - Utilities and Consumer Staples

Steve Stark - Materials, Consumer Discretionary & Industrials

Angelita Fuentes - Healthcare and Financial Sector

Jason Parsons - Real Estate and Telecommunications

Kashyap Suratia - Technology and Energy

Core Messages
- In a downward market, there are still areas where investors can find hedges and capture gains during the downturn. 

Hypothesis :
Technology, Consumer Staples, Utilities, and Healthcare will be sectors that can survive market downturns and a place where investors can hedge against a major downturn. 

What do we want from the data?
Market data for the 2008 financial crisis. Jan. 03, 2006, through Dec. 30, 2010.
Flat market Jan. 02, 2014, through Dec. 29, 2017.
Political period Jan 03, 2017, through Dec 30, 2019.

Retrieve daily and cumulative returns from these three different periods expressed in visualization format.

We want the yearly returns for a ten-year period beginning January 4, 2010 until December 30, 2020.


Questions:

Which sectors offer the best return-per- unit-of-risk? ( Sharpe Ratio >= 1.0)

        Crash 1: All sectors had Sharpe Ratios well below 1.0

        Crash 2: VGT - Sharpe Ratio above 1.0

        Crash 3:  VGT and VHT (Health Care) both with Sharpe Ratios over 1.0

Which sectors may diverge from a downtrending S&P 500? (low/negative correlations)

        Overall, sectors mostly correlated to the S&P 500. VCR, VIS & VGT had the highest correlation to the S&P 500. 


Which sectors will provide the strongest return in a down market? (cumulative returns)

    Information Technology &  Health Care consistently outperformed the S&P 500. 
    From the Monte Carlo Simulations on the stock APIs, the winners were BRK.B, JNJ, PG and WMT.
    Overall, the winning sectors were:
        Information Technology
        Health Care
        Consumer Staples
        Consumer Discretionary
        Financials



How favorable a return can be projected for a portfolio leveraged in favor of these sectors? 
(ETF weighted model portfolio)

        All weighted ETF portfolios outperformed the S&P 500 and came out of the downturns with positive returns. 


Creating a weighted  portfolio with select stocks from winning sectors, what kind of returns could be anticipated? (Ticker Weighted Model Portfolio)

        Monte Carlo Simulations on winning stocks in different sectors showed as much as 5x returns over a 5 year period. 





