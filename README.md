# Bitcoin_Arbitrage_Analysis


## Summary
In this program, we are sorting through historical trade data for Bitcoin on two exchanges: Bitstamp and Coinbase. We are applying the three phases of financial analysis to determine if any arbitrage opportunities existed for Bitcoin between Janurary 2018 and March 2018.

This analysis consists of 3 phases.

1. Collecting the data.

2. Preparing the data.

3. Analyzing the data. 


### Collecting the Data

1. Using the Pandas `read_csv` function and the `Path` module, importing the data from `bitstamp.csv` file, and creating a DataFrame called `bitstamp`. Setting the DatetimeIndex as the Timestamp column, and parsing and formatting the dates.

2. Using the `head` function to confirm that Pandas properly imported the data.

3. Repeating Steps 1 and 2 for `coinbase.csv` file.


### Preparing the Data

1. For the bitstamp DataFrame, dropping all `NaN' values in the DataFrame.

2. Using the `str.replace` function to remove the dollar signs ($) from the values in the Close column.

3. Converting the data type of the Close column to a `float`.

4. Reviewing the data for duplicated values, and dropping them if necessary.

5. Repeating Steps 1–4 for the coinbase DataFrame.

### Analyzing the Data

1. Choosing the columns of data on which to focus analysis.

2. Getting the summary statistics and plotting the data.

3. Focusing analysis on specific dates.

4. Calculating the arbitrage profits.


## Results
    
It is clear that as time progresses through the data, the spread between the bitcoin prices of the two exchanges narrows greatly.  This drastically reduces the potential return of arbitrage as you move further in time from January to March, 2018.  Upon analysis, the spread between the prices is so extreme, that in March there was no potential profits from arbitrage between bitcoin prices from bitstamp and coinbase (after factoring in trade costs).  Although the cause for this reduction in spread is not proven in this analysis, it is a reasonable assumption that arbitrage betweeen these two exchanges rapidly increased in the February of 2018, greatly reducing the spread in price, and by March had virtually eliminated opportunites for further arbitrage (given the assumed trading costs).

## Requirements

Python 3.7
Jupyter Lab
Pandas library