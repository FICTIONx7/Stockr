# Stockr
Stalk the Stock

# INTRODUCTION

Stockr is a personal Quants-based project conceived on a summer night to serve as a one stop destination for all trading related things conceivable.
The tagline "Stalk the Stock" pretty much sums up the entire purpose of this project- "Stockr".

# TABLE OF CONTENTS



# PROBLEM

As a novice trader, I constantly found myself switching from one tab to another, one strategy to another, one broker to another and on and on. I could not find one single place wherein one could limitlessly explore and play around with the stock data. Some of the problems were straightaway visible to me while some more i came across during the journey. I have attempted to broadly list down the major problems as:

### PROBLEM 1

- Technical Indicators, a day-trader closest companion lacked vastly in most terminals that limited a trader to explore its complete potential. As a trader, the parameters of the technical indicators that i could play around with were limited as per the terminal. Neither i had the opportunities to try off new technical indicaots.

### PROBLEM 2

- There was no potential use of MACHINE LEARNING in any major trading terminal to serve as an additional indicator.

### PROBLEM 3

- Lack of data visualization the way a user wants.

### PROBLEM 4 

- No existence of backtesting strategies. There was no place to create a strategy for backtesting without being limited by the parameters of the strategy that one could play around with.

### PROBLEM 5

- No presence of algorithmic trading in the terminal itself. In the name of "automated trades", one was limited to few parameters based on which one could trade.

### PROBLEM 6

- No single trading terminal had an automated algorithm to detect things such as: Support and Resistance levels, Chart Patterns.

# SOLUTIONS

All of the above problems are resolved in this project and Stockr is continously being updated to include new things to resolve several other problems.

### SOLUTION 1

In Stockr, all the algorithms for Technical Indicators are manually coded to allow complete freedom in using them and playing around with any of the parameters of a technical indicator that a trader wishes to play around with.

### SOLUTION 2

Stockr includes a lot of statistical analysis upon stock data and then deploys a Machine Learning model(XGBoost) for future trade trend prediction to predict whether the trade would reach its target, stoploss or none.

### SOLUTION 3

Stockr has interactive candlestick plots for the price action and all the Technical indicators.

### SOLUTION 4

Stockr has several manually coded Backtesting strategies such as Ichimoku backtesting strategy or Double_Top/Double_Bottom chart pattern backtesting strategy. After backtesting, Stockr creates and provides a useful database related to all the trade details of the backtesting strategy along with the backtesting results.

### SOLUTION 5

Stockr connects with the trading terminal's API to allow users to trade in real time based on a user defined strategy. One can simply connect to the trading terminal through the code and modify statements based on which one wished to trade and the bot will automatically place the order.

### SOLUTION 6

Stockr has algorithms to automatically detect Support and Resistance levels and also detects not only the candlestick patterns but also Chart patterns like Double Top/ Double Botttom, Flag Up/ Flag Bottom, etc. It stores the pattern detection information on a database which the user can access to study historical data.


# INSTRUCTIONS and WALKTHROUGH

The Stockr project can be accessed from [here](https://github.com/FICTIONx7/Stockr).
To keep the project size small enough so as to be visible on Github itself, the complete code has been broken down into 6 different parts.

[PART 1](https://github.com/FICTIONx7/Stockr/blob/main/Quants_Project_Part_1.ipynb) imports the necessary libraries and modules. It then fetches historical stock data onto a database and visualizes it on an interactive CandleStick plot.

##### NOTE: In order to keep the notebook size small and for the plots to be visible, the plots have been rendered static.

[PART 2](https://github.com/FICTIONx7/Stockr/blob/main/Quants_Project_Part_2.ipynb) has manually coded algorithms for major Technical Indicators. It plots the techincal indicators on intractive plots. Further, it stores the historical indicator values on a separate database.

[PART 3](https://github.com/FICTIONx7/Stockr/blob/main/Quants_Project_Part_3.ipynb) has manually coded algorithms to detect major candlestick and chart patterns. It further stores the pattern detection details on a database.

[PART 4](https://github.com/FICTIONx7/Stockr/blob/main/Quants_Project_Part_4.ipynb) consists of some statistical analysis over stock data. It identifies trade trend frequency based on user defined target and stoploss. It further deploys a Machine Learning model(XGBoost) for future trade trend prediction.

[PART 5](https://github.com/FICTIONx7/Stockr/blob/main/Quants_Project_Part_5.ipynb) has algorithms for several backtesting strategies. The backtesting results and trade details are stored in a database. The strategies are further finetuned to increase returns.

[PART 6](https://github.com/FICTIONx7/Stockr/blob/main/Quants_Project_Part_6.ipynb) connects with the broker's terminal API in order to implement an automated trading bot based on user defined signal.

##### NOTE: The complete Source Code can be accessed from [here](https://github.com/FICTIONx7/Quants_Project/blob/main/Quants_Project_1.ipynb). Owing to the large Jupyter notebook size, the outputs aren't visible.

##### NOTE: In case you want to run the notebook by yourself, simply press ENTER wherever an input is asked to proceed with the default values already embedded within in most places. Otherwise, enter a suitable value.

# RELEVANT EXPLANATIONS

Walkthrough for Chart detection algorithm:

On running the Chart detection algorithm for TATAELXSI, we got the following database of dates whenever we encountered the Chart pattern.

![SS-signal](https://user-images.githubusercontent.com/110126448/186232027-bfdf2223-c3b3-426f-9198-7aa59cb2dab7.png)

Selecting any random date from here, let's say 09/03/2022

Proceed as shown below:

![SS-pattern](https://user-images.githubusercontent.com/110126448/186232483-deb5af63-182e-4386-b3a6-2d7a91655404.png)

After having drawn the trendline:
- Check whether the triangles formed form a double top or double bottom pattern. Look for historical Support and Resistance levels and see if they match with the pattern high and low. If the chart pattern is formed, trade accordingly.
- However, if double bottom and double bottom is not formed as in the above case, then trade in the latest trend direction with target as the pattern high and stoploss as the pattern low along with some variation based on your preference.
- As can be seen, the target was reached successfully in the above case without reaching stoploss.


Thank You.
