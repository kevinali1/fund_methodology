# Overview of Mutual Funds #

Valuehorizon defines a “mutual fund” as a collective investment scheme that pools investors’ money into a portfolio, manages it, and charges a fee in return. The rules governing the fund’s management, distribution policy, fee structure, investment objectives and risk are documented in its prospectus. The rules governing the fund’s custody and stewardship policies are documented in its trust deed.

A “mutual fund class” is an interest in the portfolio defined by certain specifications. These classes are usually designated by a particular letter eg. “Class A” or “Class B”. The main differences between classes of the same fund usually relate to their expenses, trading currency and minimum investment amount. Each multi-class fund will have a representative “primary class”, which is usually the class with the smallest minimum investment and other entry requirements. As at April 30, 2013, Valuehorizon tracks 69 funds and 83 fund classes. See section 7.0 for the full list.The following is Valuehorizon’s guide for the treatment of mutual fund data and performance measures. It will cover the basic concepts used in mutual fund analysis, as well as the standard methodologies to quantitatively compute the risks and returns of any fund.

## Asset Categories ##
Each fund is associated with an asset category. Valuehorizon determines the asset category for each fund based on the funds investment objectives found in its prospectus. The asset categories are:

* Equity - the fund invests in shares of listed or unlisted companies. The fund may also invest in equity derivatives or other equity funds.
* Fixed-Income - the fund invests in fixed income instruments such as bonds, debentures, loans and annuity-like instruments. The fund may also invest in fixed-income derivatives or other fixed-income funds.
* Real Estate - the fund invests in real property or real estate investment trusts. The fund may also invest in other real estate funds.
* Balanced - the fund invests in a mixture of assets from the three categories above. The fund may also invest in alternative assets.

## Primary Currency ##

Each fund is associated with a primary currency. For single-class funds or multi-class funds with the same trading currency, this will be the trading currency of the fund. For multi-class funds with different trading currencies, this will be the currency with the largest portfolio allocation.

## Peer Groups and Sub-Peer Groups ##

Valuehorizon defines peer group as a group of funds with characteristics that are sufficiently similar to warrant a valid performance comparison. These peer group selection criteria are usually (but not necessarily) related to the following fund characteristics:

* Investment objective;
* Primary currency;
* Asset class;
* Risk/return characteristics.

Sometimes the funds within a peer group may have a wide array of narrowly defined investment strategies. In these cases, Valuehorizon may define an additional sub-peer group to allow a further, more selective comparison.

Valuehorizon reserves the right to change the assigned peer group and sub-peer group of any fund at any time without notice. These changes will be reflected immediately in the online database and in the subsequent issue of the Mutual Fund Journal.

## Fees and Expenses ##

All mutual funds have costs. These may include transaction costs, brokerage commissions, analyst and manager salaries, marketing expenses, legal expenses and accounting expenses. Investors pay for these costs through direct and indirect fees.

Indirect fees include the following:

* Management fees - this is the amount paid to the management firm as compensation for managing the portfolio. This amount is usually a percentage of total fund assets deducted each year.
* Distribution fees - this is the amount paid to cover the distribution and service expense of the fund. It is also usually deducted as a percentage of total fund assets.
* Administrative expenses - these are amounts paid to cover legal expenses, custodial fees, accounting fees, and any other costs related to the administration of the fund.
* These fees are paid for indirectly since they are deducted directly out of the fund assets. Funds quote their daily net asset values after these fees have been deducted. As such, Valuehorizon’s performance metrics are stated net of these fees.

Direct fees include the following:

* Initial Sales Charge (also known as an Entry Load) - this is a fee paid by the investor upon purchasing units in the fund. It is usually charged as a percentage of the amount invested. For example, a person investing $100,000 in a fund with a 5% initial sales charge will have to pay a $5000 fee with the remaining $95,000 available to purchase units.
* Deferred Sales Charge (also known as an Exit Load) - this fee is similar to the initial sales charge in all respects except that it is paid upon exiting the fund.  It is usually charged as a percentage of the amount being withdrawn.
* Trailer Fees (also known as Trailer Commissions) - this is a fee paid to the fund dealer who sells the fund. It is usually paid annually and charged as a percentage value of the investor’s account holdings.

The act of adjusting a fund’s performance to account for direct fees is referred to as load-adjusting. Valuehorizon does not load-adjust any of its performance statistics.

## Units and Net Asset Values ##

Funds are generally traded in “units” or “shares” which can be subscribed (purchased) or redeemed (sold). Funds are described as “open-end” or “closed-end” based on how these units are treated.

An open-end fund is one which can issue and redeem units at any time so that investors can purchase units directly from the fund. Most open-end funds allow ownership of fractional units. 

A closed-end fund is one which is listed on an exchange such that there is a fixed number of units outstanding so that investors must purchase units from other investors via a market.

The actual net asset value per unit of a fund (“NAV”) is defined as the net assets under management divided by the number of units outstanding. It is usually quoted daily in a newspaper of record and/or the fund’s website. Open-end funds operate under one of the following NAV systems:

* Fixed NAVs - the fund fixes its NAV at a predetermined price. This will be the trading price for the life of the fund. Investors receive a return solely through distribution payments. 
* Floating NAVs - the fund calculates and publishes its NAV daily. Investors receive a return through both the distribution payments and capital gains via the unit price. Some funds may quote separate bid and ask NAVs.

A fund’s “price” is either its closing exchange quote (for closed-end funds) or its NAV (for open-end funds). When calculating performance, if a fund switches from and open-end system to a closed-end system (or vice versa), the price according to the definition above will be utilised both before and after the switch.

Some managers of market-listed closed-end funds quote an actual NAV in addition to the fund’s listed trading price. In these cases, Valuehorizon will always use the traded price. If a fund switches its trading currency during its lifetime, the historical prices before the switch will be retroactively converted to the new currency using historical forex rates.

## Forward Filling ##

A common problem experienced by analysts when trying the model financial time-series is how to treat missing data. Although a good quality time-series will have very few missing data points on trading days, it will inevitably have missing data points on holidays, weekends, and other non-trading days. The standard practice is to compute a simple forward-fill. Given a set of quoted NAVs or prices, Qt, the forward-filled price Pt on date (or time) t, ranging from 0 to n, is calculated recursively as follows:

IMAGE HERE

## Distributions ##

Many funds pay investors a distribution according to either a predetermined frequency stated in its prospectus or at the discretion of the fund manager. Each distribution has an associated reinvestment date. There are two types of distributions:

* Amount Type - these distributions are quoted as the actual value paid per fund unit.
* Rate Type - these distributions are quoted as a rate applied to the investor’s holdings.

In general, these distributions are paid according to a predetermined frequency, but are accrued to the investor daily. All distributions have an associated “reinvestment date” (sometimes called the ex-distribution date). This is usually the same as the payment date.

## Growth of $10,000 ##

The growth of $10,000 is a time series representing the performance of the fund assuming a theoretical investment of $10,000 was made at a some point in the past. Each distribution is assumed to be reinvested on its reinvestment date at the applicable offer price. The growth values are not load-adjusted. All unreinvested accrued distributions are added cumulatively to the growth value. Furthermore, the initial and ending price are based on bid NAVs.

To compute this growth measure, a series of “number of units held” must first be computed as follows:

IMAGE HERE

Where Nt is the number of shares outstanding as at date (or time) t, Pb,t is the fund bid price on date t, Po,t is the fund offer price on date t, and Dt is the distribution paid and reinvested on date t. 

Finally, the growth of $10,000 can be computed:

IMAGE HERE

Where Gt is the growth of $10,000 and Da,t is the unreinvested cumulative distributions accrued as at date t.

## Standardized Financial Statements ##

Almost all funds publish their audited financial statements every year. Valuehorizon standardizes these financials in accordance with its Fund Financial Statement Taxonomy™ to build a set of comparable financial time-series. IFRS changes to the treatment of certain items may be applied retroactively.

Some funds also publish unaudited financials quarterly or semiannually. Although these financials are not standardized, certain pertinent data may be extracted from these unaudited statements. These data usually relate to assets under management, subscriptions or redemptions. Valuehorizon provides financial statements for the following categories:

* Income Statement Data
* Balance Sheet Data
* Cash Flow Data
* Miscellaneous Data (including Changes in Equity Data)

The following caveats should also be noted:

* Data may be converted to another currency to allow a comparison to other funds.
* The accounting period may not be 12 months. In this case, the data may be pro-rated to represent a 12-month estimate.
* The financial year end may not necessarily be December 31.
* Unless stated otherwise, all data refer to the latest annual audited financial statement data for the calendar year.
* Standardization adjustments may create differences between the data presented and the published data. However, the summation figures (i.e. line item totals) presented will always be equivalent to the published figures.
* All data are based on restated figures where possible.

Valuehorizon also provides a set of financial statement ratios based on the standardized financial statements. These include return ratios, expense ratios and activity ratios.

With the exception of assets under management data, standardized financial statement and ratio data are generally not presented in this journal. However, they can be viewed, compared and downloaded online at www.valuehorizon.com/datasets. The online database methodology should be consulted for the definitions and interpretations of the various financial line items.

## Assets Under Management ##

Assets under management (AUM) is defined as the fund’s total assets less its total liabilities. It is commonly used in the calculation of the fund’s management and administration fees. It is also used in the calculation of the net asset value per unit figure quoted by open-end funds by dividing by the number of units outstanding.

AUM data are usually sourced from official fund documentation including (but not limited to) the following:

* Audited annual reports and financial statements.
* Unaudited quarterly financial statements.
* Fund reports including unitholder correspondence.
* Regulator reported statistics.

In cases where the AUM data reported is not in the fund’s primary currency, the data will be converted to the correct currency using forex rates on the applicable date. Forex rates are sourced from OANDA. 

The size of a fund is often a reflection of one or more of the following variables:

* The reputation of the fund manager - fund families with a long history of returns and relationships with investors often enjoy higher subscriptions and lower redemptions.
* The performance of the fund manager - funds that perform well both in terms of risk and return tend to get higher subscriptions.
* The economic climate - when equities are rallying, funds tend to flow into equity and balanced funds. When equities are declining, funds often experience a flight to quality into the often less risky fixed-income funds.
* Corporate actions - when funds change their prospectus terms, or experience other structural changes, they often experience a greater amount of subscriptions or redemptions depending on investors’ overall aggregate perception of whether or not the change is favourable.
* Subscription limits - some funds may limit the funds they accept due to a lack of available investments or over-subscription.

The size of a fund or family of funds is not always related to the performance of the fund manager, but can be attributed to a myriad of factors (as shown above).

## Holdings ##

Some funds provide data on the assets they own either as a set of aggregate statistics, a top holdings schedule or (in some rare cases), a full schedule of investments. 

Funds that provide aggregate holdings statistics usually do so by providing a breakdown of the funds holdings into one or more of the following categories:

* Currency
* Geographic Region
* Asset Category
* Time to Maturity (for fixed income investments)
* Credit Quality (for fixed income investments)

Valuehorizon does not track these aggregate holdings datasets. However, Valuehorizon tracks top holdings data as reported by various funds. If the “Percentage of Portfolio” of the top holdings are published by the fund, Valuehorizon also calculates an “Estimated Value” figure which is the percentage of portfolio multiplied by the latest assets under management figure as at the holdings reported date. The estimated value data are available online only.

## Fund Management and Custody ##

The investment decisions of a fund are governed by an entity known as the Fund/Investment Manager. This can be an individual person, a team, or a registered company or organization. The Investment Manager has the responsibility of making decisions in line with the investment objectives noted in the fund’s Prospectus.

The underwriting and distribution of the fund’s units is carried out by the Fund Sponsor. This is an entity that is usually, but not always, related to the Fund Manager by virtue of sharing the same parent entity.

The trust and custodial functions of a fund are carried out by an entity known as the Trustee. They are usually responsible for the administration of the fund, share registry, and calculation of net asset values. The Trustee’s responsibilities are governed by a document known as the Trust Deed or Declaration of Trust. A Trustee has a fiduciary responsibility to unitholders to manage the assets in accordance with the Trust Deed.


















