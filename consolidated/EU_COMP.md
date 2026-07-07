# European Consolidated Equities

This is a consolidated feed providing trade data and best bid/offer across European equity markets, giving a unified view of the European equity landscape.

* Country: Austria Belgium Switzerland Czechia Germany Denmark Spain Finland France UK United Kindom Greece Hungary Ireland Iceland Italy Luxembourg Netherlands Norway Poland Portugal Sweden [AT BE CH CY CZ DE DK ES FI FR GB GR HU IE IS IT NL NO PL PT SE]
* Mkt Hours: 08:00-17:00
* Time Zone: Europe/Paris
* Start Date: 20150101
* Real Time Available: No
* Bars Available: Yes
* Book Depth Available: No



Details are provided below

* `Table Schemas for EU_COMP`
* `Field Enumerations for EU_COMP`
* `Trading Hours for EU_COMP`
* `Recent Holidays for EU_COMP`



Includes the following coverage:

#### EU_COMP -  Coverage

| Security Type      |   # of Symbols | % of Total   |
|--------------------|----------------|--------------|
| Bond               |            115 | 0.39%        |
| Corporate Bond     |              9 | 0.03%        |
| Depository Receipt |            186 | 0.62%        |
| ETC                |            261 | 0.88%        |
| ETF                |           4478 | 15.01%       |
| ETN                |            403 | 1.35%        |
| Equity             |          18384 | 61.63%       |
| Fund               |           4680 | 15.69%       |
| Investment Fund    |           1273 | 4.27%        |
| Preferred Stock    |             17 | 0.06%        |
| Right              |             20 | 0.07%        |
| Unknown            |              1 | 0.0%         |
| Warrant            |              1 | 0.0%         |
| Total              |          29828 | 100%         |


Consists of 3 Databases

* `EU_COMP`  - Tick Data
* `EU_COMP_BARS`  - 1 Minute Bars
* `EU_COMP_DAILY`  - End of Day Metrics




## EU_COMP

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* NBBO - National Best Bid / Offer quotes
* QTE - Best bid / offer quotes
* STAT - Static data, e.g. ISIN, description, security type
* TRD - Trades





## EU_COMP_BARS

