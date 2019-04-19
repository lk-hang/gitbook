# Market Beta and Downside Risk

Yaron Levi and Ivo Welch

[TOC]

## Summary

Their research question:

* are all-days market-beta a good measure for stocks' ability to hedge against bear and crash markets?



All-days market-beta is defined as beta that is measured on all days, whereas down-beta is only measured on days when the stock market declined. 

They show that : 
* all-days market-beta is a better measure than down-beta only for predicting down-beta for the next period.
* the relationship between ex-post down-betas and returns is positive, but the relationship between ex-ante down-betas and returns is negative
* Ex-ante down-betas or plain-betas did not earn a positive risk premium. The positive alpha found in Ang, Chen and Xing (2006) exist because exposure to market premium is omitted. The alpha turns negative once adjusted for market risk premium.

Overall, their evidence is not consistent with a theory of reward for bearing downward risk.

## Data Construction

They look at daily stock return from CRSP from 1927 - 2016, on a calendar-year basis. For each year, the estimate the betas by regressing daily returns on the factors. They also apply a few filters, among which:

* individual daily stock returns were winsorized at -25% and 25%
* stock returns were also winsorized at the 2nd and 98th percentiles (within each year)
* Stocks are included if 126 data points are available each year

Stocks are categorized into different beta groups (low, medium and high betas). 

## Analysis

They compare all-days beta with down-beta.

Stock market-down days are betas calculated from down-days $$ \hat{b}^-_{y-1}$$.

