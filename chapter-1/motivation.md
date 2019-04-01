# Introduction

## Introduction 

In recent years, more funds (ETFs, Mutual Funds) have been pursuing a portfolio strategy that tracks (mimics) a predetermined benchmark. Examples include:


- S&P 500 capturing Large Caps
- S&P Small Cap  600 Index, capturing small companies in the range of $400 million to $1.8 Billion as of 2017
- Russell 1000 Index  (an index of the 1,000 largest companies in the US)
- Russell 2000 Index (the bottom of the 2,000 stocks in the Russell 3000 Index)


Managers are typically evaluated on the basis of their performance against the benchmark. They choose their active portfolio where they aim to mimic the performance of the benchmark. For example, the Information Ratio measures the measurement of portfolio returns in excess of the benchmark return (i.e. index return), while at the same time minimizing the tracking error. If all funds perform a factor investing, using factor modeling (such as CAPM, FF3, FF4, or FF5), then most of these funds get similar views on return expectations and return covariances. Mathematically, the funds are solving the following mathematical problem:
$$
\begin{align}
\max_a \quad & a'\mu - \frac{1}{2} \gamma a'\Sigma a \\
& a'1  = 0 \\
& -b \leq a
\end{align} \\
$$

