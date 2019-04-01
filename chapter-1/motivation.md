# Introduction

## Problem Formulation 

In recent years, more funds (ETFs, Mutual Funds) have been pursuing a portfolio strategy that tracks (mimics) a predetermined benchmark. Examples of these benchmarks include:


- S&P 500 capturing Large Caps
- S&P Small Cap  600 Index, capturing small companies in the range of $400$ million to ​$1.8 billion as of 2017 
- Russell 1000 Index  (an index of the 1,000 largest companies in the US)
- Russell 2000 Index (the bottom of the 2,000 stocks in the Russell 3000 Index)

Managers are typically evaluated on the basis of their performance against the benchmark. They choose their active portfolio where they aim to mimic the performance of the benchmark. For example, the Information Ratio measures the measurement of portfolio returns in excess of the benchmark return (i.e. index return), while at the same time minimizing the tracking error. If all funds perform a factor investing, using factor modeling (such as CAPM, FF3, FF4, or FF5), then most of these funds get similar views on return expectations and return covariances. 

One constraint that all these funds share is the inability to short assets. A portfolio manager constructs a portfolio, with portfolio weights $$(w_1, ..., w_N)$$ with the constraint that: $$ 0 \leq w_i$$, and $$\sum_{i=1}^N w_i = 1 $$ . The fact that this short sale constraint exists limits portfolio managers to short assets for which they have a negative view (or opinion). However, since these managers are rewarded by their performance relative to a chosen benchmark, they can still decide to underweight a particular asset in their portfolio relative to the benchmark. Suppose for example that there exists a stock $j$ for which the benchmark weight equals $b_j > 0$. By choosing $w_j < b_j$ the portfolio manager is essentially underweighting this asset. The difference in $w_j$ and $b_j$ is the active weight $a_j = w_j - b_j$, which can be negative when the manager underweights or positive when the manager over-weights asset $j$ in her portfolio. The constraint that $0 \leq w_i$ implies that the active weight can be at most $a = -b_i$ . In the frictionless market, the portfolio manager can select any active portfolio, and could express her view by choosing $a = -1$ for example. However, the short-sale constraint limits portfolio managers to take this view.

Mathematically, the funds are solving the following mathematical problem:
$$
\begin{align}
\max_a \quad & a'\mu - \frac{1}{2} \gamma a'\Sigma a \\
& a'1  = 0 \\
& -b \leq a
\end{align} \\
$$

The solution of this problem can be found [here].



