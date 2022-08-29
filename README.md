# ALPHA STOCK STRATEGY OF A-SHARE MARKET

All the content below are the contributions I made during my working experience as a Quant analyst at [Anzhi Investment](http://www.anzhicapital.com/). Some of the strategies are sourced from open-souce materials and have been improved based on the original version.
## Contents

- [Summary](#summary)
- [Strategies and Performances](#Strategies)
- [Future Work and valuable resources](#code-of-conduct)
- [Team](#team)

### Summary

This project is build based on research results from different hedging funds and security companies. Each strategy will
has its sourcing materials in its own folder with my own understanding and expectations of future work. Plus, references
materials are all stored in
[Google Drive](https://drive.google.com/drive/folders/1KSSDIotg2n2ICwLlg-hzt7jbaX5b0g6G?usp=sharing)
and have all been categorized into different levels from **L1~L5** as of recommendation degree(i.e. **L5** is highly
recommended whereas **L1** is poorly recommended). Backtest results will also be posted for references.

### Strategies and Performances


#### Single factor strategy

Single alpha factor strategy is aming to find those stocks which are highly valued in one direction, which can be both financial aspect(PB/ROE etc.) or cash flow of (north streaming, public equity fund etc.), also the forecasting statistics we get from reports of institutions. It is easy for Portforlio Managers to understand and implement(choose different direction based on his/her own understanding of current/future market), but it is lack of robustness which means this single direction will lose its ability of choosing the right stocks in the future.

* $pb\_roe\_ep$ : combined info from $PB$, $ROE$ as well as ep, to find those stocks which are undervalued.
* $fnetprofit\_gr$ : stocks which have a profound growth of netprofit stats forecasted by several analyst.
* $con\_roe$ : common-joint roe forecasted by serveral analysts and algo will set a decay factor which will take time series decaying of forecasting ability into consideration.

#### Strategies
Different strategies which sourced from analyst strategy reports of large-scale mutual fund are reproduced and improved.
##### Excess Expectation
Using different criteria to create a stock pool which have the potential to excess their expections as of financial statistics, which we believe that those stocks will be able to generate alpha returns comparing to the whole market. Fundamental filter and techical filter will be utilized separately as a 2 layer filter to optimize our targeting portforlio.
##### Ind_Timing
Timing the right industries will create a noticeable alpha return, here we will conclude the general strategies that have been deployed by most of the funds and reproduce them as different timing signals.
##### Investor Preferences
Those participants on the A share market are clustered as different types arbitrarily which are **Value Investor**,**Growth Investor**, **GARP Investor**, **Trading Investor**, different types of investors will have their own criterias to select stocks and we will combine those different criterias together to create a factor representing that direction of layering of stocks.
##### North top 20
As mentioned above, north capital steaming has played an important role in A share market, we will keep track of the toppest capital inflows and set those stocks as our target portfolios.
##### Multi Factors
Different factors are clusterd into different dimensions/groups arbitrarily, which are pure valuation, relative valuations.
##### Machine Learning Techniques
Unlike the most commmon way that are deployed in hedge fund companies in China which are highly unrobust since they keep optimize factors iteratively to improve in-sample performances, a robust methodology is absolutely a better way to replace the original method and will have a great performance especially on out-sample/test data.
So, gene porgramming, tree-based methods([XGBoost](https://github.com/JonnyStart95/Stock_Strategies_Panel/blob/master/Machine%20Learning%20Techniques/XGBoost.md)/lightGBM etc.), deep learning(LSTM and other neural based networks) are researched and implemented to as a brand new strategy right now in our company(simulating and testing stage).
