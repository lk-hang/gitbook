# Market Beta and Downside Risk

Yaron Levi and Ivo Welch

[TOC]

## Summary

Their research question:

*are all-days market-beta a good measure for stocks' ability to hedge against bear and crash markets?*






## Data Construction

They look at daily stock return from CRSP from 1927 - 2016, on a calendar-year basis. For each year, the estimate the betas by regressing daily returns on the factors. They also apply a few filters, among which:

* individual daily stock returns were winsorized at -25% and 25%
* stock returns were also winsorized at the 2nd and 98th percentiles (within each year)
* Stocks are included if 126 data points are available each year

Stocks are categorized into different beta groups (low, medium and high betas). 

## Analysis

They compare all-days beta with down-beta.

Stock market-down days are betas calculated from down-days $$ \hat{b}^-_{y-1}$$.

