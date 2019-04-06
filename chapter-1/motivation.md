# Introduction

## Problem Formulation 

In recent years, more funds (ETFs, Mutual Funds) have been pursuing a portfolio strategy that tracks (mimics) a predetermined benchmark. Examples of these benchmarks include:


- S&P 500 capturing Large Caps
- S&P Small Cap  600 Index, capturing small companies in the range of $400$ million to ​$1.8 billion as of 2017 
- Russell 1000 Index  (an index of the 1,000 largest companies in the US)
- Russell 2000 Index (the bottom of the 2,000 stocks in the Russell 3000 Index)

Managers are typically evaluated on the basis of their performance against the benchmark. They choose their active portfolio where they aim to mimic and/or outperform the performance of the benchmark. One variable to measure the success of the strategies of the portfolio managers is by looking at the information ratio, which measures of portfolio returns in excess of the benchmark return (i.e. index return), standardized by the tracking error, which is the risk difference between the two portfolios. 

One constraint that all these funds share is the inability to short assets. A portfolio manager constructs a portfolio, with portfolio weights $$(w_1, ..., w_N)$$ with the constraint that: $$ 0 \leq w_i$$, and $$\sum_{i=1}^N w_i = 1 $$ . The fact that this short sale constraint exists limits portfolio managers to short assets for which they have a negative view (or opinion). However, since these managers are rewarded by their performance relative to a chosen benchmark, they can still decide to underweight a particular asset in their portfolio relative to the benchmark. Suppose for example that there exists a stock $$j$$ for which the benchmark weight equals $$b_j > 0$$. By choosing $$w_j < b_j$$ the portfolio manager is essentially underweighting this asset. The difference in $$w_j$$ and $$b_j$$ is the active weight $$a_j = w_j - b_j$$, which can be negative when the manager underweights or positive when the manager over-weights asset $$j$$ in her portfolio. The constraint that $$0 \leq w_i$$ implies that the active weight can be at most $$a = -b_i$$ . In the frictionless market, the portfolio manager can select any active portfolio, and could express her view by choosing $$a = -1​$$ for example. However, the short-sale constraint limits portfolio managers to take this view.

Mathematically, the funds are solving the following mathematical problem:




$$
\max_a \quad a'\mu - \frac{1}{2} \gamma a'\Sigma a \\
a'1  = 0 \\
 -b \leq a
$$

## Solution

The problem can be solved intuitively by maximizing the Lagrangian function:
$$
\Lambda(a, \lambda_0, \lambda) = a'\mu - \frac{1}{2} \gamma a' \Sigma a + \lambda_0 a'\mathbb{1} + \lambda' (a + b)
$$
where $$ \lambda $$ is a $$N \times 1$$ vector containing Lagrangian variables. The FOC is:
$$
\mu - \gamma\Sigma a + \lambda_0 + \lambda = 0
$$


with the KKT conditions that $$ \lambda '(a + b)$$ = 0, and $$\lambda \geq 0$	$ .
$$
\lambda = \gamma \Sigma a - \mu - \lambda_0
$$
This condition says that stocks with high shadow costs have lower expected return, or high marginal contribution to risk. 



## Factor Construction

One may wonder what$$\mu, \Sigma$$ in the portfolio optimization problem might be. Suppose that all portfolio managers have homogeneous views on the stocks. Our hypothesis is that If all funds perform some sort of factor investing, such as CAPM, FF3, FF4, or FF5, then most of these funds get similar views on return expectations and return covariances. Suppose these managers agree on CAPM, that is:

$$ \mu_i = E[R_i] = \beta_i E[R_m] $$

and $$\Sigma$$ is constructed as a diagonal matrix with variance defined by:

$$V(R_i) = \beta_i V(R_m) \beta_i + \sigma^2_{\varepsilon,i}$$

On the other hand, if agents agree on a multivariate factor model, such as 3-Factor Fama French model, $$\mu$$ and $$\Sigma$$ are constructed as:

$$\mu = E[R_i] = \beta_1 E[F_1] + \beta_2 E[F_2] + \beta_3 E[F_3]​$$

and 

$$\Sigma = B \Sigma_F B' + diag(\sigma^2_{\varepsilon, 1}, ..., \sigma^2_{\varepsilon, N}) $$

where $$B$$ is a $$N \times k$$ factor loading matrix, and $$\Sigma_F$$ is the $$k \times k$$  covariance matrix of the factors.



