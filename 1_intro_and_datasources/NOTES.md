**Link**
[unit 1 repo for slides, notebook and recordings](https://github.com/DataTalksClub/stock-markets-analytics-zoomcamp/tree/main/01-intro-and-data-sources)

**About the data**
* Historical data from [yfinance](https://pypi.org/project/yfinance/), where it's **15 mins delayed data**. Hence we are doing delayed trading simulations instead of live trading simulations.
* We use GDPPOT and CPI. Inflation is removed from GDPPOT to reflect the true economic capacity/output. If inflation is not removed, the increase in prices would cause the economic capacity/output to be **overstated**, causing economic policies and interest rates to be set erroneously.
* Ideally, your money should grow at a rate higher than the CPI, since it means that the amount you pay now for the same basket of goods would be different (usually more) in future. If your money doesn't grow, its value diminishes by time.
* For the key indicators commonly used as references if investing in the US, refer [slides](https://docs.google.com/presentation/d/e/2PACX-1vR_vfIYCpGhgsR_jef9uo5YdKbg68LGO6pZR5kRSrxDTHNRujKgPb7r9K1U1SM9yOFJlC7OoDAAjKHG/pub?start=false&loop=false&delayms=10000).
* Rule of 72: A simple formula to estimate how long it takes for an investment to double, given a fixed annual interest rate: $\text{Time to double (in years)} = \frac{72}{\text{Annual Rate of Return (%)}}$
* Ideally a successful long-term investment strategy is to be higher than a benchmark, the aim is to have:
    * Rolling positive return over 6 - 12 months.
    * 60/40 portfolio (equity/bonds) for risk-averse or passive investment portfolio.
    * Define a sweet spot for long-term returns for yourself, such as in the range of 6-10% per year, inflation-adjusted (corrrected to remove effects of inflation).
* 



**Abbreviations & Acronyms**
* CBO: Congressional Budget Office, a nonpartisan agency of the U.S. Congress that provides budget and economic data and analysis. The CBO releases reports that include projections of spending and revenues, deficits and debt, and economic indicators like GDP.
* GDPPOT: Real potential GDP, an estimate of the output the economy could produce if its capital and labour resources were used at a high rate. Note the data is adjusted to remove the effects of inflation.
* CPI: Consumer Price Index, represents an aggregate of prices paid by urban consumers for a typical basket of goods, excluding food and energy. 
* CAGR: Compound Annual Growth Rate, it measures the average annual growth rate of an investment (or any metric) over a period of time, assuming the profits are reinvested each year. $\text{CAGR}=\frac{\text{Ending Value}^{\frac{1}{n}}}{\text{Beginning Value}} - 1$

