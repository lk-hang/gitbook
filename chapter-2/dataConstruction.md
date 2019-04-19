# Data Description and Construction
[TOC]

## Sample Selection

My sample data is the daily data from the whole universe of CRSP, ranging from 1970-Jan to 2018-Dec. To filter the stocks, I apply the following common rules. I  include a stock if it has appeared at least 17 times for a given month in the CRSP database. Only ordinary common shares are included (`shrcd in (10, 11)`), if it is listed on NYSE, AMEX, or NASDAQ (`exchcd in (1, 2, 3)`), when the number of outstanding shares `shrout`, stock price `prc`, and returns `ret`  are not missing. Market cap for each month $$t$$ is calculated as the last observed daily price $$ \times $$ number of outstanding shares of month $$ t  - 1$$. Finally, I collect daily Fama-French factors for each month. This results in a stock-day pair of 60,469,901 observations.

## Implementation Details

I obtain $$\lambda_i$$ for each stock in each month by solving the portfolio optimization [see](<https://www.lkhang.com/chapter-1/motivation#problem-formulation>). Note that $$\lambda_i$$ is either $0$ or larger than $0$, by the KKT condition. I repeat the exercise for both CAPM and Fama French. The portfolio optimization is a quadratic programming problem and can be solved with a Goldfarb/Idnani dual algorithm `quadprog`. 

To solve the quadratic programming problem, I require specification of $$\mu, \Sigma, b$$. I use the following procedure.

### Expected Return

For each stock-month pair, I run the following regression using the daily stock return and the daily factors to obtain the $K \times 1$-vector stock betas $$ \hat{\beta}_i $$:
$$
E[r_i - r_f] = \beta_i'F + \varepsilon_i
$$
To obtain the expected return $\mu$, we simply use: $$ \hat{\beta}_i' F$$.

### Return Covariance

To obtain the return covariance matrix $$\Sigma = B\Sigma_F B' + diag(\sigma_{\varepsilon, 1}^2,..., \sigma_{\varepsilon_{1,N}^2})$$, I calculate covariance matrix of the daily factors of that month, returning, $$\Sigma_{F, t}$$. $$B$$ is the $N \times k$ factor loading matrix, estimated in the linear regression above for each month, and $$\sigma_{\varepsilon_i}^2$$ is estimated with its corresponding mean-squared error.

### Benchmark Weights

For my first exercise, I use the whole CRSP universe as a benchmark. To do so, I use the corresponding market capitalization of each stock as the benchmark weight. 

Subsequent exercises would involve more realistic benchmarks, such as the S&P 500.

- [x] Paulo mentioned that Thompson-Reuter Mutual Funds data can be found from `/wrds/tfn/sasdata/s12/s12`

### Risk Aversion

We have a free parameter risk aversion $$ \gamma $$. which captures the trade-off between expected return and tracking error. We will set $$ \gamma $$ between 0.25 to 1. Setting $$ \gamma $$ to 5 (or a large number is not good, **WHY?**).To understand the role of $$ \gamma $$ in our problem, consider the two limit cases.

* $$ \gamma \to 0 $$. In this case, our problem becomes:

$$
\max_a \quad a'\mu \\
  a'1  = 0 \\
   -b \leq a
$$

Assuming CAPM, this implies that stocks with high beta are overweighed while stocks with low beta stocks are underweighted relative to the benchmark. Thus, the short-sale constraints are active for negative expected returns  When $$ \gamma \to 0$$ , the tracking error essentially disappears in the objective function.

* $$ \gamma \to \infty $$ . 

$$
\max_a \quad a'\mu - \frac{1}{2} \gamma a'\Sigma a \\
  a'1  = 0 \\
   -b \leq a
$$

The optimal portfolio in this case is: $$ a^* = 0 $$. That is, none of the constraints are binding, and the portfolio manager will mimic the benchmark/index exactly (by holding the market portfolio exactly).

## Portfolio Construction

Once we obtained the cost of shorting, we create portfolios that are long high cost of shorting (large $$ \lambda $$) and portfolios that are short low cost of shorting ($$ \lambda$$ close or equal to 0). For each month, we sort stocks according to $\lambda$ and assign them to a bin according to its rank relative to other stocks. I will default to a quintile portfolios, that is, I choose 5 bins for my exercise (rank 5 equals large $$ \lambda $$, and rank 1 equals small $$\lambda$$ ). To create the portfolios, we first buy-and-hold each stock to calculate the monthly return of each stock. Within each quintile portfolio, we then value-weight each stock in that portfolio using the market cap of that stock from the previous month. This results in 5 portfolios sorted by $$ \lambda $$.



