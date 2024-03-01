<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->

<!-- code_chunk_output -->

- [GOAL:Alpha Generation](#goalalpha-generation)
  - [Research Problem：Multi-factor model based on machine learning](#research-problemmulti-factor-model-based-on-machine-learning)
    - [EDA of A share](#eda-of-a-share)
      - [benchmark :CSI300](#benchmark-csi300)
    - [Getting data from A share(Daily frequancy data)](#getting-data-from-a-sharedaily-frequancy-data)
    - [Stock Data pre-procession](#stock-data-pre-procession)
  - [1.Mutifactor Model](#1mutifactor-model)
    - [1.1  Feature engineering(Factor mining)](#11--feature-engineeringfactor-mining)
      - [Replicate factor from research report](#replicate-factor-from-research-report)
      - [some useful link](#some-useful-link)
      - [Research report](#research-report)
      - [Interesting Paper (Trying use)](#interesting-paper-trying-use)
    - [1.2 Data preprocessing](#12-data-preprocessing)
    - [1.3 Single factor testing](#13-single-factor-testing)
    - [1.4  Multi-factor testing](#14--multi-factor-testing)
    - [1.5  collinearity diagnostics](#15--collinearity-diagnostics)
    - [1.6 Factor recombination](#16-factor-recombination)
    - [1.7 Select stock from A share according to our model](#17-select-stock-from-a-share-according-to-our-model)
      - [Based on Machine learning](#based-on-machine-learning)
  - [2. Bulid Risk Model](#2-bulid-risk-model)
  - [3. Portfolio optimization](#3-portfolio-optimization)
  - [4.Build a Backtesting structure](#4build-a-backtesting-structure)
  - [TODO:](#todo)
    - [1. Getting data and data preprocession](#1-getting-data-and-data-preprocession)
    - [2. Build a Backtesting structure and testing simple strategy](#2-build-a-backtesting-structure-and-testing-simple-strategy)
    - [3. Feature engineering](#3-feature-engineering)
    - [4. Factor testing](#4-factor-testing)
    - [5. Select stock based on ML](#5-select-stock-based-on-ml)
    - [6. Portfolio optimization](#6-portfolio-optimization)
      - [](#)

<!-- /code_chunk_output -->


# GOAL:Alpha Generation
## Research Problem：Multi-factor model based on machine learning

### EDA of A share
#### benchmark :CSI300

### Getting data from A share(Daily frequancy data)
* From Magnum Research


* From JQData
* From WIND(real-time data?)

### Stock Data pre-procession
* Excluding ST shares, science and technology board, B shares, new shares, delisted shares.
* Exclude data with less than 14 days of trading per month.
* Remove missing values.
* Indent the data by 1% up or down.
## 1.Mutifactor Model
 


### 1.1  Feature engineering(Factor mining) 
#### Replicate factor from research report
#### some useful link
1. GTJA 191
【研报复现】国泰君安——191个短周期量价特征因子选股系列一 - 知乎  https://zhuanlan.zhihu.com/p/30195354
日频量化因子分类 - 知乎  https://zhuanlan.zhihu.com/p/270265896

2. Alpha 101
数值型因子的大规模分层测试---WorldQuant 101、国泰191、Sundays100+ - 知乎  https://zhuanlan.zhihu.com/p/60872286

#### Research report
https://github.com/Barca0412/Introduction-to-Quantitative-Finance?tab=readme-ov-file

https://github.com/hugo2046/QuantsPlaybook

#### Interesting Paper (Trying use)
1.Generating Synergistic Formulaic Alpha Collections via **Reinforcement Learning**

https://arxiv.org/abs/2306.12964


2.AutoAlpha: an Efficient **Hierarchical Evolutionary Algorithm** for Mining Alpha Factors in Quantitative Investment
https://arxiv.org/abs/2002.08245

### 1.2 Data preprocessing
* Depolarizing data
* Standardization data
* Neutrelizing data
### 1.3 Single factor testing
* Effectiveness(t-value&IC)
* Monotone Stability:Group backtest method

### 1.4  Multi-factor testing

### 1.5  collinearity diagnostics
### 1.6 Factor recombination
* single regression weighting
* IC,RankIC weighting
* Ranknet

### 1.7 Select stock from A share according to our model
#### Based on Machine learning
* Linear Model
* svm
* Lasso regression
* Random Forest
* Xgboost
* Catboost

## 2. Bulid Risk Model

## 3. Portfolio optimization
MAFS 5310 https://bookdown.org/shenjian0824/portr/#structure-of-the-book
* Mean-variance portfolio
* Markowitz portfolio
* Maximum Sharpe ratio portfolio
* Risk based portfolio
...


## 4.Build a Backtesting structure

 #### Useful link for build a Backtesting  structure
- [backtrader](https://github.com/mementum/backtrader)
- [backtrader中文教程](https://github.com/jrothschild33/learn_backtrader)
- [Qlib](https://github.com/microsoft/qlib)
- [QUANTAXIS 2.0.0](https://github.com/yutiansut/QUANTAXIS)
- [QuantLib: the free/open-source library for quantitative finance](https://github.com/lballabio/QuantLib)



## TODO:
### 1. Getting data and data preprocession
* `get_data.py`
* `preprocess.py`
* `data`: To store data

### 2. Build a Backtesting structure and testing simple strategy
* `backtesting.py`
* `simple_backtest.ipynb`；**To test backtest structure**

### 3. Feature engineering
* `GTJA_191.py`
* `Alpha_101.py`
* `Myself_factor.py`
* `factor_data` **To store all factor data**

### 4. Factor testing
* `factor_analysis.py`

### 5. Select stock based on ML
* `ML_selector.py`
### 6. Portfolio optimization
* `portfolio_opt.py`



#### 