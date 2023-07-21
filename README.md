# crypto-systematic-strategy

The purpose of this project is to showcase a systematic strategy in Cryptocurrency, more specifically, an hourly frequency Long-short strategy with a universe of 30+ cryptocurrencies. The in-sample period is set to be 2019 to 2022 and out-sample is 2023-01-01 to 2023-06-01.

### Data
The original 1min resolution data is obtained from https://www.kaggle.com/datasets/tencars/392-crypto-currency-pairs-at-minute-resolution. In order to reduce the effect of some errors/outliers in the data, I reduce the resolution to 1 hour. More details could be found in the notebook **data_pipeline.ipynb**

### Backtest
The backtest framework uses the signal value to generate the weight of the long-short portfolio and compute the historical performance like Sharpe ratio, annual return, and turnover ratio. The trading fee is set to be 0.1%. More details about the assumption and limitations of the Backtest Framework could be found in the Summary section in the notebook **strategy.ipynb**

### Signal
The notebook **strategy.ipynb** elaborates on several signal ideas, with their backtest performance and discusses the limitation/bias and ways of improvement. Moreover, this notebook also displays the performance of an equal-weight combination of signals to test both the strategy's insample and outsample performance. 
