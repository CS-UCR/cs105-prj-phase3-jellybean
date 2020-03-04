# CS105-Project: Data Analysis for Stock Prediction

###### jellybean_proj_CS105.ipynb

Program scrapes stockmonitor.com for top performing 100 Nasdaq stocks (live data) 
and then extracts those symbols to get corresponding historic data from Yahoo Finance.
All data is collected, cleaned, and saved to corresponding csv files.
Data includes symbol, name, price, volume, pChange, high, low.

Two machine learning algorithms are used to make predictions about the stock data: 
Linear Regression & Neural Network Regressor. By using two ML algos, we can see how
their predictions compare. When making a buying decision, it’s probably wise to have 
a second opinion.

Both ML algos train on the historic data for each stock with the label being percent change.
The pCHange target will help the ML algos learn how much each stock changes each day based 
on performance.

Once each ML algo has made its prediction for each stock, we take the 5 largest predicted
percent change movers. Then, we find the lowest value and add that to all best predictions 
each for their corresponding algorithm. We do this to make the graphs easier to understand 
when comparing which stocks are favored to move more than others.

Finally, the first two bar charts demonstrate the best 5 predicted stocks for each ML algo, and
the third, top 5 current movers live. We expect to see at least one stock that the ML algos agree 
on and that stock should be in the top 5 movers of the day by bell close.

## Installation

Code is ready to run in jupyter notebook. 

'pip install' needed dependencies, or if using anaconda, 
install libraries through navigator/profile terminal.

## Usage

'Config' section is self-explanatory

The program is meant to be run at the beginning of the trading day.
If you already have the historic data you need then simply leave 'updateHistoric' = False.

The program can be run after trading hours to see how the predictions performed.

run in jupyter notebook
