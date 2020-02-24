---
layout: post
title: Why asset price volatility increases wealth inequality
---

This blog post will cover [my paper](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3452599) which explains why an increase in asset price volatility will lead to an increase in wealth inequality.

Wealth inequality, and inequality in general, have recently come to the forefront
of economics ([Pikkety 2015](https://www.aeaweb.org/articles?id=10.1257/aer.p20151060), [Saez & Zucman 2016](https://academic.oup.com/qje/article/131/2/519/2607097)). When it comes to the role of the stock market in generating wealth inequality, [Campbell, Ramadorai, and Ranish 2019](https://www.aeaweb.org/articles?id=10.1257/aeri.20180158) find that stock return heterogeneity increased equity wealth inequality in Indian stock markets. They assert that if some undiversified investors randomly do well, while others randomly do poorly, this would generate inequality on its own.

In my paper, I build on that assertion and as ask how stock price volatility is related to wealth inequality. It is well known that stock price volatility magnifies trading returns and losses. Following the logic of [Campbell, Ramadorai, and Ranish 2019](https://www.aeaweb.org/articles?id=10.1257/aeri.20180158), if stock price volatility increases log heterogeneous returns, this should, in turn, increase wealth inequality.

Testing this assumption is problematic because it requires data on individual wealth inequality from those individuals that participate in the stock market. This type of data is typically not available. Furthermore, one would like to operate in a controlled setting where the effect of volatility on inequality can be isolated.

To do the latter, I turn to simulation modelling. The type of model I employ is an agent-based model because in these types of models individual data can be tracked. My model consists of a hundred noise traders that hold a portfolio that contains stocks and money. Each agent forms expectations about the future stock price based on white noise. This means that every simulation period agents will randomly expect the price to move up or down. When they expect that the price will go up the next period, they buy now. Agents that expect the price to go down will try to sell stocks.

This means that in the simulation, there is supply and demand. How will these be matched? For this, I use a limit-order book matching algorithm that is very similar to those employed by real stock markets. The algorithm tries to match buy orders with the highest price to sell orders with the lowest price, as long as the price of the buy order is higher or equal to that of the sell order. When two orders are matched, a transaction will take place between the owners of these orders.

When simulating this model over time, the following data is generated.

![](https://flic.kr/p/2ix3AbB)

My main result is that increasing volatility will increase wealth inequality at the end of the simulation.

This result is robust to a sensitivity analysis.

This work is novel because most research has focused on a channel that works through stock price levels. Following this channel, when stock prices rise, inequality increases because it is mostly the rich that own stocks and vice versa.  
