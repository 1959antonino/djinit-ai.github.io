---
layout:     post
title:      Algorithmic Trading
date:       2020-09-27 07:00:00
summary:    Implementations of AI in Trading
categories: Python, Stock Market, AI
---

# Algorithmic Trading

Did you know that in reality, a trade could generate profit margins at a pace that is impossible for humans?

Thanks to <strong>Algorithmic Trading</strong>, a growing number of investors are taking advantage of what they consider to be optimal market conditions to come out considerably richer.

<em>Whoa slow down…</em>

### What is an Algorithm?
Algorithms are math equations used to program computers to make decisions.An algorithm is a procedure or formula for solving a problem, based on conducting a sequence of specified actions. A computer program can be viewed as an elaborate algorithm. In mathematics and computer science, an algorithm usually means a small procedure that solves a recurrent problem.
<br>
<p align="center">
<img src="/images/algorithmic_trading-1.png" height=500 width=750 />
</p>

<em>So now you must be wondering...</em>

### What is trading?

<p align="center">
<img src="/images/algorithmic_trading-2.png" height=250 width=375 />
<img src="/images/algorithmic_trading-3.png" height=250 width=375 />
</p>

We all know how important it is to invest money in the right avenues to grow wealth. Stock market investment is one such lucrative option that has rewarded steadfast investors with high returns over the years. However, to gain the maximum out of a financial instrument, it is essential to know about its workings.

The concept behind how the stock market works is pretty simple. Operating much like an auction house, the stock market enables buyers and sellers to negotiate prices and make trades.

<em>We finally arrived at …</em>

## Algorithmic Trading Defination

Algorithmic trading (also called automated trading or algo-trading) uses a computer program that follows a defined set of instructions (an algorithm) to place a trade.Algorithmic trading makes use of complex formulas, combined with mathematical models and human oversight, to make decisions to buy or sell financial securities on an exchange. The trade, in theory, can generate profits at a speed and frequency that is impossible for a human trader.The defined sets of instructions are based on timing, price, quantity, or any mathematical model. Apart from profit opportunities for the trader, algo-trading renders markets more liquid and trading more systematic by ruling out the impact of human emotions on trading activities.
In simple words an automated and pre programmed trading instructions with a lot of different parameters is algorithmic trading.

### Where is it used?

According to “Global Algorithmic Trading Market 2018-2022” report published by Research and Markets, if data is to be believed, the global algorithmic trading market size is projected to grow from $11.1 billion in 2019 to $18.8 billion by 2024, expanding at a CAGR of 11.1 per cent. Moreover, it is being used widely and is ever-expanding its reach in emerging markets.

On Wall Street, traders employ algo trading to buy and sell stocks automatically. Algorithmic trading may extend momentum trades as stocks make a big run.

Algorithmic trading is dominated by large trading firms, such as hedge funds, investment banks, and proprietary trading firms. Given the abundant resource availability due to their large size, such firms usually build their own proprietary trading software, including large trading systems with dedicated data centers and support staff.

<p align="center">
<iframe width="80%" height="30%" src="https://www.youtube.com/embed/2u007Msq1qo" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</p>

### Why is it used?

Advantages of higher accuracy and lightning-fast execution speed, trading activities based on computer algorithms have gained tremendous popularity.

The defined sets of instructions are based on timing, price, quantity, or any mathematical model. Apart from profit opportunities for the trader, algo-trading renders markets more liquid and trading more systematic by ruling out the impact of human emotions on trading activities.

Technically, there are several mathematical algorithms at play for making the trading decisions on the basis of current market data, which then send and execute the order(s) in the financial markets. This method makes trading free of all emotional human impact (like fear, greed, etc.) since decisions to carry out each trade are made by computers in a systematic manner.

Big firms prefer these conditions that make them the most profitable.

### Is it for me as an individual?

<em>Yes, absolutely</em>

If you are planning to open a trading account you can give algo trading a shot. At an individual level, experienced proprietary traders and quants use algorithmic trading. Proprietary traders, who are less tech-savvy, may purchase ready-made trading software for their algorithmic trading needs. The software is either offered by their brokers or purchased from third-party providers. Quants generally have a solid knowledge of both trading and computer programming, and they develop trading software on their own.

### Algo-trading provides the following benefits:
  <ul>
    <li>Trades are executed at the best possible prices.</li>
    <li>Trade order placement is instant and accurate (there is a high chance of execution at the desired levels).</li>
    <li>Trades are timed correctly and instantly to avoid significant price changes.</li>
    <li>Simultaneous automated checks on multiple market conditions.</li>
    <li>Reduced risk of manual errors when placing trades.</li>
    <li>Algo-trading can be backtested using available historical and real-time data to see if it is a viable trading strategy.</li>
    <li>Reduced the possibility of mistakes by human traders based on emotional and psychological factors.</li>
    <li>Ensuring that orders are executed at what are deemed to be optimal buying or selling conditions</li>
    <li>Often limits or reduces transaction costs, thus allowing investors to retain even more of their profits.</li>
    <li>Monitoring many stocks at once.</li>
  </ul>
    
<em>That’s a lot of benefits,</em>

### Why doesn’t everyone use it?

Drawbacks:
  <ul>
    <li>ne simple mistake can rapidly escalate in a major way.</li>
    <li>"Flash crashes" on global markets - algorithmic trading was blamed for the "Flash Crash" of 2010, which led U.S. stock indexes to collapse (though they rebounded within an hour), as well as an October 2016 crash that saw the British pound plunge toward its 31-year-low in a single night.</li>
    <li>It has to be governed as it's just a piece of software that cannot be blindly trusted.</li>
  </ul>
    
### Requirements to be met for a trader?
  <ul>
    <li>Should have knowledge of the market as its important for making the algorithm work efficiently and smoothly.</li>
    <li>Clarity about what should have been implemented.</li>
    <li>Should take into account all the fail cases - where the program can produce undesirable effects.</li>
    <li>Should be clear with all the stuff that needed: the data and its correlation.</li>
    <li >Order placing capabilities which can route the order to the correct exchange.</li>
    <li >Backtesting capabilities on historical price feeds.</li>
    <li >As a smart investor, you need to understand risks and challenges that are involved in trading.</li>
  </ul>
  
As we dive deeper into algorithmic trading we need to understand the parameters that can affect the stock prices and the correlations that we need.

### Parameters to be checked

#### Statistical Arbitrage

One example is a statistical arbitrage trading partner where we see the ratio/spread between a stock price, co-integrated. If the value of the spread exceeds the expected range, then you buy a stock that has gone down and sell stocks that have outperformed in the hope that the spread will return to normal levels.

#### Availability of Market and Company Data

All trading algorithms are designed to act on real-time market data and price quotes. A few programs are also customized to account for company fundamentals data like earnings and P/E ratios. Any algorithmic trading software should have a real-time market data feed, as well as a company data feed. It should be available as a build-in into the system or should have a provision to easily integrate from alternate sources.

<u>Example:</u>

Yahoo Provides such data for the users:
<strong>To fetch the data from Yahoo finance, write ‘pip install yfinance’ in the terminal.</strong>
!pip install yfinance
We can then use the download method to fetch the data in the ipython notebook:

\# Import yfinance<br>
import yfinance as yf

\# Get the data for stock Facebook from 2017-04-01 to 2019-04-30<br>
data = yf.download('AAPL', start="2017-04-01", end="2019-04-30")

\# Print the first five rows of the data<br>
data.head()

#### Connectivity to Various Markets

Traders looking to work across multiple markets should note that each exchange might provide its data feed in a different format. Your software should be able to accept feeds of different formats. Another option is to go with third-party data vendors like Bloomberg and Reuters, which aggregate market data from different exchanges and provide it in a uniform format to end clients.

#### Latency

This is the most important factor for  algorithm trading. Latency is the time-delay introduced in the movement of data points from one application to the other.
In today’s dynamic trading world, the original price quote would have changed multiple times within this 1.4 second period. Any delay could make or break your algorithmic trading venture. One needs to keep this latency to the lowest possible level to ensure that you get the most up-to-date and accurate information without a time gap. Latency has been reduced to microseconds, and every attempt should be made to keep it as low as possible in the trading system. A few measures to improve latency include having direct connectivity to the exchange to get data faster by eliminating the vendor in between; improving the trading algorithm so that it takes less than 0.1+0.3 = 0.4 seconds for analysis and decision-making; or by eliminating the broker and directly sending trades to the exchange to save 0.2 seconds.

<br>
<p align="center">
<img src="/images/algorithmic_trading-4.png" height=500 width=750 />
</p>

### Algorithmic Trading Strategies

<p align="center">
<iframe height="500" width="700" src="https://www.youtube.com/embed/4Ae2_i5nMxs" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</p>

Any strategy for algorithmic trading requires an identified opportunity that is profitable in terms of improved earnings or cost reduction. The following are some of the common trading strategies used in algo-trading:

#### Trend-following Strategies

The most common algorithmic trading strategies follow trends in moving averages, channel breakouts, price level movements, and related technical indicators. These are the easiest and simplest strategies to implement through algorithmic trading because these strategies do not involve making any predictions or price forecasts. Trades are initiated based on the occurrence of desirable trends, which are easy and straightforward to implement through algorithms without getting into the complexity of predictive analysis. Using 50- and 200-day moving averages is a popular trend-following strategy.

#### Arbitrage Opportunities

Buying a dual-listed stock at a lower price in one market and simultaneously selling it at a higher price in another market offers the price differential as risk-free profit or arbitrage. The same operation can be replicated for stocks vs. futures instruments as price differentials do exist from time to time. Implementing an algorithm to identify such price differentials and placing the orders efficiently allows profitable opportunities.

#### Index Fund Rebalancing

Index funds have defined periods of rebalancing to bring their holdings to par with their respective benchmark indices. This creates profitable opportunities for algorithmic traders, who capitalize on expected trades that offer 20 to 80 basis points profits depending on the number of stocks in the index fund just before index fund rebalancing. Such trades are initiated via algorithmic trading systems for timely execution and the best prices.

#### Mathematical Model-based Strategies

Proven mathematical models, like the delta-neutral trading strategy, allow trading on a combination of options and the underlying security. (Delta neutral is a portfolio strategy consisting of multiple positions with offsetting positive and negative deltas—a ratio comparing the change in the price of an asset, usually a marketable security, to the corresponding change in the price of its derivative—so that the overall delta of the assets in question totals zero).

## Implementations:

A lot of algorithmic trading courses as well as contents are available that help to start the algorithmic trading journey.
Languages for Algorithmic Trading Implementation:Matlab, Python, C++, JAVA, and Perl 

### Python: 

#### Libraries:
It has a lot of libraries available for implementing algorithmic trading:<br>
Technical Analysis: TA-Lib.<br>
Backtesting: PyAlgoTrade, Zipline, Pybacktest.<br>
Python Trading Libraries for Data Collection- Ultrafinance, TWP (Trading With Python).<br>
Python libraries used for connecting to live markets using IB: IBridgePy, IBPy.

#### Code Implementation:
You need to install oandapy and create account id and access token for running the following code <br>
You can install the library by writing: ‘pip install oandapy’ in the terminal

<br>
<p align="center">
<img src="/images/algorithmic_trading-5.png" height=500 width=750 />
</p>

##### Backtesting

<br>
<p align="center">
<img src="/images/algorithmic_trading-6.png" height=500 width=750 />
</p>

<br>
<p align="center">
<img src="/images/algorithmic_trading-7.png" height=500 width=750 />
</p>

<br>
<p align="center">
<img src="/images/algorithmic_trading-8.png" height=500 width=750 />
</p>

<br>
<p align="center">
<img src="/images/algorithmic_trading-9.png" height=500 width=750 />
</p>

<br>
<p align="center">
<img src="/images/algorithmic_trading-10.png" height=500 width=750 />
</p>

##### Automated Trading

<br>
<p align="center">
<img src="/images/algorithmic_trading-11.png" height=500 width=750 />
</p>

<br>
<p align="center">
<img src="/images/algorithmic_trading-12.png" height=500 width=750 />
</p>

<br>
<p align="center">
<img src="/images/algorithmic_trading-13.png" height=500 width=750 />
</p>

## Conclusion:

In the end, algo trading has brought a new era to online trading.Though it’s not 100% dependable but if you stay vigilant then you can profit consistently from this technology.The latest automated trading platform keep updating and new features are being added continuously.

### Some courses to refer:
  <ul>
    <li><a
        href="https://www.google.com/url?q=https://www.coursera.org/learn/introduction-trading-machine-learning-gcp&amp;sa=D&amp;ust=1601212995260000&amp;usg=AOvVaw1dQwBefPe_ZWhx90qX_MN0">https://www.coursera.org/learn/introduction-trading-machine-learning-gcp</a>
    </li>
    <li><a
        href="https://www.google.com/url?q=https://www.coursera.org/specializations/machine-learning-trading&amp;sa=D&amp;ust=1601212995260000&amp;usg=AOvVaw2TQrFEqhd8SdcjtdofvK3n">https://www.coursera.org/specializations/machine-learning-trading</a>
    </li>
    <li><a
        href="https://www.google.com/url?q=https://www.coursera.org/specializations/machine-learning-reinforcement-finance&amp;sa=D&amp;ust=1601212995261000&amp;usg=AOvVaw1ChThADu_3HywakciE59Id">https://www.coursera.org/specializations/machine-learning-reinforcement-finance</a>
    </li>
    <li><a href="https://www.google.com/url?q=https://www.coursera.org/learn/trading-algorithm&amp;sa=D&amp;ust=1601212995261000&amp;usg=AOvVaw367MvtEOfzkWxGp3-vLOCb">https://www.coursera.org/learn/trading-algorithm</a></li>
    <li><a href="https://www.google.com/url?q=https://www.coursera.org/learn/advanced-trading-algorithms&amp;sa=D&amp;ust=1601212995262000&amp;usg=AOvVaw38-Xfsxsq1zZbG_RMjkHmh">https://www.coursera.org/learn/advanced-trading-algorithms</a></li>
  </ul>

