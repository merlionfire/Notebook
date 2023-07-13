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

     一般
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
       +  非常积极型的交易者可以在所有未定义风险合约中，要么在初始收益的50%处，要么在合约期限的一半处进行管理，因为这种方法优先考虑调节异常风险，并实现可能的合理规模的盈利。 这就是上面提到的 c``21 DTE or 50% Profit`` 策略。

       
