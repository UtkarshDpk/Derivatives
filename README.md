# Derivatives
This project is a case studies of derivatives viz., *Future Contracts* and their application in one of the three different types of trading viz., *Hedging* as well as the operations of *Margin Accounts* of Futures for the daily settlement of profits. This Daily settlement is one of the key roles of the exchange to maintain margin account on both sides of the trasaction.

## Scenario

Given a historical dataset of prices of GLD and Futures contracts, we want to hedge the delivery of the underlying asset GLD by using Futures contracts as well as calculate net profit earned for the given period.

1. ### Hedging.pdf
    Shows the application of Futures contracts which are primarily traded on exchanges to hedge the risk of the underlying asset which in this case is GLD. 

    SPDR Gold Trust (GLD), the largest, most popular gold ETF, is an investment fund that holds physical gold to back its shares. The share price tracks the price of gold, and it trades like a stock, but the vast majority of investors don’t have a claim on the underlying gold. The reason for this is that you can only request physical delivery of metal if you own a minimum of 100,000 GLD shares (most investors don’t: at $1,000 gold, 100,000 shares is more than a million dollars. Even if you do own enough shares, the GLD ETF reserves the right to settle your delivery request in cash.

    Given the day of the hedge to be 60<sup>th</sup> day, we use correlation coefficient and standard deviations of the two variables to calculate the **Optimal Hedge Ratio**. An optimal hedge ratio (also called minimum-variance hedge ratio) is a ratio that tells us the percentage of our asset or liability exposure that we should hedge. Since futures contracts are never 100% effective as hedging instruments, businesses aiming to use them for risk coverage purposes use the optimal hedge ratio formula to select the most appropriate futures contract and the number of contracts needed to protect the full extent of the company asset or liability. It equals the product of the correlation between the prices of the hedging instrument and the hedged instrument and the volatility of the hedged instrument divided by the volatility of the hedging instrument. An optimal hedge ratio is most relevant where the characteristics of the hedged instrument and the hedging instrument are different i.e. in a cross hedge. 
    
    This information can be used to provide a better estimate of the number of contracts a company should use to hedge their position, such that any loss in the spot market is more exactly matched by the gain on the contracts.

    In our case we are given the optimal number of contracts to be 100. So we can calculate number of GLD shares we can hedge.

2. ### Margin Accounts.pdf
    
    When a futures hedge is set up the market is concerned that the party opening a position by buying or selling futures will not be able to cover any losses that may arise. Hence, the market demands that a deposit is placed into a margin account with the broker being used – this deposit is called the **Initial Margin**. These funds still belong to the party setting up the hedge but are controlled by the broker and can be used if a loss arises. Indeed, the party setting up the hedge will earn interest on the amount held in their account with their broker. The broker in turn keeps a margin account with the exchange so that the exchange is holding sufficient deposits for all the positions held by brokers’ clients. The gain or loss is calculated on a daily basis and credited or debited to the margin account as appropriate. This process is called **Marking to Market**.
    
    Having set up the hedge and paid the initial margin into their margin account with their broker, the company may be required to pay in extra amounts to maintain a suitably large deposit to protect the market from losses the company may incur. The balance on the margin account must not fall below what is called the **Maintenance Margin**. When these extra funds are demanded it is called a **Margin Call**. The necessary payment is called a **Variation Margin**. If the company fails to make this payment, then the company no longer has sufficient deposit to maintain the hedge and action will be taken to start closing down the hedge.

    We start on April 20th 2017. We purchase five futures contracts (each 100 ounces) for the delivery of 500 ounces of GLD. Therefore, our daily gain is 500 times the change in futures price of one ounce. The initial margin is 5 x $6000 = $30,000. A margin call will happen when our initial margin falls below $22500 which is the maintenence margin. Our initial bank balance is $1,000,000. We put up $30,000 initial margin, so the bank will be $970,000 at the end of day one.