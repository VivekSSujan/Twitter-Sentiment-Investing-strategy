# Twitter-Sentiment-Investing-strategy
A sentiment-driven stock investing strategy that uses Twitter engagement metrics (likes and comments) to rank and select high-interest stocks each month. This strategy builds a rebalanced portfolio of the top 5 sentiment-ranked stocks and compares its performance against the NASDAQ ETF (QQQ).

📊 Workflow Overview

	1.	Load Twitter Sentiment Data
 
	•	Source: CSV file with tweet data (date, symbol, twitterLikes, twitterComments)
 
	•	Filtered for stocks with >20 likes and >10 comments.
 
	•	Created a custom engagement_ratio = comments / likes.
 
	2.	Aggregate Monthly Sentiment
 
	•	Data grouped by month and stock.
 
	•	Calculated average engagement ratio per stock.
 
	•	Ranked stocks within each month based on engagement.
 
	3.	Select Top 5 Stocks Monthly
 
	•	Chose top 5 stocks from each month (based on engagement rank).
 
	•	Shifted selection to the start of the next month for investing.
 
	4.	Price & Return Data
 
	•	Used Yahoo Finance (yfinance) to fetch historical stock data.
 
	•	Calculated log returns of selected stocks.
 
	•	Constructed a monthly rebalanced portfolio of top 5 sentiment-ranked stocks.
 
	5.	Compare with Benchmark
 
	•	Fetched QQQ (NASDAQ ETF) prices.
 
	•	Calculated log returns of QQQ.
 
	•	Compared strategy returns with benchmark returns visually.
