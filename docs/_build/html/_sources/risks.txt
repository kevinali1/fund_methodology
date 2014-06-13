=========================
Calculation of Risks
=========================

In accordance with industry standards, risk data are calculated using the trailing 36 monthly holding  period returns. Valuehorizon calculates two basic risk measures: the volatility of excess returns, and the Sharpe ratio.

Volatility of Excess Returns
===============================

The excess return of a fund in a particular month is the difference between the return on a 90-day risk-free zero-coupon instrument for that month and the holding period return of the fund for that month. Given the 90-day spot rate at the beginning of month t, R90,t the return on a 90-day risk free zero-coupon instrument (also called RF or the “risk free return”) for month t is calculated as:

IMAGE HERE

Thus, given the holding period return of the fund in month t, HPRt, the excess return of the fund for month t, ERt, is calculated as follows:

IMAGE HERE

After the trailing 36 monthly excess returns are calculated for the fund, the volatility of excess returns can be calculated as:

IMAGE HERE

Note that this represents the population standard deviation of monthly excess returns and not the sample standard deviation as evidenced by the use of 36 in the denominator (as opposed to 35).

One limitation of the volatility of excess returns is that is gives equal weighting to positive and negative monthly returns. However, investors are generally more concerned with downside volatility. A number of alternative risk measures have been developed to address this need, such as drawdown and semivariance. Valuehorizon may switch to one of these alternative measures in the future, but continues to use the simple standard deviation due to its popularity, simplicity of calculation and intuitive interpretation.

Sharpe Ratio
===================

Instead of just focusing on returns, investors need to be conscious of the risk and volatility they expose themselves to along the way.

The Sharpe ratio is a measure of risk-adjusted performance and is often described as the reward per unit of variability. It seeks to give a numerical representation of how well the return of an asset compensates an investor given the amount of risk taken. The classic definition of the Sharpe ratio is the mean excess return for the trailing 36 months divided by the volatility of the excess returns over the same time period. 

Mathematically this can be represented as follows:

IMAGE HERE

The Sharpe ratio is usually used as a ranking metric. A higher ratio is desirable since it means that the fund gives a better return for a given level of risk (see limitations below).

Limitations
===================

Historically, risk has always been difficult to quantify. Modern finance theory uses standard deviation as the de facto risk measurement. The underlying idea is that risk can be equated with volatility.

Furthermore, the Sharpe ratio is one of the most common risk/return measures. First developed in 1966 by William Sharpe, it has been met with almost equal amounts of acceptance and criticism. There are two main criticisms of the Sharpe ratio:

1. The returns of an investment may not follow a normal distribution. This is especially applicable to actively managed funds that may employ exotic trading or hedging strategies giving rise to skewness and kurtosis in their returns. These may include strategies with small upside returns and the occasional large negative return (so called Black Swan events), investments in illiquid markets, and serially correlated returns. These strategies give rise to higher Sharpe ratios due to the appearance of low volatility or smoothness of returns.
2. The Sharpe ratio treats positive returns as equal to negative returns. Many analysts believe that this treatment is unrealistic since investors care more about negative returns than positive returns. The Sharpe ratio penalizes both upside and downside equally. For this reason, some analysts prefer to use the Sortino ratio, which uses the downside semi-variance (i.e. the measurement of return variation below a minimal acceptable return, MAR) as a substitute for regular standard deviation in the denominator. Other analysts prefer a weighted semi-deviation. Some analysts defend the Sharpe ratio, stating that the choice of MAR introduces personal bias - different investors will choose different MARs depending on their level of risk tolerance. In addition, the incorporation of positive returns in the Sharpe ratio may be desired since high returns require high risk. Just because a portfolio with high risk gave a positive return does not mean it could not have produced a high (or even disastrous) loss.

Despite these potential limitations, Valuehorizon continues to use the Sharpe ratio due to its simplicity, intuitive interpretation, and ease of calculation/verification. Valuehorizon does not currently use the Sortino ratio, nor does it calculate the downside semi-variance.

There are other alternative risk/return measurements available such as the Jensen’s alpha and Treynor ratio. Both of these measurements are based on the Capital Asset Pricing Model and require relevant benchmarks to compute beta. Valuehorizon does not compute these measurements due to the lack of applicable benchmarks especially in Caribbean markets. Although peer group average benchmarks are produced, they do not satisfy the investability criteria for a relevant benchmark.

Investors should be aware of these both the pros and cons of using the Sharpe ratio as well as the regular standard deviation as a measure of risk. Particular attention should be paid to actively managed portfolios as well as funds invested in illiquid markets.
