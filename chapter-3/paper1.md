#  Market Timing

Paulo Manoel

<u>The research question</u>: 

**Do funds that bet on risk factors (i.e. beta strategies) create values?** 



## Summary

Manoel argues that the current performance measure of mutual funds (i.e. the total tracking error) is not a good measure of whether mutual funds are in active betters on risk factors (or betas).

His argument is that TEV is really composed of two factors, one that measures 

1. idiosyncratic volatility (alpha-strategies)
2. timing volatility (beta-strategies)

Specifically, given a portfolio $$P$$ at time $$t$$, the insights of the paper come from decomposing the TEV (the standard deviation of the difference between the portfolio returns and the benchmark returns) as follows:
$$
\begin{align}
TEV_{Pt} 
&= \sqrt{\text{var}_t[R_{Pt} - \beta^*_p f_{t+1}]} \\
&= \sqrt{\text{var}_t[(\beta_{Pt} - \beta_{P^*})^T f_{t+1} + \varepsilon_{t+1}]}
\end{align}
$$
Manoel argues that if we use *timing volatility*, defined as 
$$
\sqrt{\text{var}_t[(\beta_{Pt} - \beta_{P^*})^T f_{t+1}}
$$
we will be better able to measure how active funds are in beta-investing. TEV is not a good measure of value-creation by beta-strategies, because it tends to be overloaded/dominated by the second component, which measures bets on idiosyncratic risk:
$$
\sqrt{\text{var}_t[\varepsilon_{t+1}]}
$$
He proceeds to categorize funds using TVol only, where high TVol funds are funds that are active in beta-strategies, whereas low TVol funds are funds with typically low active bets on betas, and show that high TVol funds outperform low TVol funds, with a return performance of 29 basis points.