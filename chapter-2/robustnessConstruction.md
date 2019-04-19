# Robustness Checks

## No Benchmark

First, I solve the portfolio optimization problem of an agent that does not aim to maximize her return (and minimize her 

tracking error) relative to a benchmark. In this setup, her problem becomes:
$$
\begin{align} \max_{w}  \quad & w'\mu - \frac{1}{2}\gamma w' \Sigma w \\
\text{s.t.} \quad & w'e = 1 \\
& 0 \leq w \quad (\lambda)
\end{align}
$$
We similarly extract the shadow cost of shorting $$(\lambda)$$ given a risk model (i.e. CAPM or FF3) that specifies $$ \mu$$ and $$\Sigma$$. This can be easily done (as before) using the ``quadprog``routine in Python.

## S&P 500 as the benchmark

My original exercise uses the CRSP universe (on average 4990 stocks per month). The returns are not winsorized in any way, and stocks are included only if they appear 17 times or month per month, and has non-missing, non-zero, market cap at the end of each month. 

I access S&P 500 listings through `/wrds/crsp/sasdata/a_indexes/DSP500LIST`, which can be merged with CRSP. `DSP500LIST` shows the date a stock is first (and last) listed on S&P500. Note that the number of stocks in my exercise is not necessarily 500, because my definition of inclusion in the exercise depends on whether a stock has appeared at least 17 times in a given month. In reality, some stocks are included in the S&P500 in the middle of a month and/or excluded from S&P 500 in the middle of the month, causing these stocks to have less than 17 appearances in a month. 

## Quarterly Investment Horizon

In this exercise, an agent solves the portfolio optimization problem using data from the last quarter (Say 2018Q4), form a buy-and-hold portfolio for the current quarter (say 2019Q1), where the benchmark weights are from the last month of the previous quarter (Dec 2018). Stocks are included if it has appeared at least 50 times in a quarter, where the market cap in the last month of each quarter is non-zero, or non-missing.

