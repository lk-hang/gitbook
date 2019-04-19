# Margin CAPM 

Nicolae Garleanu and Lasse Pedersen

<u>Research question:</u>

How does margin constraint affect asset returns?

## Summary

When margin constraint binds, price gaps (i.e. base) arise for risky securities of different margin requirements. These price gaps exist in the cross-section and in the time series.

* Cross-sectional : price gaps depend on margin requirement
* Time-series: price gaps depend on shadow cost of capital, which can be measured as collateralized and uncollateralized loans/borrowing

The paper is both an empirical and theoretical exercise.
Theoretically, they find that:

1. CCAPM is augmented by security's marign times the general funding cost
2. basis is due to margin requirements $$ \times $$ funding cost and difference in beta
3. Stocks with high margins have high betas and volatilities during the crises, since these stocks will have large funding liquidity risk
4. funding cost, or the shadow cost of capital, is the interest differential between collateralized and uncollateralized loans. 
5. In bad times, margin constraints bind, leading to lower rates (why?), and to a rise of margin risk premium.

Empirically, they find that:

1. evidence supporting model predictions using the basis between CDS Minus Bond, Investment-grade Minus High Yield
2. evidence from the CIP failure
3. Asset pricing effect from the Fed's lending facilities (What exactly?)
4. Quantify a bank's incentive to perform regulatory arbitrage to loosen capital requirement (??)

# Model

* Agents are heterogeneous risk-averse.

Margin CAPM :
$$
E[r_i] = r_f + \beta_i \times \text{covariance risk premium} + m_i \times \text{margin premium}
$$
Margin premium is the risk premium for the fact that there is margin requirement for an asset, and is positive when the margin constraint is binding, and zero otherwise.

The margin CAPM is nested inside the traditional CAPM. Note that margin CAPM is the same as the CAPM under normal circumstances. Under bad times, however, the margin constraint will bind and the margin premium becomes positive, deviating from the CAPM.

Assets with the same underlying cash flow but different margin requirements can explain the margin premium. As an example, they compare bonds with CDS, arguing that bonds have high margin requirements, but not for CDS. As a result, when the margin constraint binds, the required return is higher for the bond than it is for the CDS, since the 

