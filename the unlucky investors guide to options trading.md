# Chapter 3 Short Options

-  卖期权的风险最大来自IV由低转高的短暂过程。而一旦IV高了起来，市场会消耗这种高IV，这时建仓的风险会大大降低。
-  卖期权的长期盈利效果是通过大量的小额的交易才能体现。 这和赌场的庄家一样，极小的edge是通过限制单次下注额度，利用大量的次数来体现的。     
   + 如果交易数太少  -> 则偏差很大，即 可能赚很多， 有可能赔的很多
   + 如果每次数额大  -> 会由于小概率时间而赔光。 
   + 但是提高交易次数是不容易的。因为卖期权是找高IV时候建仓，以提高成功率。但是， 以SPY为例， 高IV 只占很小比例， 如：
   

        ### Table   VIX Data ( 2005 - 2021 ) 
        | VIX Range   | % of Occurrences |
        |----------|-------------:|
        | 0-15 |  43% | 
        | 15-25 | 40% | 
        | 25-35 | 11% |
        | 35+ | 6% |
        
 -  为了提高交易次数，不得不在低IV时候，也建仓。下表表示低IV 也可以盈利。

      
       ###  Table  SPY Strangle Data ( 2005 - 2021 ) 
       | VIX Range   | Pob of Profit | Average P/L |
       |----------|-------------:|:------------|
       | 0-15 |  82% |  $20 |
       | 15-25 | 78% |  ${\color{darkred}$7}$ |  
       | 25-35 | 86% |  $159 |
       | 35+ | 89% | $255 |      
       
   + 但是资产配置要和IV  ${\color{green}正相关}$.
   
      * IV 低  $\rightarrow$ 资产配置比例少，但不少于 $`{25 \%}`$. 否则收益过少。
      * IV 高或者变高的过程  $\rightarrow$ 资产配置比例加大，但不超过 $`50 \%`$， 以防曝险。
      * 分配给短期权保费的资金也不应过于集中于单个头寸。一个适当规模的头寸不应占据超过投资组合资金的**5%**至**7%**  


           ###  Table Guidelines for allocating portfolio capital according to market IV. 
           | VIX Range   | Max Portfolio Allocation|
           |----------|-------------:|
           | 0-15 |  25% |  
           | 15-25 | 30% | 
           | 25-35 | 35%  |
           | 35+ | 50% |

   + 提前关闭仓位的好处 
      - 避免 $\gamma$ 风险。
        越接近到期日，期权越受到股价异动的影响，即 $\gamma$ 随着接近到期日变大，提前关仓可以避免在期权整个久期的后半程，受到波动的影响。  
      - 由于时间短了，则可以提高资金效率，从而**提高交易次数**  
        ###  Table SPY Strangle Statistics (2005–2021)
        | Statistics                     | Held to Expiration | Managed at **21** DTE |
        |--------------------------------|-------------------|------------------|
        | POP                            |       81%         |       79%        |
        | Average P/L                    |       $44         |       $30        |
        | Average Daily P/L              |     $1.29         |     $1.60        |
        | Standard Deviation of P/L      |      $614         |      ${\color{green}$260}$        |
        | CVaR (5%)                      |     –$1,535       |     ${\color{green}–$695}$        |
        
# Chapter 4 Buy Power Reduction ( BPR )
 1. 在当前市场条件下，BPR 作为一个相当可靠的度量标准，用于未定义风险头寸的最坏情况损失。
 2. BPR 用于确定一个头寸是否适合具有特定购买力的投资组合
  
 3. 当隐含波动率（IV）较高时，卖出高溢价期权头寸带来更高的收入和更大的利润潜力，但是保证金比例（BPR）的降低也使得可以开设更多的卖出高溢价期权头寸，相较于IV较低时。由于每笔交易的平均盈利和亏损（P/L）更高，并且可以开启更多潜在盈利头寸，因此在高IV条件下，为高波动率情况保留较大比例的投资组合购买力非常重要。这也进一步证明，随着IV的增加，将投资组合资金的比例分配给卖出高溢价期权的BPR是合理的。这些关键的高IV利润提升了投资组合的表现，同时也为潜在的未来损失提供了保护。历史数据显示，当VIX超过40时，与VIX低于15相比，同等资本量可以覆盖大约两倍数量的16𝛥 SPY捆式多空期权组合的BPR。考虑到投资组合分配指南，这两种波动率环境下允许的卖出高溢价交易数量的差异更大。  

     Table Here's the table converted to Markdown format:

   | Scenario | A | B | C |
   | --- | --- | --- | --- |
   | Stock Price | $150 | $150 | $300 |
   | Call Strike | $160 | $175 | $320 |
   | Put Strike | $140 | $130 | $280 |
   | Call Price | $1 | $2 | $2 |
   | Put Price | $1 | $2 | $2 |
   | BPR | $2,000 | $1,750 | $4,000 |
   | IV | 20% | 45% | - |
   
   Please note Scenario B where IV > IV of A, but BPR < BPR 0f A due to width strike width due to High IV

  Table - Two portfolios with the same net liquidity but different amounts of
market volatility, using SPY strangle data from 2005–2021.

   Sure! Here's the table converted into Markdown table format:

   | Scenario           | A             | B             |
   |--------------------|--------------|--------------|
   | Net Portfolio Liquidity | $100,000      | $100,000      |
   | Current VIX            | > 40         | < 15         |
   | Portfolio Allocation  | $50,000       | $25,000       |
   | Approx. 16𝛥 SPY Strangle BPR | $1,500        | $3,300        |
   | Max Number of Strangles | 33           | 7            |

 Note : 
 -----
 需要注意的是，风险购买力比率（BPR）可以用于比较**同类型策略**的风险资本，但不能用于比较明确定义风险策略和未定义风险策略之间的风险。
 
 例如，
 -----
 + 如果交易基础资产为A的空头跨式期权所需的资金占比（BPR）是交易基础资产为B的空头跨式期权所需BPR的两倍，并且其他参数相同，    
    -> 我们可以得出结论，A的风险是B的两倍。这是一个有效的比较，因为我们正在考虑两个具有相同风险配置的交易，
 +. 但是BPR不能用于比较具有不同风险配置的策略（例如，空头跨式期权与空头看跌期权），因为它没有考虑到利润概率或承担大额损失的概率等因素。

 理解BPR在从期权理论过渡到实际期权交易时至关重要，因为它对应着交易空头期权的实际资本需求。
 
 
4. BPR也是讨论期权的资本效率（期权杠杆）的必要条件。
    例如:
    ----
    考虑一只股票以100美元的价格交易，并且波动率为20%，假设一个交易员希望以看涨的方向做多这个资产。交易员可以通过下面的示例中展示的几种不同方式来获得对这个基础资产的看涨方向敞口。
     
      Table  -  Example trades that offer bullish directional exposure. Assume that the 50𝛥 (ATM) call and put contracts have 45 DTE durations and cover 100 shares of stock.
    

      | Strategy               | Capital Required | Max Profit | Max Loss | Probability of Profit (POP) |
      |------------------------|------------------|------------|----------|-----------------------------|
      | 50 Shares of Long Stock| $5,000           | ∞          | $5,000   | 50%                         |
      | Long 50𝛥 Call         | $280             | ∞          | $280     | 30%                         |
      | Short 50𝛥 Put         | $2,000 (BPR)     | $280       | $9,720   | 60%                         |
      
      
      期权杠杆的效应是明显的，
      
      * 因为多头认购头寸与多头股票头寸相比，风险资本减少了94% ( $5000 -> $280 ) ，但获得了相同的盈利潜力。
      * 空头认沽头寸可能会亏损初次投资的数倍，但具有比多头股票头寸更高的可能性盈利（POP = 60%），且需要较少的资本（减少60% -> $2000 vs $ 5000）。
