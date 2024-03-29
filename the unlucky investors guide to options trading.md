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

     ### Table-  Options P/L and probability of profit (POP) statistics 45 days to expiration (DTE) 16 $\Delta$ strangles with six different underlyings, held to expiration, from 2009–2020. Assets include SPY (S&P 500 ETF), GLD (gold commodity ETF), SLV. 
     | Asset | Underlying | Average Profit | Average Loss | POP |
     | --- | --- | --- | --- | --- |
     | ETFs | SPY | $160 | –$297 | 82% |
     | ETFs | GLD | $125 | –$424 | 83% |
     | ETFs | SLV | $33 | –$103 | 81% |
     | Stocks | AAPL | $431 | –$1,425 | 76% |
     | Stocks | GOOGL | $1,108 | –$2,886 | 80% |
     | Stocks | AMZN | $1,041 | –$2,215 | 78% |


     可见ETF有高的**POP** 由于他们的波动性低，导致成功的概率会高。 但是，股票**高**的波动性带来大的收益（代价是少许降低的POP）

     其实无论股票或是ETF， 期权价格是和 标的物的价格 有关。
     比如  ：
       same IV, duration and $\Delta$  --> options prices 和 prices 相关。
       ### Table - Two sample options underlyings with the same IV but differing stock and put prices 

      | Option Parameters | Scenario A | Scenario B |
      | --- | --- | --- |
      | Stock Price | $100 | $200 |
      | IV | 33% | 33% |
      | 45 DTE 16 $\Delta$ Put Price | $1 | $2 |

      在情景A中，看跌期权价格为1美元（基础价格的1%）。由于期权定价的高效性，情景B中的空头看跌期权价格也将是基础价格的1%，因为两种资产具有相同的隐含波动率。产品的中立性表明，没有任何一种（流动性）基础资产本质上比另一种更优越，仅仅是不同资产之间存在比例权衡。股票的高风险、高回报性质并不本质上比ETF的相对稳定性更好或更差，但某些资产可能更适合个人交易者。因此，我们可以得出结论，选择基础资产基本上取决于五个主要因素（按重要性排序）：

      - 1.期权市场的流动性   
      - 2.交易的BPR相对于账户规模的大小   
      - 3.基础资产的隐含波动率 
      - 4.每笔交易所需的P/L波动幅度、结束P/L的变化以及尾部风险暴露的大小 
      - 5.所偏好的公司、行业或市场暴露 
        

 3. Choose a Contract Duration

    对于卖期权的合同期限的选择有以下的考量：

    - 短期 （ < 30 天 ）: 由于$\gamma$ 随着接近到期日变大， P/L 也会**变化**很大，这是不希望看到的。另外，在选择同样的$\Delta\的price strike 时候，会太靠近当前股价，从而跟容易受$\gamma$的影响。
    - 长期  ( > 60 天 ）: P/L 是不会波动很大，但是占用 Buy Power， 不利于资金的利用。
    - 中期 （ 30 < DTE < 60 天 ） ：
       + 作为卖方，要反复交易以提高交易次数，从而令profit更接近**统计意义的优势**。
       + 如果有选举，财报等事件， 一般会令IV 升高，这是可根据事件性质选择DTE. 短期事件，就选短一些的期权卖， 长期事件，就选DTE长的。 
      
 4. Choose defined or Undefined Risk

    - Defined  <- 适合小账户，初学者
      + 风险有限，占用的资金（BPR） 少，P/L 在存续期内波动不大
      + 但是POP 低， 潜在的收益也低，由于多条腿，开关仓的成本也高
     
    - **Undefined**  <-  推荐
      + 风险无限，占用的资金（BPR） 大，P/L 在存续期内波动大
      + 但是POP高， 潜在的收益也高。         

    -   卖期权的资金分配

        |   | Undefined Risk Allocation |   defined Risk Allocation |
        | --- | --- | --- |
        | 占用可用资金 | > 75% | < 25 % |
        | 每笔的BPR占总资金| < 7%  | < 5% | 

        例子 ：  Portfolio allocation for defined and undefined risk strategies with a **$100,000** portfolio at different VIX levels.
         
        | VIX Level | Maximum Portfolio Allocation | Minimum Undefined Risk Allocation | Maximum Defined Risk Allocation |
        |-----------|-------------------------------|----------------------------------|-------------------------------|
        | 20        | $30,000                      | $22,500= *$30,000 x 75 %* ($7,000 = *$100,000 x 7%* max BPR per trade) | 7,500 ($5,000 max BPR per trade)   |
        | 40        | $50,000                      | $37,500 ($7,000 max BPR per trade) | $12,500 ($5,000 max BPR per trade) |

     
 5.  Choose a Directional Assumption  - 推荐 中性 如 **short strangle** 或者 **Iron Condor**

        ### Table - Examples of popular short options strategies with the   same $\Delta$ of approximately **20**,  $\Delta$ = 16 for Short Strngle and $\Delta$ = 10 for long leg of Iron Condor 

        | Strategy          | Composition                              | Defined or Undefined Risk | Directional Assumption | POP   |
        |-------------------|------------------------------------------|---------------------------|------------------------|-------|
        | Naked Option      | Short OTM put                           | Undefined                 | Bullish                | 80%   |
        |                   | Short OTM call                          | Undefined                 | Bearish                | 80%   |
        | Vertical Spread   | Short OTM put, long further OTM put     | Defined                   | Bullish                | 77%   |
        |                   | Short OTM call, long further OTM put    | Defined                   | Bearish                | 77%   |
        | Strangle          | Short OTM put, short OTM call           | Undefined                 | Neutral                | 70%   |
        | Iron Condor       | Short OTM vertical call spread,         | defined                          |    Neutral                    |   60%    |
        |                   | short OTM vertical put spread           |                |                        |       |
     
     - Iron Condor 宽度的选择

       ### Table Statistical comparison of 45 DTE 16𝛥 SPY iron condors with different wing widths, held to expiration from *2005–2021*. Wings that have a smaller $\Delta$ are further from ATM compared to wings with a larger $\Delta$. Included are 45 DTE 16𝛥 SPY strangle statistics held to expiration from *2005–2021* for comparison   
      | 16𝜟 Iron Condor Statistics (2005–2021) | | | |16𝜟 Strangle Statistics (2005–2021) |
      | --- | --- | --- | --- | --- |
      | Statistics | **5𝜟 Wings** | 10𝜟 Wings | 13𝜟 Wings | 2005-2021 |
      | POP | **79%** | 75% | 73% | ${\color{green}81}$% | 
      | Average P/L | **$35** | $15 | $6 | ${\color{green}$44}$ |
      | Standard Deviation of P/L | **$251** | $132 | $74 | ${\color{green}$614}$ |
      | Conditional Value at Risk (CVaR) (5%) | **−$771** | −$399 | −$220 | ${\color{green}−$1,535}$ |

     宽的iron Condor Win !!!   
      + 盈利更多 （ **35** ） 
      + POP更大 （ **79%** ）。这意味着**胜率**更高

      **short Strnagle** 有最大的POP 和 P／Ｌ．　但风险和 BPR 也大。  

     ### Table - Average BPR comparison of 45 DTE 16𝛥 SPY strangles and 45 DTE 16𝛥 SPY iron condors with 10𝛥 wings when held to expiration using data from 2005–2021.

      | VIX Range | Strangle BPR | Iron Condor BPRa |
      | --- | --- | --- |
      | 0–15 | $3,270 | $363 |
      | 15–25 | $2,641 | $426 |
      | 25–35 | $2,261 | $585 |
      | 35–45 | $1,648 | $553 |
      | 45+ | $1,445 | $615 |

     **策略**
     ```
     - Low IV 时候  -> Short width wing Iron Condor,另外，由于低的BPR，则可以占用多一些的资金。
     - When IV 变高 -> 转 去 Short Strangle 策略， 利用它的高收益和高POP。
     ```  
     
 6.  Choose a $\Delta$

     ## Table 1 - Statistical comparison of 45 DTE SPY strangles of different deltas, held to expiration from 2005–2021.
        | Statistics | 16𝜟 | 20𝜟 | 30𝜟 |
        | --- | --- | --- | --- |
        | POP | 81% | 76% | 68% |
        | Average P/L | $44 | $49 | $54 |
        | Standard Deviation of P/L | $614 | $659 | $747 |
        | CVaR (5%) | −$1,535 | −$1,673 | −$1,931 |


     ## Table 2 - Average BPRs of 45 DTE SPY strangles with different deltas, sorted by IV from 2005–2021.
       | VIX Range | 16𝜟 | 20𝜟 | 30𝜟 |
       | --- | --- | --- | --- |
       | 0–15 | $3,270 | $3,366 | $3,573 |
       | 15–25 | $2,641 | $2,756 | $3,014 |
       | 25–35 | $2,261 | $2,415 | $2,794 |
       | 35–45 | $1,648 | $1,715 | $2,058 |
       | 45+ | $1,445 | $1,421 | $1,520 |


     ## Table 3 - Probability of incurring a loss exceeding the BPR for 45 DTE SPY strangles of different deltas, held to expiration from 2005–2021.
      | Strangle Delta | Probability of Loss Greater Than BPR |
      | --- | --- |
      | 16𝛥 | 0.90% |
      | 20𝛥 | 0.93% |
      | 30𝛥 | 1.0% |
     
     **策略**
     
     ```当IV增加时，关闭现有头寸并重新开仓，使用调整后的行权价更好地反映新的波动率条件是一个好的做法。``

# Chapter 6 Managing Trads
` 研究对于short options 策略， 如何管理仓位，如止盈，止损等
  主要讨论在期权到期前，如何关掉仓位。 
  1. 提前关掉仓位的策略是基于一下几点
      - 早关仓，可以提高交易次数。卖期权的edge是统计意义上的，这需要大样本才能体现。一个仓位如果久期太长，那可以交易的次数也会下降。
      - 早关仓，可以提高资金的利用率。让一个仓位占用的BPR可以多用几次。
      - 早关仓，可以降低$\gamma$风险。越接近到期日，标的物的价格可能会大大影响当前的利润。
     
      
   
  2. 方法一  按固定好的**时间**关仓

      - 好处是，好操作（类似于机械操作)，资金周转率可测，尤其适合DTE比较长的合同。虽然DTE后程，利润实现的更多，更快。但是尾部事件可能会造成灾难。
      - 距离到期日多久关仓比较好呢？
    
      ## Table - Statistics for 45 DTE 16𝛥 SPY strangles from 2005–2021 managed at different times in the contract duration. Average P/L is ${P/L / Credit}$
 
      | Management DTE | Probability of Profit (POP) | Average P/L | Average Daily P/L | P/L Standard Deviation | Conditional Value at Risk (CVaR) (5%) |
      | --- | --- | --- | --- | --- | --- | 
      | 40 DTE | 67% | 2.3% | $0.23 | 73% | –206% |
      | 30 DTE | 73% | 10% | **$1.75** | 88% | –212% |
      | 21 DTE | 79% | 21% | **$1.60** | 96% | –283% |
      | 15 DTE | 78% | **25%** | $1.51 | 105% | –304% |
      | 5 DTEa | 82% | **33%** | $1.34 | 185% | –514% |
      | Expiration | 81% | 28% | $1.29 | 247% | –708% |
    
     **策略**
     
     ```Trade-off 是 DTE/2 关仓，比如上表中的 21 DTE， 有高的 Average Daily P/L， 有利于资金周转和提高交易次数，而79%的利润也相当不错```


  3. 方法二  按固定**止盈目标**关仓

     就是如果仓位提前到达一定比例的（25%,50%...%75, 100%) 利润点，就止盈。 否则就等到期权到期。 
     ## Table - Statistics for 45 DTE 16𝛥 SPY strangles from 2005–2021 managed at different profit targets. If the profit target is not reached during the contract duration, the strangle expires. The final row includes statistics for 45 DTE 16𝛥 SPY strangles managed around halfway to expiration (21 DTE) as a reference.
 
      | Profit Target | POP | Average P/L | P/L Standard Deviation | Probability of Reaching Target | CVaR (5%) |
      | --- | --- | --- | --- | --- | --- |
      | 25% or Exp. | 96% | 11% | 191% | 96% | −522% |
      | 50% or Exp. | 91% | 16% | 236% | 90% | −654% |
      | 75% or Exp. | 84% | 22% | 245% | 80% | −699% |
      | 100% (Exp.) | 81% | 28% | 247% | 52% | −708% |
      | **21 DTE** | **79%** | **21%** | **96%** | N/A | **−283%** |

      Remark:
      这个策略普遍有**高**的 P/L Standard Deviation，可见该方法的P/L 波动太大。 25%的止盈虽然有高一些的POP,可是Average P/L太低了，不值得。


      ## Table - Average daily P/L and average duration for the contracts and management strategies described in Table 6.2.
       | Profit Target | Average Daily P/L Over Average Duration | Average Duration (Days) |
       | --- | --- | --- |
       | 25% or Exp. | $1.75 | 15 |
       | 50% or Exp. | $1.67 | 24 |
       | 75% or Exp. | $1.49 | 34 |
       | 100% (Exp.) | $1.29 | 44 |
       | 21 DTE | ${\color{green}$1.60}$ | 24 |


     **策略**
     + defined risk position ( 像iorn condor )  -> 可以应用 50% 或更低的比例 为止盈点。这背后的逻辑是， defined short positions 本身的特性就决定了 P/L 波动不大，就是说到达高盈利的机会不大，是缓慢的实现盈利的。所以，低一些的止盈目标有利于早些时候关仓，从而实现有效资金利用。
     + Undefined risk position ( 如上表的short strangle ), 波动大，提高一些止盈点如 50% - 75%, 到达的可能比有保护的策略大多了。所以值得提到止盈点，以期提高一下单次交易的利润值，当然这可能要令仓位多留一些时间。  
      
  4. 方法三  按固定**止损目标**关仓

     就是如果仓位提前到达一定比例的（-50%,-100% ... -300%, -400%)，就止损。 否则就等到期权到期。
     可是这样容易由于股价的波动，早早推出。而大多数的股票是可以涨回的，这样会大大降低盈利的可能。
     ## Table - Statistics for 45 DTE 16𝛥 SPY strangles from 2005–2021 managed at different loss limits. If the loss limit is not reached during the contract duration, the strangle expires. The final two rows reference other management strategies for comparison.

      | Loss Limits       | POP  | Avg P/L | P/L Standard Deviation | Prob. of Reaching Target | CVaR (5%) |
      |-------------------|------|---------|-----------------------|--------------------------|-----------|
      |  −50% or Exp.      | 58%  | 21%     | 90%                   | 40%                      | −168%     |
      | −100% or Exp.     | 69%  | 25%     | 110%                  | 25%                      | −238%     |
      | −200% or Exp.     | 76%  | 27%     | 131%                  | 13%                      | −338%     |
      | −300% or Exp.     | 79%  | 27%     | 149%                  | 8%                       | −450%     |
      | −400% or Exp.     | 79%  | 27%     | 160%                  | 6%                       | –536%     |
      | None (Exp.)       | 81%  | 28%     | 247%                  | N/A                      | −708%     |
      | 21 DTE            | 79%  | 21%     | 96%                   | N/A                      | −283%     |
      | 50% Profit or Exp.| 91%  | 16%     | 236%                  | 90%                      | −654%     |

      Remark:

      - 降低盈亏标准差和异常风险：采用较低的止损阈值，如-50%，相比持有期权合约直至到期日，可以减少极端损失和波动性的潜在风险。这可以提供更加可控的风险管理方法。

      - 更常见的损失：采用较低的止损阈值，损失更有可能发生，因为期权经常达到这一阈值。然而，值得注意的是，许多仓位可能在到期前恢复，这意味着止损可能导致过早退出仓位。

      - 尾部风险和突然的市场变动：尽管止损有助于限制损失，但它并不能完全消除超过设定阈值的可能性，原因可能是突然的隐含波动率扩张或基础价格的显著变动等因素。这些事件可能导致比预期更大的损失，并导致交易在计划止损水平之外关闭。

      - 中间止损的实际可行性：一个更实际的止损阈值可能至少为-200%。这意味着采用更宽松的止损水平以应对潜在的市场波动，并避免因临时价格变动而出现过早退出的情况。

      - 盈利潜力和尾部风险：相比在期权到期时持有，持有期间通常具有更大的盈利潜力和更大的亏损潜力。然而，在合理的盈利目标上管理可能涉及更高水平的尾部风险。在确定适当的退出策略时，平衡盈利潜力、损失控制和风险承受能力是至关重要的。

      - 与其他管理策略的结合：在更活跃的交易场景中，止损通常与其他管理策略结合使用。这种方法允许交易者使用多种工具和技术根据市场情况和个人交易目标调整仓位。
    
     **策略**
     
     ```-200% 作为止损点```


  5. 综合比较

     - 以 short strangle 为例， 按 潜在损失 （ 即 CVaR 和 P/L standard deviation ) 由 **高到低** 排列：
       | 管理策略     | 管理条件                      |
       |-------------|-------------------------------|
       | 1       | 持有至到期日                   |
       | 2       | 在盈利目标在50%至75%之间管理   |
       | 3       | 在亏损限制为-200%时管理        |
       | **4**    | **在距离到期日一半的21天时间点进行管理** |  <- Win !!

     - 多种策略的组合
       例如，假设一位交易员使用45天到期日的16𝛥 SPY short strangle，并希望采用高概率盈利（POP），中等盈亏标准差(P/L dev) 和适度的异常风险管理策略。一种可能的方式是
       以一下两个条件先到者为准
       +  在初始收益(credit) 的**50%**    <- 固定盈利  
       +  距离到期日还有21天              <- 固定时间点
       
       该策略的统计数据如表

     ## Table - Statistics for 45 DTE 16𝛥 SPY strangles from 2005–2021 managed either at 50% of the initial credit or 21 DTE, whichever comes first. Statistics for other strategies are given for comparison and ranked by CVaR.  ``21 DTE or 50% Profit`` 最好。

       
      | Management Strategy     | POP  | Average P/L | Average Daily P/L | P/L Standard Deviation | CVaR (5%) |
      |-------------------------|------|-------------|------------------|-----------------------|-----------|
      | 21 DTE                  | 79%  | 21%         | $1.60            | 96%                   | –283%     |
      | **21 DTE or 50% Profit**    | 81%  | 18%         | ${\color{green}$1.67}$            | **96%**                   | –288%     |  
      | –200% Loss or Exp.      | 76%  | 27%         | N/A              | 131%                  | –338%     |
      | 50% Profit or Exp.      | 91%  | 16%         | $1.67            | 236%                  | –654%     |
      | None (Exp.)             | 81%  | 28%         | $1.29            | 247%                  | –708%     |

     - 策略选择的考量
    
       + 可能的盈利：如果目标是实现更频繁的盈利，通常会以较小的盈利潜力或增加异常损失的风险为代价。换句话说，追求更高的胜率可能需要接受较低的单笔盈利金额或更高的亏损可能性。

       + 大额盈利：如果目标是追求较大的盈利，通常会导致盈利交易的频率降低。在这种情况下，成功交易的发生次数可能较少，但潜在盈利可能更高。然而，这种方法也可能使交易者面临更大的风险，特别是异常损失方面。

       + 小幅亏损潜力：如果优先考虑将重大亏损的可能性降至最低，通常会导致盈利潜力降低或盈利可能性较低。通过优先考虑风险管理并限制亏损的潜力，交易者可能需要接受较小的盈利或采取不太可能盈利的交易设置。


     ## Table - Qualitative comparison of different management strategies.
      | Criteria                   | 21 DTE | 50% or Exp. | –200% or Exp. | Exp. |
      |----------------------------|--------|-------------|---------------|------|
      | Convenience                | Med    | High        | High          | High |
      | POP                        | Med    | High        | Med           | Med  |
      | Per-Trade Loss Potential   | **Low**    | High        | **Low**           | High |
      | Per-Trade Profit Potential | Med    | Low         | **High**          | High |
      | Number of Occurrences      | **Med**    | Med         | Low           | Low  |

      例如

       +  对于 passively（被动型）交易者而言，如果其投资组合可以承受更多的异常风险，那么仅使用止损，其他情况下则将交易持有至到期日，以尽可能提取现有仓位的外在价值可能更有意义。
       +  对于可以承受更多异常风险的 active（积极型）交易者而言，可以将普通仓位管理在固定的盈利目标上，并在到期日前半程关闭风险较高、回报较高的交易。
       +  非常积极型的交易者可以在所有未定义风险合约中，要么在初始收益的50%处，要么在合约期限的一半处进行管理，因为这种方法优先考虑调节异常风险，并实现可能的合理规模的盈利。 这就是上面提到的 ``21 DTE or 50% Profit`` 策略。

     - 重要提示
    
       + 以上的仓位管理策略是针对undefined. 对于有保护的策略，如iron condor， 因为有最大loss的存在，不用考虑提前关仓。
       + 以上策略是长期的回测结果。 但是不同的退出策略在不同时期会有完全不同的P/L。 可以说 和入场时间时候的市场状况，尤其是IV的变化特性，有很大关系。
         例如：
         同样应用 `２１DTE`　退出策略，　**２０２０－２０２１**　就很好， 但是 在**2018 - 2020** 年，就很差。

# Chapter 7 Basic Portfolio Management
 - 资本配置和头寸规模
   建议把资金分成两部分
   + 核心头寸
     - 标的物 ： ETF
     - 资金配额 ： 75% of **可动用资金** （ 25 % when Low IV and 50 % when High IV of 总资产 ）
     - 特点 ： 获利稳定，持续，暴险不大
   + 补充头寸
     - 标的物 ： 各大股票
     - 资金配额 ： 25% of **可动用资金** （ 25 % when Low IV and 50 % when High IV of 总资产 ）
     - 特点 ： 为了参与市场，获利高（因为一般IV 过高，期权的溢价高 ） ，但风险也大
    
       
     ## Table - Statistics for 45 DTE 16𝛥 strangles from 2011–2020, managed at expiration. Included are examples for core and supplemental position underlyings.
      | Position | Underlying | POP | Average Profit | Average Loss | Conditional Value at Risk (CVaR) (5%) |
      | --- | --- | --- | --- | --- | --- |
      | Core | SLV | 84% | $32 | −$88 | −$201 |
      | | QQQ | 74% | $109 | −$183 | −$454 |
      | | SPY | 80% | $162 | −$320 | −$800 |
      | | GLD | 81% | $119 | −$456 | −$1,100 |
      | Supplemental | AAPL | 74% | $425 | −$1,443 | −$4,771 |
      | | GOOGL | 80% | $1,174 | −$2,955 | −$6,593 |
      | | AMZN | 77% | $1,235 | −$2,513 | −$6,810 |
     
 - 资本配置的多样化
   例如
   + 分配不同比例的资金到 ETF， Low IV 和 High IV 资产
   + 配置**不相关**，甚至**负相关**的资产。
   ## Table - The five-year correlation history for the assets through these relationships fluctuate with time over short timescales, they are assumed to remain relatively constant long term.
      | Asset | Symbol | SPY | QQQ | GLD | TLT | AMZN | AAPL |
      | --- | --- | --- | --- | --- | --- | --- | --- |
      | Market ETFs | SPY | $${\color{lightgreen}1.0}$$ | 0.89 | -0.13 | -0.33 | 0.62 | 0.64 |
      | Market ETFs | QQQ | $${\color{lightgreen}0.89}$$ | 1.0 | -0.12 | -0.26 | 0.75 | 0.74 |
      | Low Volatility Assets | GLD | $${\color{red}-0.13}$$ | -0.12 | 1.0 | 0.39 | -0.12 | -0.11 |
      | Low Volatility Assets | TLT | $${\color{red}-0.33}$$ | -0.26 | 0.39 | 1.0 | -0.18 | -0.22 |
      | High Volatility Assets | AMZN | 0.62 | 0.75 | -0.12 | $${\color{red}-0.18}$$ | 1.0 | 0.50 |
      | High Volatility Assets | AAPL | 0.64 | 0.74 | -0.11 | $${\color{red}-0.22}$$ | 0.50 | 1.0 |  
  
      当配置ETF时候，也要考虑将不相关或负相关的ETF组合一下，比如下表, 表示出
      + 单独的SPY或QQQ会令总头寸面临比较大概率的损失( ~5.8% or 3.9%)
      + 如果是SPY 和 GILD或TLT （见上表，这两个几乎是负相关）组合， 头寸遭受大规模损失的概率会**大大降低**
     ## Table - The probability of outlier losses (worse than 200% of the initial credit) occurring simultaneously for different types of 16𝛥 strangles held to expiration from 2011 to 2020. All contracts have approximately the same duration (45 DTE), open and close dates. The diagonal  entries correspond to the probability of the specific strategy incurring an outlier loss individually, and the off-diagonal entries correspond to the probability of the pair incurring outlier losses simultaneously. Probability of Loss Worse than 200Statistics for 45 DTE 16𝛥 strangles from 2011–2020, managed at expiration. Included are examples for core and supplemental position underlyings.        

      | Asset | SPY | QQQ | GLD | TLT |
      | --- | --- | --- | --- | --- |
      | SPY | **5.8%** | 3.9% | 2.1% | 1.9% |
      | QQQ | **3.9%** | 8.7% | 1.9% | 1.7% |
      | GLD | *2.1%* | 1.9% | 12% | 4.8% |
      | TLT | *1.9%* | 1.7% | 4.8% | 12% |
   
   Remark : 
   ``尽管用不相关的资产多元化来降低损失，是有效果的。但是，还是有可能发生大的损失(如 1.9%), 这就需要让仓位尽可能的小，以希防止意外损失``
   
 - 通过监控**希腊字母**来控制风险

   + Beta-weighted delta (𝛽𝛥)
     由于不同资产的价格是不一样的 ，所以不可以直接将各个头寸的𝛥累加。 但是可以借助个头寸对于**SPY**的𝛽， 通过

     $Total \space \beta\Delta \space = \space \sum\limits_{i=1}^{n} \beta_i \Delta_i \space = \space \beta_1 \Delta_2 + \beta_2 \Delta_3 + ......  + \beta_n \Delta_n$

     **策略**
     令𝛽𝛥保持中性，降低由于市场(SPY)的波动带来的Loss
     
   + Theta(𝜃)  
     $\theta \space ratio \space = \frac{\theta}{ \text{net portfolio liquidity} } $

     它表示，同样的钱（net portfolio liquidity），每天的**Time Decay* 能产生多少利润。
     
     ## Table - Daily performance statistics for five portfolios passively invested in SPY from 2011–2021. Each portfolio has $100,000 in initial capital, and the amount of capital allocated in each portfolio ranges from 25% to 50%.
     
      | SPY Allocation Percentage | Daily Portfolio P/L (2011–2021) |
      | --- | --- |
      | 25% | 0.013% |
      | 30% | 0.015% |
      | 35% | 0.017% |
      | 40% | 0.020% |
      | 50% | 0.025% |

    这个表表示直接投资SPY的每天回报是多少，大概在 **0.013% ~ 0.025%**。 由于卖期权的风险大得多，所以**要求的回报也要多余直接投资SPY**。
    
     - 建议 **0.05% ~ 01.%**  (  $\theta \space ratio$ ),但不能大于 0.2%
     - theta ratio 不能太大的背后逻辑是：
       **𝜃**和**Gamma (𝛤)**是 **正相关的**,高**𝜃**固然利于利润实现，但**Gamma**也会变大，造成仓位的不稳定。如果高**𝜃**存在，则需要再平衡仓位，rolling当前仓位，或直接关了，在在开仓于别的期权。
       
 - DTE多样化
   考虑到期权在临近到期日的时候P/L Dev 会比较大，所以，可以让所以组合有不同的DTE以期望减少单个仓位对整体P/L的影响。 但是这种策略很难回测和量化

 - 期权策略的多样化
   可以建立有保护的期权和裸期权的混合仓位，这样会在 **P/L**和**风险**中达成trade-off. 如下表中Combined 组合会在2020下跌中少一些损失

   ## Table - Statistical analysis of the three portfolios first four statistics (POP, average P/L, standard deviation of P/L, and conditional value at risk (CVaR)) gauge portfolio performance during more regular market  conditions (2005–2020). The final column gives the worst-case drawdown from the 2020 sell-off (the cumulative losses from February to March 2020).

      | | 2005  | - |- | 2020 | 2020  Sell-off |
      | --- | --- | --- | --- | --- | --- |
      | Portfolio Type | POP | Average P/L | Standard Deviation of P/L | CVaR (5%) | Worst-Case Drawdowns |
      | Strangle | 76% | $379 | $1,803 | -$5,174 | -$77,520 |
      | **Combined** | 75% | $221 | $1,275 | -$3,648 | -$45,080 |
      | Iron Condor | 67% | $64 | $799 | -$2,324 | -$12,640 |

 - 根据 **POP** 进行头寸平衡
   根据凯莉公式 ：
   + expected change in bankroll after one play is given by ``pb − q``
 ```math   
   e^{rt}-1 \approx rt =  pb - q
```
   + Optimal fraction of the bankroll to allocate to this trade
```math   
   b = \frac{rt+q}{p}=\frac{1+rt}{p}-1
 ```  

 ```math
    f = p - \frac{q}{b} = p - \frac{1-p}{\frac{1}{p}(1+rt)-1 }
 ```

 ```math
    f = r\cdot t\cdot \frac{p}{1-p} 
 ```

 ```math
    f = r\cdot\frac{DTE}{356}\cdot\frac{POP}{1-POP} 
 ```

   如果按照这个凯莉公式来安排资金分配，有如下的回测比例
   ## Table - POPs and allocation percentages of buying power for 45 DTE 16𝛥 SPY, QQQ, and GLD strangles from 2011–2018. 


   | Symbol | POP | Allocation Percentages |
   | --- | --- | --- |
   | SPY Strangle | 79% | 1.4% |
   | QQQ Strangle | 73% | 1.0% |
   | GLD Strangle | 84% | 1.9% |

   总的来说，这些分配百分比相当低，因为凯利准则主张进行许多小的、不相关的投注。当试图分配25%到50%的投资组合购买力时，严格遵守这些投注大小有些不切实际；因为没有足够的不相关的基础资产。无风险利率的价值为理想的资本配置提供了保守估计，因此扩大这些百分比并采取更积极的方法是合理的。为了在不违反资本配置指南的情况下扩大这些百分比，可以使用这些投注大小作为启发式方法来估计资本配置的比例，而不是明确的百分比。例如，与其按照POP权重分配，更启发式的方法如下：

   + According to initial estimates, 1.4% of portfolio buying power should be allocated to SPY strangles and 1.9% to GLD strangles.
   + Dividing by 1.9, these weights correspond to a ratio of approximately 0.74:1.0.
   + This means that SPY strangles should occupy roughly 0.74 times the portfolio buying power of GLD strangles.
   +  If the maximum per-trade allocation of 7% goes toward GLD strangles,then approximately ``5.2% (derived from 0.74 × 7% = 5.2%)  `` should be allocated to SPY strangles.

   继续这个例子，假设分配给SPY窄幅和QQQ窄幅的资本进一步分裂。虽然这些基础资产是相关的，但在这些头寸之间分配资本比将整个5.2％分配给一个基础资产实现了更多的多样化。这个过程也可以使用POP权重来估计： 
   +  根据初步估计，应将1.4％的组合购买力分配给SPY窄幅，1.0％分配给QQQ窄幅。
   +  通过2.4％（从1.4％+1.0％）进行划分，这些权重对应于大约0.58：0.42的比率。
   +  这意味着SPY窄幅应占资本分配的58％，QQQ窄幅应占42％。
   +  如果最多可以分配5.2％的头寸，则组合资本的3.0％应用于SPY窄幅，2.2％应用于QQQ窄幅。


- **例子** （多种策略一起考虑）
   + 步骤1：使用过去的数据确定适当的基础资产。核心头寸应具有适度的P / L标准偏差和良好的多元化基础资产。ETF，例如下表中的ETF，是核心头寸基础资产的可行候选者。尽管市场ETF高度相关，但足够数量的不相关和反相关资产可以实现合理的特异性风险降低。
   ## Table -  Correlations between different ETFs from 2011–2018. Included are two market ETFs (SPY, QQQ), a gold ETF (GLD), a bond ETF (TLT), a currency ETF (FXE - Euro), and a utilities ETF (XLU).  

   | Sector | Symbol | SPY | QQQ | GLD | TLT | FXE | XLU |
   | --- | --- | --- | --- | --- | --- | --- | --- |
   | Market ETFs | SPY | 1.0 | 0.88 | -0.02 | -0.44 | 0.16 | 0.49 |
   | Market ETFs | QQQ | 0.88 | 1.0 | -0.03 | -0.36 | 0.12 | 0.35 |
   | Diversifying ETFs | GLD | -0.02 | -0.03 | 1.0 | 0.19 | 0.34 | 0.08 |
   | Diversifying ETFs | TLT | -0.44 | -0.36 | 0.19 | 1.0 | -0.03 | -0.04 |
   | Diversifying ETFs | FXE | 0.16 | 0.12 | 0.34 | -0.03 | 1.0 | 0.18 |
   | Diversifying ETFs | XLU | 0.49 | 0.35 | 0.08 | -0.04 | 0.18 | 1.0 |


   + 步骤2： 计算应分配给每个头寸的投资组合资本的百分比。这些百分比可以使用上面的方程，并根据前一节中描述的方法进行缩放，如表8.4所示。 表8.4中显示的核心头寸具有高POP，具有适度的P / L标准偏差，并且具有良好的多元化基础，分配金额低于每笔交易购买力的7％上限。 分配给短期溢价的总投资组合购买力占30％，足以满足此回测的最低25％。使用2011年至2018年初的数据初始化投资组合后，现在可以在2018年初至2019年底的新数据上进行回测，但请记住，此测试不考虑动态管理或隐含波动率
   ## Table -  Core position statistics for 45 DTE 16𝛥 strangles from 2011–2018. The allocation ratio is the allocation percentages normalized such that the largest bet size is set to 1.0. The portfolio weights are determined by multiplying the allocation ratio by 7% (the maximum per-trade allocation percentage). The adjusted portfolio weights show how portfolio capital is split across assets that are highly correlated.

   | ETF | POP  | allocation Percentages |
   | --- | --- | --- |
   | SPY Strangle | 79% | 1.4% |
   | QQQ Strangle | 73% | 1.0% |
   | GLD Strangle | 84% | 1.9% |
   | TLT Strangle | 78% | 1.3% |
   | FXE Strangle | 83% | 1.8% |
   | XLU Strangle | 81% | 1.6% |
  
   | Weights | SPY/QQQ :  GLD : TLT : FXE : XLU |  
   | --- | --- |
   | Allocation Ratio | 0.74:1.0:0.68:0.95:0.84   |
   | Portfolio Weights | 5.2% : 7.0% : 4.8% : 6.7% : 5.9% |
   | Adjusted Portfolio Weights | 3.0% : 2.2% : 7.0% : 4.8% : 6.7% : 5.9% |

    + 回测结果：
   ## Table -  Portfolio backtest performance statistics for the three portfolios described in Figure 8.3 from 2018–2019
   | Portfolio Type | POP | Average P/L | Standard Deviation of P/L | Worst Loss |
   | --- | --- | --- | --- | --- |
   | SPY Equity | 60% | $285 | $2,879 | −$6,319 |
   | Equal-Weight | 67% | $26 | $2,440 | −$6,117 |
   | POP-Weighted | 67% | $268 | $1,610 | −$3,561 |

  
  **where**
  Portfolio performance of three different portfolios from early 2018 until September of 2019. Each portfolio has $200,000 in initial capital with 30% of the portfolio capital allocated. This initial amount of $200,000 allows at least one trade for each type of position, as $100,000 in initial capital does not.
   - The 30% SPY equity portfolio (a) has 30% allocated to shares of SPY.
   - The 30% equally-weighted strangle portfolio (b) has 5% allocated to each of the six types of strangles
   - 30% POP-weighted portfolio (c) has the 30% weighted according to the percentages in Table 8.4.
       
  All contracts have the same delta (16𝛥),  identical durations (roughly 45 DTE), and the same open and close dates. For the sake of comparison, the trades in the equity portfolio are opened on the first of each month and closed at the end of each month.


   有趣的是，上表显示，尽管股票组合的尾部敞口小于期权组合，但股票组合是三个组合中波动性最大、经历最大最坏情况回撤的。基于POP加权的组合表现更加稳定，每次交易标准差显著低于其他两个组合，每次交易的POP与等权重组合相匹配，平均盈亏与股票组合相当。尽管基于POP加权的组合由未定义的风险策略组成，但在回测期间，其盈亏变动性和最坏情况损失几乎只有股票组合的一半。等权重跨式组合的表现也不如基于POP加权的组合，尽管与股票组合的相似组合相比，其盈亏变化或严重回撤并没有更多。再次强调，通过根据市场波动性增加分配比例（可以通过添加不相关的短期权头寸来实现）或者纳入更复杂的管理策略，可以进一步优化两种跨式组合的表现。尽管如此，这个简化的回测说明了资本分配、多样化和基于POP加权分配等风险管理技术的影响。基于凯利准则得出的POP 1−POP 启发式提供了一个很好的指导，可以在初始化组合时确定应该分配多少资本给一个交易，表明应该将更多的资本分配给更高的POP交易，将较少的资本分配给不太可靠的交易。然而，这种方法并没有为动态组合管理提供一个全面的结构。在不同的时间点，交易经常达到盈利或亏损目标，需要重新定位执行价格，或者提供新的机会。交易员可以通过选择相同的合同期限或管理策略来简化复杂的管理过程


# Chapter 8 Binary  Events
 - 二值事件会有以下
   + 公司财报公告（促使盈利交易）
   + 公司财报公告（促使盈利交易）
   + 新产品发布
   + 石油市场报告
   + 选举
   + 美联储关于整个市场的公告

  

 ![IV indexes for different stocks from 2017–2020 AMZN ](https://github.com/merlionfire/Notebook/blob/main/image/AMZN_IV_around_earnings.png)
 ![IV indexes for different stocks from 2017–2020 AMZN ](https://github.com/merlionfire/Notebook/blob/main/image/AAPL_IV_around_earnings_IV_around_Earnings.png)
 - 二值事件普遍有
   + 事件之前， IV **膨胀**
   + 事件之后， IV **收缩**
 

 - 想通过在事件之前， 卖出高溢价的期权，事件之后快速盈利的想法是不现实的。因为IV高是有原因的，事件出现后的市场反应是**不可预估的**. **极有可能**标的物在事件出来之后，走出Expected Move（尽管高IV造成很宽的范围）范围。 从而对short策略的期权仓位，造成极大的损失。 可买期权也赚不到钱，压错方向不说，高昂的期权费也出的赚到的利润大大折扣。

 - 但是二值事件也有非常有利于交易的属性
   + 发动，结束时间比较短，意味着交易的获利的时间短，有利于资金的效率
   + 高风险意味着高回报，高手视为赚大钱快钱的良机
   + 需要跟仓，动态调仓。有利于初学者学习期权调仓技术。
    
 - 3个大科技股的二元事件的统计结果 ：

   ## Table :　Statistics for 45 days to expiration (DTE) 16𝛥 AAPL strangles from 2005–2020. Trades are opened the day before an earnings report and closed either one, five, 10, or 20 days after earnings.
   | Day Position Is Closed Relative to Earnings | POP  | Average P/L | Standard Deviation of P/L | Conditional Value at Risk (CVaR) (5%) |
   |--------------------------------------------|------|-------------|---------------------------|--------------------------------------|
   | **Day After**                                  | 72%  | ${\color{green}$85}$         | $203                      | –$405                                |
   | 5 Days After                               | 70%  | $43         | $400                      | –$1,027                              |
   | 10 Days After                              | 61%  | $60         | $408                      | –$1,025                              |
   | 20 Days After                              | 56%  | ${\color{red}–$34}$        | $660                      | –$1,976                              |
     
  
   ## Table :　Statistics for 45 DTE 16𝛥 AMZN strangles from 2005–2020. Trades are opened the day before an earnings report and closed either one, five, 10, or 20 days after earnings.

   | Day Position Is Closed Relative to Earnings | POP  | Average P/L | Standard Deviation of P/L | CVaR (5%) |
   |--------------------------------------------|------|-------------|---------------------------|-----------|
   | **Day After**                              | 65%  | ${\color{green}$99}$         | $803                      | –$1,927   |
   | 5 Days After                               | 65%  | $85         | $842                      | –$2,154   |
   | 10 Days After                              | 72%  | $1          | $1,446                    | –$4,416   |
   | 20 Days After                              | 76%  | ${\color{red}$78}$         | $1,540                    | –$4,477   |


   ## Table : Statistics for 45 DTE 16𝛥 GOOGL strangles from 2005–2020. Trades are opened the day before an earnings report and closed either one, five, 10, or 20 days after earnings.
   | Day Position Is Closed Relative to Earnings | POP  | Average P/L | Standard Deviation of P/L | CVaR (5%) |
   |--------------------------------------------|------|-------------|---------------------------|-----------|
   | **Day After**                                  | 75%  | ${\color{green}–$60}$       | $1,320                    | –$4,639   |
   | 5 Days After                               | 67%  | –$113      | $1,358                    | –$4,724   |
   | 10 Days After                              | 65%  | –$122      | $1,275                    | –$3,675   |
   | 20 Days After                              | 71%  | ${\color{red}–$2}$        | $1,584                    | –$4,909   |
 
   通过上面的表格，可以得出投机二值事件的准则

   + 由于波动太大，需要用更小的资金投机二值事件。一般是是平常投资股票标的物期权的一半资金。
   + 最好是季报之前开仓，季报之后马上关仓。 不要让期权保留太久，上表可见留得越久，损失越大。


# 总结
 1.  隐含波动率（IV）是从金融保险的供求关系中衍生出来的市场风险情绪的代理。当期权价格上涨时，IV上升；当期权价格下降时，IV下降。IV反映了未来价格变动的预期幅度，而不具有方向性。它还可以用来近似资产的一个标准差预期价格范围（尽管这并未考虑行权价格的偏斜）。芝加哥期权交易所波动率指数（VIX）旨在跟踪标准普尔500指数的IV，并被用作衡量整个市场风险的代理。VIX和所有波动率信号一样，被认为会在显著扩张后回归下降，这表明一些统计学上的有效性，因此一旦波动率膨胀， 可以对波动率的下行方向进行假设。
 2.  与买期权策略相比，卖期权费策略可以获得更一致的盈利并具有长期统计优势。获得一致盈利的代价是面临大额且有时是未定义的损失风险，这就是为什么卖期权费交易者的两个最重要的目标是实现足够的一致盈利来弥补中等但更有可能的损失，并构建一个能够承受不太可能的极端损失的投资组合。
 3.  卖期权策略的盈利能力取决于具有大量的交易次数，以达到正向的统计平均值，这是大数定律和中心极限定理的结果。至少需要大约200次交易的发生，才能使策略的平均盈亏（P/L）趋于长期的盈利目标，而更多次数则更好。
 4.  卖期权头寸的极端亏损是非常不太可能发生的，但通常发生在基础资产价格波动较大而预期波动范围较窄（低隐含波动率）的情况下。因为在低隐含波动率下发生大幅价格波动是罕见且难以可靠地建模的，减少这种风险暴露的最有效方法是在隐含波动率升高时进行卖期权交易。
 5.  尽管高波动率环境对于卖期权头寸来说是理想的，但卖期权头寸在所有波动率环境中都具有较高的盈利概率（POP）和一定的统计优势。此外，由于波动率大部分时间都较低，因此在所有隐含波动率环境中交易卖期权策略可以使交易者更加稳定地获利，并增加交易次数。在采用这种策略时，为了管理异常风险的暴露，保持较小的仓位规模和限制分配给卖期权头寸的资本量至关重要，尤其是在隐含波动率较低时。通过根据当前市场情况调整分配给卖期权头寸的资本量，可以进一步改进这种策略。
        | VIX Range | Maximum Portfolio Allocation |
        |-----------|-------------------------------|
        | 0–15      | 25%                           |
        | 15–20     | 30%                           |
        | 20–30     | 35%                           |
        | 30–40     | 40%                           |
        | 40+       | 50%                           |
 6. 购买力减少（BPR）是放置和维持期权交易所需的投资组合资金量。买期权的BPR仅仅是合约的成本，而卖期权的BPR旨在包含交易所交易基金（ETF）标的资产至少95%的潜在亏损和股票标的资产90%的潜在亏损。BPR用于按交易评估卖期权风险，有两种方式：BPR是对未定义风险头寸的最坏情况亏损的相当可靠的度量，BPR用于确定一个头寸是否适合投资组合，基于其购买力。已定义风险的交易不应占据超过投资组合购买力的5%，未定义风险的交易不应占据超过7%，对于小账户可以有例外。BPR的公式复杂且特定于策略类型，但卖跨式期权的BPR大约是标的资产价格的20%。BPR可用于比较同一策略的风险变化（例如，标的资产A的卖跨式期权与标的资产B的卖跨式期权），但不能用于比较具有不同风险配置的策略的风险（例如，标的资产A的卖跨式期权与标的资产A的 iron condor 期权）。
   
 7. 交易者根据个人的盈利目标、风险承受能力和市场观点进行交易，但一般来说，了解以下内容是良好的实践：
   + 只交易具有流动期权市场的标的资产，以最小化流动性风险。选择标的资产在某种程度上是随意的，但选择一个风险水平适当的标的资产非常重要。股票标的资产往往比ETF标的资产风险更高、回报更高。这意味着股票标的资产更频繁地提供高隐含波动率（IV）的机会，但它们也具有更多的尾部损失风险，并且交易成本更高。
   + 选择一个对购买力的有效利用，允许一致性，提供合理的交易次数，整个期间具有可管理的盈亏波动，并且具有适度的期末盈亏变动性的合约期限。30至60天的期限适合大多数交易者。
   +  与已定义风险交易相比，未定义风险交易具有更高的盈利概率（POP）、更大的盈利潜力、无限的下行风险和更高的购买力减少（BPR）。高盈利概率的已定义风险交易（例如，宽铁蝶式期权）与未定义风险交易具有相似的风险特征，同时还能提供对极端损失的保护。与未定义风险交易相比，这样的交易更适合低隐含波动率条件，并允许占用未定义风险的投资组合资金。
   + 具有较高增量（delta）的合约相比较具有较低增量的合约更具风险，但也有更高的回报潜力。在交易期权费时，考虑10𝛥到40𝛥之间的合约，这个范围足够大，可以实现合理的增长，但也足够小，以便在整个期间内具有可管理的盈亏波动和期末盈亏变动性。

8. 在选择管理策略时，需要考虑的主要因素包括便利性和一致性、资本分配偏好、期望的交易次数、每笔交易的平均盈亏以及每笔交易的风险暴露。提前管理的头寸的每笔交易盈亏较低，但尾部风险较小，相比持有至到期的头寸。因为提前管理还可以容纳更多的交易次数，并在每天的平均盈亏上更高，所以在到期前平仓并将资金重新配置到新的头寸通常比从现有头寸中提取更多价值更有效地利用资本。

   + 如果根据剩余到期日（DTE）来管理，考虑在合约期限的中点左右关闭交易，以实现相当数量的长期盈利并证明尾部损失风险的合理性。
   + 如果根据盈利目标来管理一个未定义风险的头寸，选择一个介于初始信用的50%至75%之间的目标，可以获得合理的盈利同时减少异常损失的潜在程度。选择过低的盈利目标会降低平均盈亏，而选择过高的盈利目标对减轻异常风险的作用不大。已定义风险头寸的盈利目标可以较低，因为它们通常波动性较小。
   + 如果结合不同策略，通常在未定义风险的合约中，在初始信用的50%或合约期限的一半左右进行管理，可以获得合理、稳定的盈利，并降低异常风险的程度。
   + 如果采用止损策略，至少要有一个中等范围的止损阈值，例如初始信用的-200%。如果止损过小（例如-50%），由于期权的盈亏波动较大，亏损的可能性更高，尽管它们通常会恢复。还需要注意的是，在价格快速波动的情况下，止损并不能保证最大亏损，因此除非进行被动交易，否则通常将止损与另一种管理策略相结合。止损策略通常不适用于已定义风险的策略。
  
9. 遵守资本分配准则对于限制尾部风险并实现合理的长期增长至关重要：
   + 分配给卖期权头寸（如卖跨式期权和卖铁蝶式期权）的投资组合购买力应根据当前市场波动性的情况，范围在25%至50%之间，其余的资本可以保留为现金或低风险的被动投资。[参考要点5]。
   + 在分配给卖期权的资本中，至少75%应保留用于未定义风险交易（单个头寸不得分配超过投资组合购买力的7%），最多25%应保留用于已定义风险策略（单个头寸不得分配超过投资组合购买力的5%）[参考要点6]。
   + 一般而言，分配给卖期权的资本中最多25%应用于补充头寸，即用于市场参与的高风险、高回报交易工具。其余部分应用于核心头寸或具有较高盈利概率和适度盈亏变动性的交易，以提供稳定的盈利和合理的异常风险暴露。
  
10. 将期权投资组合的标的资产进行多样化（即交易一系列相关性较低的资产）是投资组合风险管理中最重要的多样化工具之一，特别是对于异常风险管理。策略多样化和期限多样化虽然不像标的资产多样化那样重要，但也是其他简单的风险管理技巧。
11. 希腊字母指标构成了一组用于量化期权暴露的风险度量标准。每个合约都有自己特定的希腊字母指标集合，但某些希腊字母指标可以在具有不同标的资产的头寸之间进行相加。因此，这些度量指标可用于总结投资组合的各种风险来源并指导调整。 两个关键的希腊字母指标是β加权Delta (𝛽𝛥) 和Theta (𝜃)。β加权Delta代表一个头寸相对于某个指数的定向暴露量，而不是相对于标的资产本身。Theta代表一个期权每天预期的价值下降量。β加权中性的投资组合对投资者具有吸引力，因为它们对市场的定向波动相对不敏感，并从隐含波动率和时间的变化中获利。
12. 由于卖期权交易者持续从时间衰减中获利，各个头寸的总theta值可以可靠地估计卖期权投资组合的每日预期增长。期权投资组合的最低theta比率（𝜃投资组合/净流动性）应在0.05%至0.1%之间，并且不应超过0.2%，因为这表示风险过大。如果投资组合未达到这些theta比率的指导原则，则应按以下方式调整头寸：

   + 如果一个适当分配、多样化的投资组合是β加权中性的，但提供的theta值不足够，那么应重新评估投资组合中的头寸。在这种情况下，可以考虑用未定义风险交易替换一些已定义风险交易，或将未定义风险头寸滚动至更高的增量。还可以添加新的增量中性头寸，例如卖跨式期权和`iron condor`期权。隐含波动率和theta也具有高度相关性，这意味着如果theta值过低，可以考虑使用更高的隐含波动率标的资产。如果投资组合在β加权中性的同时具有过多的theta风险，则可以采取相反的措施。

   + 如果theta比率过低（<0.1%），而投资组合不是β加权中性的，则应重新平衡或收紧现有头寸，或增加新的卖期权头寸。

      + 如果β加权Delta (𝛽𝛥) 过大且为正（看涨），则应增加新的负β加权Delta头寸（例如，在正β标的资产上卖出认购期权，或在负β标的资产上卖出认沽期权）。

      + 如果β加权Delta (𝛽𝛥) 过大且为负（看跌），则应增加新的正β加权Delta头寸（例如，在正β标的资产上卖出认沽期权）。

   + 如果theta比率过大（>0.2%），而投资组合不是β加权中性的，则应重新平衡或扩大现有头寸，或移除卖期权头寸。

      + 如果β加权Delta (𝛽𝛥) 过大且为正（看涨），则应移除正β加权Delta头寸（例如，在正β标的资产上卖出认沽期权）。

      + 如果β加权Delta (𝛽𝛥) 过大且为负（看跌），则应移除负β加权Delta头寸（例如，在正β标的资产上卖出认购期权）。

   + 如果适当分配、多样化的投资组合提供了足够的theta，但不是β加权中性的，则应重新评估现有头寸。例如，可以关闭或重新平衡具有偏斜性的头寸，或用提供相当数量theta的新的增量中性头寸来替换它们。

13. 二元事件交易，如在季度财报公布期间进行的交易，应谨慎对待，只占用闲置的投资组合资本，并且其头寸规模应保持异常小。二元事件交易必须经过仔细监控，并且通常在比较短的时间尺度内进行，相比更典型的交易来说。它们通常在二元事件前一天开仓，二元事件后一天平仓。
