# Gamma_Trading

In this project, we engage in simulating the outcomes of a portfolio comprising delta-hedged call futures options. 
The primary driving force behind these speculative trades is the disparity between one's estimated volatility and the market-implied volatility. 
A pertinent question arises: what volatility should we employ for computing delta and initiating the delta hedge?

In the first scenario, we assume that the true volatility surpasses market volatility, and we employ the latter to compute delta. 
As depicted in the plot below, the cumulative profit exhibits a consistent positive trajectory, albeit with occasional deviations due to discrete hedging.

![case1](https://github.com/WuYenSun/Gamma_Trading/blob/main/gamma_trading01.png)


Upon closer examination, we identify instances where cumulative Profit and Loss (PnL) remains relatively flat in the second half of the simulation. 
This phenomenon is often linked to futures prices diverging significantly from the strike price, reducing gamma and daily PnL.

![case1_flat](https://github.com/WuYenSun/Gamma_Trading/blob/main/gamma_trading02.png)


In the second scenario, we again assume that the true volatility surpasses market volatility, but this time, we employ the former to compute delta. 
As evident in the plot below, the cumulative profit follows a positive trajectory, but with more pronounced fluctuations. 

![case2](https://github.com/WuYenSun/Gamma_Trading/blob/main/gamma_trading03.png)


In the final scenario, we delve into the idealized world of Black-Scholes (1976), assuming equal volatility for all factors. 
As portrayed in the plot below, the cumulative PnL distribution closely aligns with zero. 
This outcome serves to validate the effectiveness of the Nobel Prize-winning idea - dynamic hedging.

![case3](https://github.com/WuYenSun/Gamma_Trading/blob/main/gamma_trading05.png)


Lastly, we scrutinize sample points where daily PnL experiences abrupt spikes. 
We find that such occurrences are typically linked to futures prices closely aligning with the strike price, an impending maturity date, or a combination of both, resulting in a significantly elevated gamma. 
Consequently, daily delta hedge strategies may falter in such scenarios, leading to sharp fluctuations in daily PnL.

In summary, the above results illustrate the crucial role of gamma in shaping the performance of the hedged option portfolio, a key reason why this trading strategy is often referred to as gamma trading. 
Additionally, it's worth noting that the performance in the first case tends to be less volatile compared to the second case. 
As a practical approach, delta is typically computed using the market implied volatility. 
The key takeaway is that achieving profitability in gamma trading hinges on accurately estimating true volatility relative to the market. 
The choice of delta computation method primarily influences how smoothly you can earn the premium.
