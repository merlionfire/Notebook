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


# Chapter 5 Constructing a Trade

   构造期权合约需要的6个步骤
 1. Choose an asset universe.

    - A **high** open interest or volumne across strikes ( > **a few hundred** / strike )
    - A **tight** bid-ask spread ( < $`1 \%`$ of the contract price )
    - A available contract with several strike prices and expiration dates.
   
 2. Choose an Underlying

       Table  - General pros and cons for **stock** and **ETF** 
      | Stocks |  | ETFs | | 
      | --- | --- | --- | --- |
      | Pros | Cons | Pros | Cons |
      | Tend to have options with higher credits and higher profit potentials | Single‐company risk factors | Inherently diversified across sectors or markets | Limited selection compared to stocks |
      | Frequent high implied volatility (IV) conditions | Earnings and dividend risk | Tend to have options with lower BPRs and are still highly liquid | High IV conditions are not common |

    选择标的资产时，交易所需的资本是一个限制因素。单个头寸通常不应占据组合资本的**5%**至**7%**，``这意味着股票标的可能不适合小账户，因为它们的交易成本更高``。
   
    然而，由于在IV升高时**卖出**期权有几个好处，股票标的在某些情况下可能是更好的标的
    - 由于股票面临公司和行业特定的风险，因此它们往往与**ETF**相比具有更高的波动率，并且往往"更容易出现波动率升高的机会"。请注意，如果交易股票期权，投资者还应注意可能推动这些IV膨胀期的上下文信息（例如，盈利报告日期，公司公告），因为它可能会影响策略选择。在使用ETF标的交易期权时，这种做法就不那么重要了
    - 附加的风险因素（加上流动性股票通常比ETF更昂贵的事实）导致股票期权在合同期间通常具有**更大**的**盈利**和**亏损**波动，更多的P / L变化以及更多的尾部风险。如果交易的资本要求不过分，并且基础资产的IV有利，则这些将是考虑的下一个因素。总的来说，"股票期权通常更具风险，但也具有比ETF期权更高的利润潜力"

   
Single‐company risk factors

 3. 


 

 4. 
