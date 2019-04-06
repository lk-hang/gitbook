# Data Description and Construction
## Sample Selection

My sample data is the daily data from the whole universe of CRSP, ranging from 1970-Jan to 2018-Dec. To filter the stocks, I apply the following common rules. I  include a stock if it has appeared at least 17 times for a given month in the CRSP database. Only ordinary common shares are included (`shrcd in (10, 11)`), if it is listed on NYSE, AMEX, or NASDAQ (`exchcd in (1, 2, 3)`), when the number of outstanding shares `shrout`, stock price `prc`, and returns `ret`  are not missing. Market cap for each month $$t$$ is calculated as the daily price $$ \times $$ number of outstanding shares of month $$ t  - 1$$. Finally, I collect daily Fama-French factors for each month.

## Implementation Details

I obtain $$\lambda_i$$ for each stock in each month by solving the portfolio optimization. Note that $$\lambda_i$$ is either $0$ or larger than $0$, by the KKT condition. I repeat the exercise for both CAPM and Fama French. The portfolio optimization is a quadratic programming problem and can be solved with a Goldfarb/Idnani dual algorithm `quadprog`. 

For each stock-month pair, I run the following regression the daily stock return and the daily factors to obtain the stock betas $$ \beta $$:
$$
E[r_i - r_f] = \beta'F + \varepsilon_i
$$




