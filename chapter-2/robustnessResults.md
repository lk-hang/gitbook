# Robustness Results

Here I discuss results pertaining to several exercises.

* Why were the *ex-ante* alphas so high?
* no benchmark
* Use S&P 500 stocks (roughly 481stocks per month) as the benchmark rather than the CRSP universe (roughly 5000 stocks per month)[^1].
* Use quarter as an investment horizon rather than a month. 

[^1]:The number of stocks in my exercise is not necessarily 500, because my definition of inclusion in the exercise depends on whether a stock has appeared at least 17 times in a given month. In reality, some stocks are included in the S&P500 in the middle of a month and/or excluded from S&P 500 in the middle of the month, causing these stocks to have less than 17 appearances in a month. 



## Why were the Alphas so high?

The alphas were so high ex-ante, because these were realized returns. The stocks that have highest realized return, would have highest beta (assuming positive market risk premium), but also highest alpha. 

For example, using CAPM as the risk model, we find that the average return for rank = 0 as follows:

* The expected return is 5.51% (The expected excess return equals 5.13%)
* The average MKT factor equals : 0.56

The time-series regression that follows:
$$
E[R_i - R_f] = \alpha_i + \beta_i E[R_m - R_f]
$$
is estimated as:
$$
E[R_i - R_f] = 4.41 + 1.28 * E[R_m - R_f]
$$

Since the empirical mean of $$ R_i - R_f$$ equals 5.13, and the empirical mean of Market Excess Returns equals 0.56, this result shows how CAPM is unable to capture the time-series variation of the rank 0 portfolio correctly. 

See figure below: 

![img1](/images/img1.png)





## No Benchmark

### CAPM as RiskModel (coming later)

### Fama French as RiskModel 

